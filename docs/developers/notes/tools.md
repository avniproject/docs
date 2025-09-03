---
title: "Auto setup nvm"
slug: "tools"
excerpt: ""
hidden: false
createdAt: "Fri Nov 18 2022 04:48:55 GMT+0000 (Coordinated Universal Time)"
updatedAt: "Mon Dec 11 2023 12:04:24 GMT+0000 (Coordinated Universal Time)"
---
### nvm

Since we use nvm and our different projects/branches use a different version of node. In order to always use the correct version of the node we have two tools. These set the node version and the default node version. The default node version must be set if one uses the avni client to do react-native run-android, which internally launches the packager or metro bundler. Each project has a .nvmrc file checked in specifying the node version.

- A customized cd command that sets the node version and default node version. You can put this in our bashrc or bash profile files. See the function below.
- When we are in a particular directory and switch the git branch the node version may need to change. To support this we have git checkout hooks.

```Text shell
function cd () {
  builtin cd "$@"  
  if \[[ -f .nvmrc ]]  
  then  
    nvm use > /dev/null  
    nvm alias default current > /dev/null  
  fi  
}
```
