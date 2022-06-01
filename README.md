# Architectural Katas Contest Summer 2022
This repository hosts anything related to the ajolotes team architectural katas contest

### Users Identified

* Non-Profit User --> Interacts with the Platform
* Community Leader/Mentor --> Assigns non-profit assignments / role based training assignment / schedules meeting with non-profit

* Administrator --> Require community configuration / specifying community leader 
* Candidate --> Registration / engagement
* Career Mentor --> Uploads roadmap to system, updates assignment

## Architecture characteristics identified

* Ease of Use
* Authentication/Authorization
* Privacy 
* Legal
* Robustness
* Performance
* Availability


### Ease of Use Architecture considerations - UX Focus

Front-end experience

The portal will be accessed as a web application that follows HTML 5.0 Standards. Will provide a reactive UI that is responsive to the users. Will use a framework such as React, Angular or Vue to enable the front-end experience.

Back-end experience

- Performance/Fast response to the user
- Reliability/Robustness (Fail gracefully)
- 

General UX guidelines: 

* Use simple language that people can understand
* Step by step processes, and mechanisms to start from where left
* Provide guidance through images / videos, etc about system features
* Provide online support for people that needs help/clarification
        Online chat
        Chatbot
        Call with support person
* Support all current commercial browsers: Chrome, Safari, Edge, Firefox
* Atomic operations / Easy to process and retrieve
 

 Will support enhanced experience for people with disabilities:
* People with color blindness - Use right contrast for site colors and texts
* People with hand injuries - Add keyboard shorcuts to ease the usage
* People who is hard of hearing - Add captions if video content is provided or audio content is provided
* People who is blind - Use friendly html structure so the screen readers are able to interpret the app. Also include alt text on images. 
* People with dislexia / attention deficit: Provide different ways to navigate the site / find information, avoid unnecessary distracting content

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

Trade-offf: Requires following guidelines from third party companies. Potentially multiple guidelines if allowing different services to authenticate








