---
title: "My Dashboard and Search Filters"
slug: "my-dashboard-and-search-filters"
excerpt: ""
hidden: false
createdAt: "Fri Jan 03 2020 05:01:30 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
Avni allows the display of custom filter in **Search** and **My Dashboard filter** page. These settings are available within App designer. Filter settings are stored in organisation_config table.  You can define filters for different subject types. Please refer to the table below for various options.

# Filter Types

[block:parameters]
{
  "data": {
    "h-0": "Type",
    "h-1": "Applies on Field",
    "h-2": "Widget Types",
    "0-0": "Name",
    "0-1": "Name of the subject",
    "0-2": "Default (Text)",
    "1-0": "Age",
    "1-1": "Age of the subject",
    "1-2": "Default : Numeric field. Fetches result matching records with values +/- 4.",
    "2-0": "Gender",
    "2-1": "Gender of the subject",
    "2-2": "Default : Multiselect with configured gender options.",
    "3-0": "Address",
    "3-1": "Address of the subject",
    "3-2": "Default : Multiselect option to choose the address of the subject. Nested options appear if multiple levels of address are present. e.g. District -> Taluka -> Village.",
    "4-0": "Registration Date",
    "4-1": "Date of Registration of the subject",
    "4-2": "Default : Fixed date  \nRange : Options to choose Start date and End date",
    "5-0": "Enrolment Date",
    "5-1": "Date of Enrolment in any program",
    "5-2": "Default : Fixed date  \nRange : Options to choose Start date and End date",
    "6-0": "Encounter Date",
    "6-1": "Date of Encounter in any Encounter",
    "6-2": "Default : Fixed date  \nRange : Options to choose Start date and End date",
    "7-0": "Program Encounter Date",
    "7-1": "Date of Program Encounter in any Program Encounter",
    "7-2": "Default : Fixed date  \nRange : Options to choose Start date and End date",
    "8-0": "Search All",
    "8-1": "Text fields in all the core fields and observations in Registration and Program enrolment",
    "8-2": "Default : Text Field"
  },
  "cols": 3,
  "rows": 9,
  "align": [
    "left",
    "left",
    "left"
  ]
}
[/block]


#### Limitation: Right now we cannot have multiple scopes for a filter, i.e. we cannot search a concept in program encounter and encounter with the same filter.

# Users need to sync the app for getting any of the above changes.
