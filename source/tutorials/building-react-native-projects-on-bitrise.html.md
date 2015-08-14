---
title: Building React Native projects on Bitrise
---
# Building React Native projects on Bitrise

This tutorial shows you how to setup [React Native](https://facebook.github.io/react-native/) on [Bitrise](http://bitrise.io/).


React Native recommends to install [iojs](https://iojs.org/en/index.html), [watchman](https://github.com/facebook/watchman), and [flow](http://flowtype.org/).

These frameworks are not required to build a [React Native](https://facebook.github.io/react-native/) project, so if you don't use them, you can skip this part.
Add the [Bash Script Runner](https://github.com/bitrise-io/steps-bash-script) step to your workflow.

    #!/bin/bash
    brew unlink node
    brew uninstall node
    brew install iojs
    brew install --HEAD watchman
    brew install flow

In order to build a [React Native](https://facebook.github.io/react-native/) app you have to install [React Native](https://facebook.github.io/react-native/) with npm. [Node](https://nodejs.org/) is already installed on our VMs, so you don't have to do it manually.
Add the [Bash Script Runner](https://github.com/bitrise-io/steps-bash-script) step to your workflow. Make sure you cd into your project's directory before running the npm install like in the following code:

    #!/bin/bash
    cd "./projectDir"
    npm install react-native

After running this script you can run every Xcode related step just like if it would be a plain old Xcode project.
