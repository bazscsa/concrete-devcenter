---
title: Appium Automated UI Test
---

# Appium Automated UI Test

You can run Your [Appium](http://appium.io/) automated UI tests during
your build and send the screenshots from your test to given email addresses.

Your tests should expect 





You can for example send a HipChat message with the result of
your Xcode archive, or with the [TestFlight](https://testflightapp.com/)
deploy's URL.

To do this all you have to do is add a **HipChat Message** step to
your app's Workflow, fill out the required inputs (authentication token,
the room's ID you want to send the message to, color of the message, ...)

In the *Message* input field you can include environment variables
defined by Bitrise or by the steps which run before the HipChat Message step.

> You can find an **Insert Variable** button under every input field.
> With this you can insert environment variables defined by Bitrise
> (for example the App's title, the Build's unique ID or the Build's
> URL on Bitrise) and environment variables exported by Steps
> which will run before this step (for example an Xcode Build's
> status or the generated IPA path).

To include the build's url (where you can see the details of the build),
the Xcode Archive step's result and the TestFlight deploy's URL
do the following:

*Make sure your workflow contains the following steps, in this order:*

1. Git Clone Repository (to clone your app's code)
2. Run CocoaPods (if you use CocoaPods)
3. Create Archive
4. Deploy: TestFlight
5. HipChat Message

Fill out the TestFlight and the HipChat steps' required input fields
and for the HipChat Message step's *Message* input you can include
the build's url with the *BITRISE_BUILD_URL* environment variable,
and the TestFlight deploy's install url with the *TESTFLIGHT_DEPLOY_INSTALL_URL*
environment variable.

An example *Message* input:

    Your build's details can be found at: ${BITRISE_BUILD_URL},
    and the TestFlight install url is: ${TESTFLIGHT_DEPLOY_INSTALL_URL}

That's all. Once you configure your Workflow this way you'll
get automatic TestFlight deploys for every successful build
of your app and you'll be notified about the build and
deploy through a HipChat message containing both the build's details
url and the TestFlight install url.
