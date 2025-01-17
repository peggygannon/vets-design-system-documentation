---
layout: default
title: Benefit applications
draft: true
anchors:
  - anchor: Eligibility
  - anchor: How to apply
  - anchor: Apply now
  - anchor: After you apply
---

# Benefit applications

<p class="va-introtext">Benefit applications are where users can go to apply for benefits in any of the benefit hubs on VA.gov. The policies and regulations around these benefits are very complex, and users often have difficulty determining if they are eligible, what they need to provide, and what to expect after they've submitted their application. For this reason, benefit applications, as a pattern, are divided into four distinct "epics" that help users navigate the process from start to finish.</p>

The four epics typically found within each benefit application are:

1. [Eligibility](#eligibility)
2. [How to apply](#how-to-apply)
3. [Apply now](#application-introduction-apply-page)
4. [After you apply](#after-you-apply)

Structuring benefit applications in this way has, through rigorous usability testing, demonstrably improved how to educate users about the benefits and how to set expectations about the application process. For the Department of Veterans Affairs, this means that applications are more accurate and complete, so the Department to better serves its constituents.

## Eligibility

For Veterans, determining whether or not they (or their beneficiaries) are eligible for a specific benefit is a difficult process. The policies governing those benefits can be complex, fraught with dependencies and variations that can be overwhelming.

The associated pattern of content and functionality designed to help users of the website understand their eligibility, therefore, needs to accomplish a few things which can seem at odds with one another. Manifested as a single page, it should:
* Provide a simple introduction to eligibility rules that covers the most common scenarios.
* Scale (expand) to represent variations in complexity.
* Prevent users from going to the wrong form.
* Provide the ability to announce changes in the law or availability of benefits that may impact their eligibility.
* Provide space to connect users to benefits that are likely to be related to their question about the benefit they are viewing.
* Guide users to the next logical step in determining their eligibility, ultimately concluding getting them to the proper benefit application.

### Eligibility hierarchy
The hierarchy of the eligibility pattern allows it to be flexible enough to cover simple or complex benefit eligibility information while still feeling straightforward and easy to follow. Generally, the eligibility pattern manifests itself as a single web page. It sits within a benefits hub based upon the following rules:

* For benefits hubs with a single benefit (such as [Health care](https://www.va.gov/health-care)), we link to a separate [Eligibility](https://www.va.gov/health-care/eligibility/) page as well as [How to apply](https://www.va.gov/health-care/how-to-apply) page from the hub landing page.
* For benefits hubs with multiple benefits (like [Life insurance](https://www.va.gov/life-insurance/)), we link to the [main options/Eligibility](https://www.va.gov/life-insurance/options-eligibility/) page from the hub landing page. From this page, the user can choose the option for which they want to explore their eligibility.
* For a benefits hub where there is only a single benefit available, such as [Veteran's Pension](https://www.va.gov/pension/), we link directly to the [Eligibility](https://www.va.gov/pension/eligibility/) and page for that benefit from the hub landing page. We also link to pages for other, related benefits (Aid and Attendance, and Survivors Pension) from the hub.

The eligibility page consists of the following elements:

![eligibility_page_heirarchy](/images/eligibility_page_heirarchy.png)

#### A. Title and statement of intent
The title should be “Eligibility for (Most Commonly Used Benefit Name).” The statement of intent should state the job the page will do for the user, by stating something like “Find out if you are eligible for (most commonly requested benefits, described in plain language). This allows a user to quickly assess if they are in the right place, and it helps search engines highly rank these pages for appropriate searches.

#### B. Critically important information (most common scenario)

The featured content component is used to present the user with the most commonly sought benefit eligibility scenario. Some benefits are complex and contain several optional paths to confirmation. It is not acceptable to repeat this element on the page; instead use the Additional eligibility information &amp; scenarios element for other variations. Note: please do not use this pattern more than one time on the page as it decreases its effectiveness at drawing the eye to the most likely sought content.

<div class="do-dont">
<div class="do-dont__do">
<h3 class="do-dont__heading">Do</h3>
<div class="do-dont__content" markdown="1">
Use a single featured component for the most common scenario.
![eligibility_page_heirarchy](/images/featured-content-do.png) 
</div>
</div>
<div class="do-dont__dont">
<h3 class="do-dont__heading">Don’t</h3>
<div class="do-dont__content" markdown="1">
Use two or more featured components for multiple scenarios, because their can't be more than one that is the most common. Use other page elements for this purpose.
![eligibility_page_heirarchy](/images/featured-content-dont.png) 
</div>
</div>
</div>

[View the featured content component](https://design.va.gov/components/featured-content).

#### C. Additional eligibility information &amp; acenarios

Benefit eligibility or requirements information that is more nuanced than the summary placed inside the Common scenario overview (featured content component), including different requirements for sub-audiences, application assistance, etc.  Group prerequisites logically by benefit type, and order benefit types from most common to less common.

![eligibility_prerequisites](https://user-images.githubusercontent.com/50150810/58469821-3a6ec380-8138-11e9-85bf-0bd2f6292aec.png)

#### D. Optional: Eligibility change announcement

When time sensitive content about a benefit — such as a new benefit being made available or a significant change in the laws around eligibility for a particular benefit — you can place an informational alert box on this page. Follow the recommendations governing alert box usage, including
* Use informational alerts to announce upcoming benefits
* Use inoformational alert boxes with expandable content to hide detail that may not apply to everyone visiting the page

[View the alert box component](https://design.va.gov/components/alertboxes).

#### E. How to apply heading and primary call-to-action button

A brief heading should precede and call attention to the primary call to action button. This heading can be followed by an optional single sentence of text or phrase if necessary.

The button will lead the user/applicant to one of two places: either the application flow for the benefit or a wizard mini-form interface allowing the user to self-select into (or out of) the appropriate benefit form.

Having a single green button on the page helps the user follow the most logical path. Note: never put more than one green button on the page. If you have a page that requires multiple benefit form links, use the wizard mini-form interface to create branching logic to get the correct benefit application (or prevent a user from applying to the wrong benefit).

The button can be followed by item 6, Additional Benefit-Eligibility-Specific Relevant Content, if necessary.

[View the button component](https://design.va.gov/components/buttons).

##### F.Optional: Wizard pattern for branching eligibility choices

In the case where there are multiple benefit options, the [Wizard pattern](https://design.va.gov/patterns/wizards) allows a user to branch into the appropriate benefit application from the eligibility page.

The text on the primary green button should represent the job the wizard is performing, such as “Find your education benefits form.”

#### G. Optional: Additional benefit-eligibility-specific relevant content

Any additional content necessary that is connected to the primary benefit eligibility use case for the page can be added here.

#### H. Optional: Benefit eligibility frequently asked questions

Use the accordion component to present questions that are common about eligibility for a benefit.

[View the accordion component](https://design.va.gov/components/accordions).

#### I. Optional: Related benefits content

Any additional benefits (e.g. vocational benefits eligibility that is related to education benefit eligibility) can be added to the bottom of the page using the RELATED PAGES component.

## How to apply
**_draft_**
This is a high-level description of the “How to Apply” page for benefit applications. The content recommended for the “How to Apply” page may overlap with the “Eligibility” or “Apply now” sections.

### Intro text
Intro text is required and describes what the page is about. For the “How to Apply” page, the intro text usually includes the following:
* The benefit(s) the application is for
* The type(s) of users the application is aimed at (Veteran, service member, qualified family member)
* SEO keywords (See [Writing for SEO](https://design.va.gov/content-style-guide/seo).)

### Preparing to apply (informational callout)
On the “How to Apply” page, use the [informational callout](https://design.va.gov/patterns/content-presentation) box to present chunked, scannable snippets of critical information needed by the majority of applicants. For example,

* describe what a user needs to do before they begin the application
* list items needed to complete the application (SSN, military history, etc.). Required items should be called out.

Note: The blue [informational callout](https://design.va.gov/patterns/content-presentation) box should only be used for the most important information on the page. Since it includes critical information, the callout should appear near the top of the page.

### How do I apply?
The “How do I apply" section lists possible application methods. It should emphasize the optimal path for Veterans, (which may be how to get help from a human instead of online help.) Some common application methods are:
* Online
   * green CTA button
* By mail
   * Link to the printable application form
   * Instructions for mailing the completed, printed form
* In person
   * link to find nearest VA regional office
* With the help of a trained professional
   * link to get help

### What happens after I apply?
The “What happens after I apply” section sets the user’s expectations about what will happen next in the application process. This section may include:

* Concise content or a link to a page describing what the user can expect after they apply
* A call to action (primary blue button) that allows the user to track the status of their application
* A card that sets the user’s expectation for how long it takes to receive a response

### Optional: More information
Include the “More information section” if there is helpful supporting information about applying for the benefit.
* For many short content items, consider using the accordion component to reduce the content on the page.
* For longer content items, consider linking to a separate page.

### Live examples
* [How to apply for VA health care](https://www.va.gov/health-care/how-to-apply/)
* [How to file a VA disability claim](https://www.va.gov/disability/how-to-file-claim/)
* [How to apply for the GI Bill and other education benefits](https://www.va.gov/education/how-to-apply/)
* [How to apply for a VA pension as a Veteran](https://www.va.gov/pension/how-to-apply/)

## Apply now

**_draft_**
This is a high-level description of the introduction page for benefit applications.
### File for [benefit] header
VA paper form equivalency appear under the page header. This shows the equivalent VA paper form
*Equal to VA Form 21-526EZ (Application for Disability Compensation and Related Compensation Benefits).*

### Sign-in
Message when a user isn't signed in:
- Lets applicants know that by signing in some information from their profile account could be prefilled into the application and that they can save their work as they go.  
- Gives time on how long the application will be saved for
- Blue CTA button *Sign In to Start Your Application*
- Link to fill out the application without signing in. (For all online applications except for Disability Compensation)

[screenshot]
![signed out.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/1d5d3f75-9047-44d1-8ebb-93c5c7c25e53)

Message when a user is signed in:
- Lets applicant know they are signed in and can save work as they go
- Green CTA button

[screenshot]
![signed in message.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/a965f3f5-5065-4b54-bfda-5ebb5452e4bb)

### Subway map
Subway, or process, map (https://design.va.gov/components/process-list) shows the applicant the steps they need to take to apply for a benefit. The headings are action words, short and concise, and consistent across forms.

**Prepare**
- Gives the applicant the information they’ll need to fill out the form, such as if they need to submit any documentation or provide their SSN, bank information, military history, spouse information, etc.
- Items that are optional are called out.

**Apply**
We use the same language for this step across all forms:
*Complete this [benefits] form. After submitting the form, you’ll get a confirmation message. You can print this page for your records.*

Within the **Apply**  header we also include content about how an applicant can get help filling out the form. This message is also consistent across all form introduction pages:

*What if I need help filling out my application? An accredited representative, like a Veterans Service Officer (VSO), can help you fill out your claim.*
[Get help filing your claim]

**VA Review**
The step tells applicants how much time it takes VA to review the application.  The content under this heading depends on what type of benefit they're applying for. For example:
{for Health Care) *We process health care claims within a week.*
(for Education) *We usually process claims within 30 days. We’ll let you know by mail if we need more information.*
(for Disability) *We process applications in the order we receive them. We may contact you if we have questions or need more information.  The amount of time it takes to review your claim depends on:
  *xxxyxlxlx
  *
  *

**VA Decision**
This step tells applicants how and when they will be informed of the status of their application (if denied or approved) and the next steps. It sets the user’s expectation for how long it takes to receive a response.


### Other components on the intro page
Depending on the type of benefit, we sometimes include an alert box with specific info about that benefit (https://design.va.gov/components/alertboxes).
This is an optional component and should only be used if there is an important benefit or application process to call out to the applicant.  
[screenshot]
![alert box.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/05c0adb9-7d2d-4040-8d2f-9742273d7771)


### OMB information
This appears at the bottom of the Introduction page and shows
•	Respondent burden
•	OMB control number
•	Privacy act (link)


### Need help?
This footer appears on the bottom of every page of the form. It includes phone numbers if an applicant needs more support or has questions about filling out the form.

### Page examples
https://www.va.gov/disability/file-disability-claim-form-21-526ez/introduction
https://www.va.gov/education/apply-for-education-benefits/application/1990/introduction
https://www.va.gov/burials-and-memorials/pre-need/form-10007-apply-for-eligibility/introduction
https://www.va.gov/pension/application/527EZ/introduction


## After You Apply
This is a high-level description of the “After You Apply” page for benefit applications.


### Intro text
Intro tex describes what will happen next in the application process after an applicant submits their applications. This section may include:
* What an applicant needs to do after they submit their application.
* SEO keywords (See [Writing for SEO](https://design.va.gov/content-style-guide/seo).)

### When will I hear back about my application?
This section appears as  card or gray alert box (https://design.va.gov/components/alertboxes) that sets the user’s expectation for how long it takes to receive a response and includes:
* Content or a link to a page describing what the user can expect after they apply
* Time frame for how long it takes to receive a response

[screenshot, HCA]
![HCA alert box.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/e1800594-661b-475c-9c4d-4172ae9d39eb)

[screenshot EDU]
![EDU alert box.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/bef3a079-2203-4e0a-a6d3-01e2c007b9bd)

[screenshot Disability]
![Disability alert.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/68505b40-9ded-4f32-b256-a33c79aa9b49)

[Preneed has this info, but not in a card or grey alert box]

![Preneed alert.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/895cf031-bb1d-4a88-ac72-5849e22596cd)



After “When will I hear back about my application” header, each of the “After You Apply” pages diverge on format. I’ve listed each page below with a brief description what appears on the page  

### HCA After You Apply
The following are the subheads on the Health Care After You Apply page
#### If you approve my application what do I do next?
On the Health Care After You Apply page, the content appears as subway process map with next steps for the applicant.

[screenshot]

![HCA subway map.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/83e01440-ba5c-4c4a-bd0d-8fc73674bc72)

### Other questions
Series of accordions addressing follow up questions an applicant might have

[screenshot]
![HCA other questions.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/051a50e4-0bde-4000-8b77-ab3aa1242d6f)


### Education After You Apply
#### What should I do while I wait?
Content describing what the user can do while they wait

#### What happens after I apply?
Content describing what the user can expect after they apply

[screenshot]
![EDU after apply.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/0866e978-6889-4656-8980-29e98a94165d)

### Disability After You Apply Page
#### The amount of time it takes to review your claim depends on:
Bullets points listing the factors that go into how long it takes to process a claim

### What should I do while I wait?
Content describing what the user can do while they wait to hear about their claim.
Includes Track Your Claims CTA blue button

[screenshot]

![Disibility with blue button.png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/fbbce6a9-0e19-4865-9772-85c7c36533e9)

#### What happens after I file a claim
Subway process map underneath this header about how a claim is processed

[screenshot]
![2019-05-23 (7).png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/ec75ac94-5a6e-4b72-b4fc-17151889962b)

#### What should I do if I disagree with a decision on my claim?
Content describing what the user options the user has if they disagree with a VA decision.

[screenshot]

![2019-05-23 (8).png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/26a3f97b-a732-433b-8752-cb9422d337eb)

### Pre-Need After You Apply

#### If I qualify for burial, how will VA notify me of the decision?
Content describing how VA inform the applicant the decision on their application.

[screenshot]
![2019-05-23 (9).png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/e9345765-8aea-4d3f-95d1-1f73588ab622)

#### What happens if VA decides I don’t qualify for burial in a VA national cemetery?

#### Can I appeal the decision?

#### What if I have other questions?

[screenshot]
![2019-05-23 (10).png](https://images.zenhubusercontent.com/59b0414bb0222d5de476aa22/2ecfaefe-6286-4e5c-bd68-b28068b2a5f3)

