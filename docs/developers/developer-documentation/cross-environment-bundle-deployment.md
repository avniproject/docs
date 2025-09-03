---
title: "Cross Environment Bundle Deployment"
slug: "cross-environment-bundle-deployment"
excerpt: ""
hidden: true
createdAt: "Wed Jan 31 2024 08:16:32 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Wed Jan 31 2024 10:31:19 GMT+0000 (Coordinated Universal Time)"
---
- Ensure that both the environments have the same build number deployed.
- In the bundle there may be use of S3 files like icons in Subject Type
  - Do find in files for such data and remove it.
  - Manually upload the assets from the application screen (app designer, edit subject type in this case)
- There is bug in platform related to bundle upload/download for GroupPrivilege.
