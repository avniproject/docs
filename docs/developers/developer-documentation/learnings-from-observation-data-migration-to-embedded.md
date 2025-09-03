---
title: "Learnings from observation data migration to embedded"
slug: "learnings-from-observation-data-migration-to-embedded"
excerpt: ""
hidden: true
createdAt: "Thu Mar 21 2024 05:50:41 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Thu Mar 21 2024 07:32:44 GMT+0000 (Coordinated Universal Time)"
---
- Migrating observations is like migrating (reading and writing) 90% of mobile database
- Large migrations take up memory and likely to go out of memory for medium to large sized data
- There is no flush functionality like hibernate, so keep memory under control one can perform commit and re-open transaction. this pushes data to the file system from memory.
- <https://gist.github.com/petmongrels/354a54ed1d0c3f492688d61c2dd63e55>
- removed code available here 
  - <https://github.com/avniproject/avni-models/blob/66f582a25831db424447205ec778c6e78588d797/src/Schema.js>
  - <https://github.com/avniproject/avni-models/blob/180550ab1d0fff8d145813ae8a466107505f8e46/test/SchemaTest.js>
