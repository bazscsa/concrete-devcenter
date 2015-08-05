![Fastlane](images/fastlane-tools-integration/fastlane_logo.png "Fastlane")

Having more time to be creative is the key to great inventions. We believe that giving developers the chance to work without distractions is the most important thing that can lead to extraordinary creations.
Our mission is to provide a platform that lets you concentrate on the process of creation, instead of the administrative tasks that get in the way of it.

That’s why we created Bitrise. But we’re not alone in this. We love how [Felix Krause](https://krausefx.com) sought to solve this problem by creating [fastlane](https://fastlane.tools). So by the combined force of earth, water, fire and wind… we integrated the whole [fastlane toolkit](https://fastlane.tools)  - booyah! How cool is that!

![Captain Planet](images/fastlane-tools-integration/captain_planet.gif "Captain Planet")

## What is fastlane?
`Fastlane` lets you define and run your deployment pipelines for different environments. It helps you unify and automate your app’s release process. `Fastlane` connects all `fastlane tools` and third party tools, like CocoaPods and xctool.

`Fastlane` is a collection of ruby scripts that covers the most usual tasks required when submitting a new iOS app or update to the App Store:

* **deliver** uploads screenshots, metadata and your app to the App Store
* **snapshot** automates taking localized screenshots of your iOS app on every device 
* **frameit** quickly puts your screenshots into the right device frames 
* **PEM** automatically generates and renew your push notification profiles 
* **sigh** automatically generates and manages your provisioning profiles
* **produce** creates new iOS apps on iTunes Connect and Developer Portal
* **cert** automatically creates and maintain iOS code signing certificates 
* **codes** creates promo codes for iOS Apps using the command line 

## How to get started?
Using `fastlane` for your workflow is easy as pie. You just have to add two steps to your workflow.

![Bitrise Worflow](images/fastlane-tools-integration/fastlane_workflow.png "Bitrise Worflow")

You need the `Certificate and profile installer` to download your `Certificate` and `Provisioning Profiles` and to install them.

With adding the `fastlane` step we ensure that you are running on the latest `fastlane` version. Inside the step you can set the `fastlane` action and we will run it automatically every time you push a new code change.

## What’s next?
`Fastlane’s` greatness comes from its ability to define different lanes for your different deployment needs - hence the name. You can combine this with Bitrise and run separate lanes for separate branches, automatically. For example you can run a lane for every code push onto the `master` branch to update your screenshots and metadata on the App Store and to release the distribution version, and a separate lane for the `develop` branch to deploy your test releases and all the others to ensure that nobody has broken anything.

We hope that you are as happy as we are to have this amazing tool inside Bitrise. Go ahead and try it out!

And as always, happy building!
