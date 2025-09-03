---
title: "Extensions"
slug: "extension-points"
excerpt: ""
hidden: false
createdAt: "Thu Oct 24 2019 09:25:29 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
Extensions are points in Avni where custom html can be used to enhance functionality. There are a few such predefined points where custom html can be inserted. 

In Data Entry App

- Subject Dashboard
- Subject Dashboard for a specific program
- Search Results page

In the Field-App

- Splash Screen

## Creating Extensions

### Creating the extension

In order to create an extension, first you need to create a web app. For each extension point, there will be parameters that you will receive that can be used for custom behaviour. Data can be fetched from the database using the Avni API.

Parameters

- Subject Dashboard - subjectUUIDs (subject's uuid), token (auth token)
- Search Results page - subjectUUIDs (Comma separated list of subjects that have been selected), token
- Splash screen - nothing

The token field must be added as a header AUTH-TOKEN in case you need to use the public API to interact with the Avni server.

### Adding the extension on the App Designer

Extensions can now be added to Avni through the app designer (<https://app.avniproject.org/#/appdesigner/extensions>).  
All your extensions must be zipped and uploaded on this screen. You can enter the name of the extension, the file name in the zip file that must be rendered (use relative paths if your HTML file is within a directory), and the type of extension (called Extension Scope). 

![](https://files.readme.io/e772f7d-Screenshot_2021-10-27_at_10.58.02_AM.png "Screenshot 2021-10-27 at 10.58.02 AM.png")
