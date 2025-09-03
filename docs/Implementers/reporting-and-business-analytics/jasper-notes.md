---
title: "Jasper notes"
slug: "jasper-notes"
excerpt: ""
hidden: false
createdAt: "Wed Nov 27 2024 04:36:12 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Wed Nov 27 2024 04:45:53 GMT+0000 (Coordinated Universal Time)"
---
### Self referential hierarchical reports

1. The contents of JRXML can be manipulated based on the url parameters. The url parameters can be coming from the same report at a higher level.
2. Each report can have filters specific to that level, which cannot be dynamically changed. So this is a blocker.

### Creating new version

This is to avoid changing the production version as it is already in use.

1. Copy can be created using export.
2. All the files are text files so these can be changed in editor and then imported after zipping.
