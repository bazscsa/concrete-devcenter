---
title: Virtual Machines and Base Box updates
---

# Base Box

The Base Box is a virtual machine image we use for running your builds.
Every build runs in its own virtual machine and the virtual machine is
rolled back to a saved state (the base box state) after the build finishes.

This way **your builds are always protected** by changes made by others and
by your previous builds and you can use a **stable environment** to
define your build workflow (*no state persists between builds*).

The user which is used for the builds is configured with **passwordless sudo** enabled,
this way **you can install all the extra things you need for your builds**
and for other automation.

**This is a guideline, not a rule documentation.**
If you need older versions of a program or you know about a useful tool
which would be beneficial for everyone to be
pre-installed [let us know](https://www.bitrise.io/contact){:target="_blank"}!


## Pre-installed component versions

The current Box OS X version is: **10.10.4 (Yosemite)**

Our current Base Box contains the following programs preinstalled:

* [Homebrew](http://brew.sh/){:target="_blank"}: `0.9.5`
* installed with Homebrew:
    * __coreutils__: `8.24` - installed with Homebrew, this means that all the tools are prefixed with the letter __g__. For example `timeout` is available as `gtimeout`.
    * __git__: `2.4.5`
    * __mercurial__: `3.4.2`
    * __xctool__: `0.2.4`
    * __go__: `1.4.2`
    * __NodeJS__: `v0.12.7`
    * __NPM__: `2.12.1`
    * __wget__: `1.16.3`
    * [ansible](http://www.ansible.com/home){:target="_blank"}: `1.9.2`
* __Xcode__:
    * __-stable__: `6.4 (build version: 6E35b)`
    * __-beta__: `7.0 beta 3 (build version: 7A152u)`
* [RVM](http://rvm.io/){:target="_blank"}: `1.26.11`
* __Rubies__ (installed with RVM)
    * `2.1.6`
    * `2.2.2`
    * `2.1.5 (p273)`, set as **default**
* __Ruby Gems__, *installed for the default Ruby version*
    * [CocoaPods](http://cocoapods.org/){:target="_blank"}: `0.37.2`
    * [nomad-cli](http://nomad-cli.com/){:target="_blank"}: `2.4.8`
    * [bundler](http://bundler.io/){:target="_blank"}: `1.10.5`
* [XcodeUnitTestMiniserver](https://github.com/bitrise-io/xcodebuild-unittest-miniserver){:target="_blank"}: `1.2.0`
* [cmd-bridge](https://github.com/bitrise-io/cmd-bridge){:target="_blank"}: `v0.9.2` installed and auto-started in server mode (with LaunchAgent)

You can find the **Virtual Machine changelog** [here](/docs/vm-box-changelog.html).

> You can find the OS X base box setup guide and automation scripts
> we use for building our OS X virtual machine base box
> in our [OS X Box Bootstrap repository](https://github.com/bitrise-io/osx-box-bootstrap){:target="_blank"},
> so you can build your own virtual machine to match the ones used on Bitrise.

*We have a special Step which reports all the installed program / component versions.
Just add the **OS X System Information Reporter** step
to your app's workflow (or you can create a separate app on Bitrise
for this purpose), run a build and check this step's output.*


## Xcode version support guideline

We have the latest stable version of Xcode pre-installed in the OS X Virtual Machines and also the the latest beta version of Xcode.

When a new major version of Xcode gets released we keep supporting the previous major version until the first significant patch version of Xcode.

As an example in case of Xcode major version 6: Xcode 6 is the major version and the first significant patch is Xcode 6.1. We kept the latest Xcode 5 installed on the Virtual Machines until Xcode 6.1 was released.


### iOS Simulator version & SDKs support

All the iOS Simulator versions which can be installed
through *Xcode -> Preferences -> Downloads* are installed and available.

### xctool support

[xctool](https://github.com/facebook/xctool){:target="_blank"} is installed through [homebrew](http://brew.sh/){:target="_blank"} and so if you need to update it
to be sure you have the latest version you can add a [Bash Script Step](https://github.com/bitrise-io/steps-bash-script){:target="_blank"}
with the content:

    #!/bin/bash
    brew update && brew upgrade xctool

*If you need the latest xctool version compiled from source
you can do it by adding a **Bash Script Runner** step
to your workflow, right before your first Xcode build, analyze, unit test or archive step, with the following content:*

    #!/bin/bash
    brew update && brew uninstall xctool && brew install xctool --build-from-source

### Technical notes

We install our Xcodes into a /Applications/Xcodes folder, postfixed with
a stability flag.

* The latest stable Xcode version is available at: `/Applications/Xcodes/Xcode-stable.app`
* The latest beta Xcode version is available at: `/Applications/Xcodes/Xcode-beta.app`

*The default Xcode version is always the latest stable version
installed in the Virtual Machine, you can specify a different version
for Xcode builder steps, for example to use the latest beta
you should specify `-beta` at the Step's related input*

### List preinstalled Xcodes and get version information

If you want to list all the preinstalled Xcode versions you can drop
a [Bash Script Step](https://github.com/bitrise-io/steps-bash-script) into your
workflow with [this content](https://github.com/bitrise-io/bitrise-script-collection/blob/master/bash/list_available_xcodes_and_sdks.sh){:target="_blank"}.

*This will find all the Xcode apps in the /Applications/Xcodes folder,
activate each by calling xcode-select and print the version of Xcode
and all the SDKs (and Simulators) available for the version.*


## Virtual Machine update scheduled

We update our OS X Virtual Machines at about every seconds week in the following manner:

* At the beginning of the week (mostly on Monday) we prepare the new Virtual Machines which will contain the latest stable Xcode version and the latest beta version too. We announce the pre-installed tool version changes on our [blog](http://blog.bitrise.io/){:target="_blank"} and also update this page once we know the final list.
* During the week we test the new Virtual Machine internally to ensure it's stable enough for the release.
* At the end of the week we release the new Virtual Machines into our production environment. We do this on the weekends, preferably on Saturday.

The box update includes the latest updates for the listed programs and for the OS
and is usually performed during the weekend to not to interfere
with your everyday business.

Updates are always announced on our [blog](http://blog.bitrise.io/){:target="_blank"}
and can be seen on [your Bitrise Dashboard](https://www.bitrise.io/dashboard){:target="_blank"} and we also send you
a *Platform Update email* about significant changes unless you disable it on
your [Account Settings](https://www.bitrise.io/me/profile){:target="_blank"} page.


### Minor updates

Additional smaller box patches might be applied during the week
in case we detect an issue with the current virtual machine environment.

These patches do not change any pre-installed tool's version,
unless it's really necessary.


## Previous and upcoming updates

Please see our [Virtual Machine changelog](/docs/vm-box-changelog.html)
for more information on past and planned updates.



> If you need older versions of a program or you know about a useful tool
> which would be beneficial for everyone to be
> pre-installed [let us know](https://www.bitrise.io/contact){:target="_blank"}!
