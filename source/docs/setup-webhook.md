---
title: Setup a webhook for your app on Bitrise
---

# What is a WebHook?

Most source code hosting service provides a feature to register WebHooks.
A WebHook is basically an URL which will be called on specified events.

To have Bitrise automatically start a Build every time you push
code into your repository you can set up a webhook at your code hosting service
which will automatically trigger a build on Bitrise with the code
you push to your repository.


# Setup a webhook for your app on Bitrise

This tutorial helps you to setup a webhook for your app on Bitrise.

> If you select Github or Bitbucket as the source code provider
> when you add your app Bitrise automatically sets up a webhook for it.
> In this case, you can skip this tutorial.

If you use the **set up your repository manually** option
on the *add new app* page, you need to set up
the webhook yourself (even if it is a Github or Bitbucket repository).

You can learn all about it in this tutorial, just follow these steps in order:

1. Add a new app with manually specified repository on Bitrise
2. Get the webhook URL from Bitrise
3. Add the webhook URL to your repository on your source code provider's website


## 1. Add a new app with manually specified repository on Bitrise

To add a new app on Bitrise, select **Add new app** on the Bitrise Dashboard, or [click here](https://www.bitrise.io/apps/add){:target="_blank"}.

In the first step, you need to select the source code provider of your app. For the purposes of this tutorial, select **Click here to set up your repository manually**, then copy and paste your GIT repository URL. For public repositories, use HTTPS URL, for private repositories use SSH URL. Next, select how Bitrise will be able to access the source code, and follow the instructions.

After the validation of your repository is finished, the app is connected to Bitrise.

## 2. Get the webhook URL from Bitrise

To get the webhook URL from Bitrise, select your app on the Bitrise Dashboard and select the *Settings* tab, where you can find your build trigger URL.

## 3. Add the webhook URL to your repository on your source code provider's website

### GitHub

If your source code provider is Github visit the [Github website](https://github.com){:target="_blank"}, select your repository, then go to *Settings*. Next, select *Webhooks & Services* and click *Add webhook*. Paste your webhook URL in the field *Payload URL*. Select *application/x-www-form-urlencoded* as the content type. You can leave the secret field blank. After you finished, click on *Add webhook*.

### Bitbucket

If your source code provider is Bitbucket visit the [Bitbucket website](https://bitbucket.org){:target="_blank"}, select your repository, then go to the repository settings. Under *Integrations*, select *Webhooks*, then click the *Add webhook* button. Paste your webhook URL in the field, add a title and make sure the "Repository push" is set as a trigger. Currently Bitrise only supports the default Push trigger. When done select *Save*.

### Other source code hosting services

If you use another source code provider you can use our Build Trigger API to trigger builds on Bitrise. For more information about using the Bitrise Build Trigger API, [click here](http://devcenter.bitrise.io/docs/api/build-trigger-api.html).
