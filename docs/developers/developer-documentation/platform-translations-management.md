---
title: "Platform translations management"
slug: "platform-translations-management"
excerpt: ""
hidden: false
createdAt: "Mon Oct 31 2022 12:55:27 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
The management of translations of the Avni platform that are not implementation specific has been described here.

Translations can be for the web app or mobile app. These translation files are maintained in the avni-webapp and avni-client repositories respectively.

Each of these repositories provides makefile targets that can be used to deploy the translations. Deployment of translations brings the source code in sync with the deployment. Production deployments are done during the release or if there is a patch release of translations. Staging deployment can be done as part of the story development as well.

### Caveat

Although the source code contains translations in all languages, only English is maintained here. The missing platform translations are also uploaded as part of the implementation. This is the current state of affairs but is currently under discussion as to what is the right way forward. **So currently only English translations need to be created and uploaded.**
