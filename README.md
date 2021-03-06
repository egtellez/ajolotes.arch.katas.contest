# Architectural Katas Contest Summer 2022
This repository hosts anything related to the ajolotes team architectural katas contest
<table>
<tr>
<td width="30%">
<img src="axolotl.jpg" alt="axolotl, our team´s mascot" width="200"/>
</td>
<td>
Ajolotes are used in laboratories to study a superpower: regenerating their limbs, lungs, heart, jaws, spines, and even parts of their brain! Scientists have found that axolotls can regrow a new limb five times perfectly, in a few weeks—without even a scar.
</td>
</tr>
</table>

### Users Identified

* Non-Profit User --> Interacts with the Platform
* Community Leader/Mentor --> Assigns non-profit assignments / role based training assignment / schedules meeting with non-profit

* Administrator --> Require community configuration / specifying community leader / Analytics
* Candidate --> Registration / engagement
* Career Mentor --> Uploads roadmap to system, updates assignment

## Architecture characteristics identified

- Ease of Use.
- Robustness.
- Performance.
- Availability (How to manage maintenance / load balancers / database mirroring / backups).
- Simplicity (Related to ease of use / Reated to workflows).
- Authentication/Authorization (Use standards).
- Privacy (Defining privacy policies, making them available to customers) / Protecting data (Encryption at rest / Traffic encryption / etc..).
- Legal (Providing legal notice from the site).
- Integration (Authentication services authentication).
- Deployability (Continuous delivery / Multiple environments / dev / uat / prod).
- Testability (TDD, Functional tests, Integration tests, etc) Multiple environments before hitting prod.

(To expand the system - Not initially)
- Scalability 
- Elasticity
- Reliability
- Customizability 


### Ease of Use Architecture considerations - UX Focus

#### Front-end experience

The portal will be accessed as a web application that follows HTML 5.0 Standards. Will provide a reactive UI that is responsive to the users. Will use a framework such as React, Angular or Vue to enable the front-end experience.



#### Back-end experience

- Performance/Fast response to the user
- Robustness (Fail gracefully)


#### General UX guidelines

* Use simple language that people can understand.
* Workflow: Step by step processes, and mechanisms to start from where the users left off.
* Provide guidance through images / videos, etc about system features.
* Provide online support for people that needs help/clarification:
        Online chat
        Chatbot
        Call with support person
* Support all current commercial browsers: Chrome, Safari, Edge, Firefox.
* Support different devices (phone / tablet / ).
* Atomic operations / Easy to process and retrieve.


 Will support enhanced experience for people with disabilities:
* People with color blindness - Use right contrast for site colors and texts.
* People with hand injuries - Add keyboard shorcuts to ease the usage.
* People who is hard of hearing - Add captions if video content is provided or audio content is provided.
* People who is blind - Use friendly html structure so the screen readers are able to interpret the app. Also include alt text on images. 
* People with dislexia / attention deficit: Provide different ways to navigate the site / find information, avoid unnecessary distracting content.


## Overall Architecture

We are proposing a monolithic architecture for this application for the following reasons:
1. The business logic is relatively simple. 
2. The user load is expected to be low, with estimated concurrent users in the low-thousands maximum.
3. User interactions will be low bandwidth, with the largest potential bandwidth items being document files. Large multimedia files will not be used, for example.
4. Design, deployment, and maintenance will be simpler and more cost-effective for a non-profit setting.
5. Due to common workflow elements, we will be able to reuse common code components.

### Data Storage

We propose using a NoSQL Database, such as MongoDB. 
*Architectural Decision Record: Do not have enough details about the data model and this allows to iterate the data model and helps iterate through a final solution. 

#### Advantages

You can quickly make changes to the data model to support new features for the system. E.G. Adding new attributes to a candidate or a non-profit or enhancing the capabilities data model.


#### Trade-offs

NoSQL databases don't have data integrity because the model from one iteration to the other can be entirely different.


### Authentication/Authorization

OAUTH2.0 / Facebook Authentication / Google Authentication
We're proposing to use public service providers for authentication. We are assumming that most of the non-profit organizations have already a facebook page or some social network where they connect with the community so they can use their account to authenticate to the platform. Similarly, we assume that users will have access to a public account such as these.

Advantages: Non-profits can link their Facebook/Instagram/Google/Twitter/etc. profiles into the portal.

Trade-off: Requires following guidelines from third party companies. Potentially multiple guidelines if allowing different services to authenticate.

