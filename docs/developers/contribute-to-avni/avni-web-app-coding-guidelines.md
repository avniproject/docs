---
title: "Avni Web App Coding Guidelines"
slug: "avni-web-app-coding-guidelines"
excerpt: ""
hidden: false
createdAt: "Wed Jan 25 2023 07:19:25 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
(not a complete doc yet)

In functional components try to avoid (**this is not a strict requirement**) creating functions in the body, as these functions get redefined with every state change. There are the following options:

- Use _useCallback_ to define memoized functions (note that even these get redefined based on the state change)
- define the function outside the functional component in the same file and pass all the required parameters which may be too many
- create class type component
