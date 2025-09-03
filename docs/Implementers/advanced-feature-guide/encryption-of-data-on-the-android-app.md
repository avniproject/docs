---
title: "Encryption of data on the Android app"
slug: "encryption-of-data-on-the-android-app"
excerpt: ""
hidden: false
createdAt: "Wed Aug 09 2023 11:42:35 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
Some implementations require a higher level of security, which includes encryption of the database on Android. 

### How to enable encryption:

To have all the users field app database encrypted, the option for encryption need to be enabled under `Organisation Details`  as shown in the image below. Users would be in need to sync the app, to reflect the encryption setting change.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e132e70-Screenshot_2023-08-14_at_4.24.22_PM.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]


### Side-effects of using the feature:

- As shown in the warning message in the image above, enabling this feature will not permit the user to use [fast sync](https://avni.readme.io/docs/fast-sync) and upload db feature from the Menu options on the field app.
- After the option is enabled, it can be disabled anytime on change of mind. 

### Developer debug notes:

- To see the data of encrypted realm db, print out the commented out line that calculates `hexEncodedKey` in the `EncryptionService`. And use the printed value to open the realm db when it asks for the encryption key as shown in the image below.

[block:image]
{
  "images": [
    {
      "image": [
        "https://files.readme.io/e79ad32-Screenshot_2023-08-09_at_4.41.56_PM.png",
        "",
        ""
      ],
      "align": "center"
    }
  ]
}
[/block]
