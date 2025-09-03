---
title: "Reports cookbook"
slug: "reports-cookbook"
excerpt: ""
hidden: true
createdAt: "Mon Oct 01 2018 05:31:25 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
The objective is to list down commonly used reporting patterns in form of working recipe, that can be reused OpenCHS development team.

## Components of line listing

- Hierarchical service area information (e.g. catchment and village)
- Individual identification details
- Programmatic details (registration date, enrolment date, exit date, number of visit)
- Field data element(s)
- Aggregated to individual data

## Good practices in report design

On a dashboard when there are multiple reports with aggregate information against the same set of dimensions, in such a case from the usability perspective consider keeping the number of rows same.

## Individual level reports

- [RECOMMENDED: List of individuals with their key details pulled up from their health record](https://reporting.openchs.org/question/165?catchment=JSS%20Master%20Catchment&en_status=Yes)
- [List of individuals with observations from latest program encounter](https://reporting.openchs.org/question/153)
- [List of individuals with their key registration, enrolment, follow-up aggregate details (number of visits, registration date, etc)](https://reporting.openchs.org/question/143)
- [List of individuals with observations between two dates](https://reporting.openchs.org/question/162)

## Aggregate reports

- [Count of program encounter and program enrolment observations by address](https://reporting.openchs.org/question/129)
- [Count of most recent program encounter observation by address](https://reporting.openchs.org/question/145) 

## Sync report

## Immunisation related reports

- [Immunisation details of individuals](https://reporting.openchs.org/question/132)
- [Line list of immunization](https://reporting.openchs.org/question/132?catchment=Ashwini%20Master%20Catchment) 

## Child anthropometry related reports

- [Grade wise statistics by age group](https://reporting.openchs.org/question/156)
- [Gradewise statistics](https://reporting.openchs.org/question/135)
- [Weight gain](https://reporting.openchs.org/question/162?catchment=JSS%20Master%20Catchment)

## Pregnancy related reports

- [ANC and Delivery Statistics](https://reporting.openchs.org/question/129)

## **Reports Nomenclature - Metabase**

**Report Name – **  
`[Not Released/Do not use]`, use this tag for the report if this is not supposed to use by the user.  
Start the name of each report with the implementation name like Phulwari, CK, IHMP etc. (so that we know which report we have created as going forward we are going to train them for ‘Analyze query’ option and this has the option to save the report.)  
A name should be preferably given by Client. (So that they can relate. maybe the same name as they were using in the previous system)  
If not given by client it should have the name of the encounter on which the report is supposed to calculate.  
With every report, we should give a directory in which the column names are defined or elaborated.  
Field Name –  
The column name should be the same throughout all the reports in an implementation. e.g.: DOB, Reg Date, Age etc.

**Definitions:**  
_Registration:_ Entering an individual in the system by clicking on the ‘Register’ in the application.

_Enrollment: _There might be the various program running in an organisation. So the registered individual needs to be enrolled in a particular program that s/he is eligible for.

_Encounter:_ Any type of visit done in the system is encounter. The individual that is enrolled in any program, there will be few visits that need to be done at a particular time.

_Catchment:_ Area of intervention is divided amongst the smaller area that is called catchment. The catchment is the work area for the health worker.

_Individual:_ Everyone registered in the system.

_Voided:_ The individual that is recorded twice or recorded by mistake. Then we ‘void’ these individuals, so that they are not shown in the reports or in the application to avoid confusion.
