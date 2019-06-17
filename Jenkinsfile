pipeline {

  agent {
    dockerfile {
      label 'vagov-general-purpose'
      args '-v /etc/pki/ca-trust/source/anchors:/usr/local/share/ca-certificates'
    }
  }

  // $HOME defaults to '/' when not set, which results in:
  //   Error: EACCES: permission denied, mkdir '/.npm'
  // jenkins runs docker using '-w <WORKSPACE>', so '.' points
  // to that WORKSPACE
  environment { HOME = '.' }

  stages {

    stage('Update VA CA Certificates') {
      steps {
        sh 'pwd'
        sh 'ls -l'
        sh 'whoami'

        // sh 'cp /va_certs/dod-eca.pem dod-eca.crt'
        // sh 'cp /va_certs/VA-Internal-S2-ICA1-v1.pem VA-Internal-S2-ICA1-v1.crt'
        // sh 'cp /va_certs/VA-Internal-S2-ICA2-v1.pem VA-Internal-S2-ICA2-v1.crt'
        // sh 'cp /va_certs/VA-Internal-S2-RCA-v1.pem VA-Internal-S2-RCA-v1.crt'
        // sh 'cp /va_certs/va.pem va.crt'

        // sh 'sudo cp *.crt /usr/local/share/ca-certificates/'
        sh 'update-ca-certificates'
      }
    }

    stage('Checkout Code') {
      steps {
        checkout scm
      }
    }

    stage('Install npm dependencies') {
      steps {
        sh 'npm install'
        sh 'bundle install'
      }
    }

    stage('Build static site') {
      steps {
        sh 'npm run build'
        sh 'bundle exec jekyll build'
      }
    }

    stage('Tar assets and upload to S3') {
      when {
        expression { env.BRANCH_NAME == 'master' }
      }
      steps {
        sh 'tar -C _site -cf _site.tar.bz2 .'

        withCredentials([[
          $class:           'UsernamePasswordMultiBinding', 
          credentialsId:    'vetsgov-website-builds-s3-upload',
          usernameVariable: 'AWS_ACCESS_KEY', 
          passwordVariable: 'AWS_SECRET_KEY']]) {
          sh "s3-cli put --acl-public --region us-gov-west-1 _site.tar.bz2 s3://bucket-vagov-design-builds-s3-upload/$GIT_COMMIT/site.tar.bz2"
        }
      }
    }

    stage('Deploy dev & staging') {
      when {
        expression { env.BRANCH_NAME == 'master' }
      }
      steps {
        script {
          commit = sh(returnStdout: true, script: "git rev-parse HEAD").trim()
        }

        build job: 'deploys/vets-design-system-documentation-vagov-dev', parameters: [
          booleanParam(name: 'notify_slack', value: true),
          stringParam(name: 'ref', value: commit)
        ], wait: false

        build job: 'deploys/vets-design-system-documentation-vagov-staging', parameters: [
          booleanParam(name: 'notify_slack', value: true),
          stringParam(name: 'ref', value: commit)
        ], wait: false
      }
    }
  }
}