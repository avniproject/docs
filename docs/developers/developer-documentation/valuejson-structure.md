---
title: "ValueJSON structure"
slug: "valuejson-structure"
excerpt: ""
hidden: true
createdAt: "Thu Jan 19 2017 12:22:39 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
On the front-end the Observation has valueJSON field that stores observation values. The structure of that can be understood from the examples below:

Multiselect (conceptUUID is the uuid of the answer which is a concept)  
{ answer: [ {conceptUUID: '00828291-c2fe-415f-a51e-ba8a02607da0’}, {conceptUUID: '00828291-c2fe-415f-a51e-ba8a02607da0’} ] }

SingleSelect  
{ answer: { conceptUUID: '00828291-c2fe-415f-a51e-ba8a02607da0' }  }

Numeric  
{ answer: 1}  
{ answer : null}

Boolean Dated  
{ answer: {value: true, date: DATE}}
