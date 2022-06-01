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

# TODO:
> - Define Architecture style (Monolith vs Distributed) Which model from these options?
> - Continue Visio Flow Diagram for Scenario: Career Case Management Functionality & Process
> - Identify components (Flow diagrams / Event storming / any other technique)
> - Upload diagrams (Architecture style / Components / Support diagrams. E.G. Flow diagrams / Event storming C4, etc..)
> - Write ADRs (Architecture Decision records)
> - Better organizing repo structure / folders / documents / sections
> - Any other activity the team identified

### Users Identified

* Non-Profit User --> Interacts with the Platform
* Community Leader/Mentor --> Assigns non-profit assignments / role based training assignment / schedules meeting with non-profit

* Administrator --> Require community configuration / specifying community leader / Analytics
* Candidate --> Registration / engagement
* Career Mentor --> Uploads roadmap to system, updates assignment

### Questions
- How many candidates for each career mentor? Review examples from Omar
  - E.G. 1 Mentor - 3 mentees (Full time job?)  How many people can a mentor mentor
- Application exists to manage non-profits?
  - Some options for non profits: https://connecteam.com/nonprofit-apps/


## Architecture characteristics identified

- Ease of Use
- Robustness
- Performance
- Availability (How to manage maintenance / load balancers / database mirroring / backups)
- Simplicity (Related to ease of use / Reated to workflows)
- Authentication/Authorization (Use standards)
- Privacy (Defining privacy policies, making them available to customers) / Protecting data (Encryption at rest / Traffic encryption / etc..)
- Legal (Providing legal notice from the site)
- Integration (Authentication services authentication)
- Deployability (Continuous delivery / Multiple environments / dev / uat / prod)
- Testability (TDD, Functional tests, Integration tests, etc) Multiple environments before hitting prod

(To expand the system - Not initially)
- Scalability 
- Elasticity
- Reliability
- Customizability 


### Ease of Use Architecture considerations - UX Focus

Front-end experience

The portal will be accessed as a web application that follows HTML 5.0 Standards. Will provide a reactive UI that is responsive to the users. Will use a framework such as React, Angular or Vue to enable the front-end experience.



Back-end experience

- Performance/Fast response to the user
- Robustness (Fail gracefully)


General UX guidelines: 

* Use simple language that people can understand
* Workflow: Step by step processes, and mechanisms to start from where left
* Provide guidance through images / videos, etc about system features
* Provide online support for people that needs help/clarification
        Online chat
        Chatbot
        Call with support person
* Support all current commercial browsers: Chrome, Safari, Edge, Firefox
* Support different devices (phone / tablet / )
* Atomic operations / Easy to process and retrieve


 Will support enhanced experience for people with disabilities:
* People with color blindness - Use right contrast for site colors and texts
* People with hand injuries - Add keyboard shorcuts to ease the usage
* People who is hard of hearing - Add captions if video content is provided or audio content is provided
* People who is blind - Use friendly html structure so the screen readers are able to interpret the app. Also include alt text on images. 
* People with dislexia / attention deficit: Provide different ways to navigate the site / find information, avoid unnecessary distracting content


## Examples of possible components / technologies

### Data Storage

No-SQL Database: Mongo DB. Architectural Decision Record: Do not have enough details about the data model and this allows to iterate the data model and helps iterate through a final solution. 

Advantages

Quickly do changes in the data model to support new features for the system. E.G. Adding new attributes to a candidate or a non-profit or enhancing the capabilities data model


Trade-offs

Doesn´t have data integrity because the model from one iteration to the other can be entirely different


### Authentication/Authorization

OAUTH2.0 / Facebook Authentication / Google Authentication
We are assumming that most of the non-profit organizations have already a facebook page or some social network where they connect with the community so they can use their account to authenticate to the platform

Advantages: Non-profits can link their facebook/instagram/google/twitter/etc profiles into the portal

Trade-off: Requires following guidelines from third party companies.Potentially multiple guidelines if allowing different services to authenticate








