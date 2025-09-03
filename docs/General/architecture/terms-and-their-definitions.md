---
title: "Terminology"
slug: "terms-and-their-definitions"
excerpt: "Specific terminology used in Avni to help in quick understanding of the data model and underlying concepts."
hidden: false
createdAt: "Fri Oct 25 2019 03:56:32 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
There is some terminology that has a specific meaning within Avni listed here. Understanding this will be useful to understand some of the documentation on this site. 

## SYSTEM-WIDE Terminology:

- **Organisation ** - Avni has a multi-tenant architecture where multiple organisations can share the same server. A tenant in an Avni installation is called an organisation. Under an organisation one can have users, configuration (like programs, forms, settings, etc) and data (like subjects, visits, etc). 
- **Implementation** - Technically, this means the implementation of an organisation within Avni. However, this term is usually used interchangeably with Organisation. 
- **Subject** - Users in an organisation usually record data about one or more "subject types". A subject type could be a _person_, a _building_, a _dam_, or anything against which long-term data is to be recorded. 
- **Individual** - In earlier versions of Avni, there could be only one subject type - an individual. _Subject types_ were introduced to the system later so that data can be recorded not just for people, but for any entity (or Subject). You might still find the term called individual in some places in Avni. All these will be replaced by the appropriate Subject term soon. Avni is already being used in places where the Subject being monitored is not a person, but an entity - like a "dam", etc. 
- **Location** - In Avni, it is mandatory to associate a subject to a location. A location could be geographic (state, village, etc) or class-rooms, etc. Locations have hierarchy support. 
- **Catchment** - A catchment is a group of locations that are monitored by a user. If there are multiple users assigned to a single catchment, they will all have access to the same data about subjects and their information under that catchment area. 
- **Form** - All information captured during registration, encounter, program enrolment, program encounter, program encounter cancellation, program exit, etc are captured through forms defined through the admin app. 
- **Concept** - This is the underlying meaning of a question asked in a form. It can be the same as the form question but can be different as well. For example, the question asked could be "_Please enter the height of a person_", while the underlying connected concept to this question could be "_Height_". Concepts provide a level of indirection between the visual form and the underlying data model and allow for validation and reporting or aggregation.

## USERS & ENCOUNTERS Terminology

- **User** - A person who can log in to the Avni system is a user. 
- **Organisation Admin** - A high-privilege User who can log in to the Avni Administration Web App for their organisation, and perform Admin functionality. 
- **Registration** - The process of creating a new _Subject_ in the system is called Registration. A subject registration is usually associated with a form that can be customized to the subject type and the implementation. 
- **Encounter** - All observations about a subject recorded at a specific point in time is called an encounter. The term is interchangeably used for visits as well. 
- **Encounter Type** - Represents the type of encounter. This helps determine the set of questions that need to be asked during an encounter. For example, there might be a _monthly_ visit where some questions are asked, while different questions are asked during a _quarterly_ visit. 
- **Visit** - Alias to encounter

## PROGRAM Terminology

- **Program** - Information about a subject can be structured into different programs that they can be enrolled in. eg: pregnancy program, vaccination program, etc. A program comprises a name, forms for program enrolment, encounter types and their related forms, and visits scheduling logic. 
- **Program Enrolment** - is the process by which a subject enrolls into a program. Enrolment is usually associated with a form that is used for baseline information when starting a program. 
- **Program Exit** - is the process by which a subject exits from a program. An exit is usually associated with a form. 
- **Program Encounter** - is an encounter that is related to an enrolment. 
- **Program Visit ** - is the same as program encounter
- **Visit Schedule** - is usually defined for a program. It can be dynamically calculated after a program enrolment or a program encounter. Logic to define a visit schedule is usually specific to the implementation and is defined using the visit scheduling extension point. 

## DOMAIN MODEL - DIAGRAM

A nice view of the domain and usage is provided in the [Implementer's concept guide - Introduction](doc:implementers-concept-guide-introduction). Head over there for a more detailed view of the system in action.
