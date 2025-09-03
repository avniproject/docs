---
title: "Install Avni"
slug: "environment-setup-guides"
excerpt: "This section explains how to install Avni on local machine, test environment or for Production environment."
hidden: false
createdAt: "Wed Jan 01 2020 04:02:45 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
Avni is required to be set up for various purposes - full-stack product developer, front end developer, testers and production users. Avni can be set up on - mac, windows, ubuntu and centos. Overtime Avni will incrementally provide setup documentation for all these combinations, but currently, the following documentation is available, based on most frequent need seen by us.

### Deployment Diagram

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/7fb05b2-Avni_2.png",
        "Avni (2).png",
        1038
      ],
      "align": "center",
      "caption": "Avni technical components"
    }
  ]
}
[/block]


Avni is composed of multiple components connected to each other. Following are a few important points about the deployment diagram.

- Any data analytics solution can be used with Avni, by connecting directly with the database. We have used Metabase and Jasper Reports so far.
- Avni currently uses AWS Cognito service where the users are stored. The management of users happens via the Avni Web Application.
- Avni is developed using ReactNative hence easily portable to iOS app, but currently there is no iOS build generated.
- AWS S3 is required only if you are capturing photos and videos from the field-app or data entry web-app. Avni will work, without errors, if you do not use them.

<hr/>
<br/>

# Local Development Environment Setup (for Avni Product)

[Environment setup for product development - Ubuntu](doc:developer-environment-setup-ubuntu)  
[Environment setup for front end product development - Ubuntu](doc:environment-setup-for-front-end-product-development-ubuntu)

# Production/Test Environment Setup

[Test and production environment setup - CentOS](doc:test-and-production-environment-setup-centos)

# Build information

[Build numbers](doc:build-numbers)

<br/>
