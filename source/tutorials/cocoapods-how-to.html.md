---
title: How to handle different CocoaPods versions
---

# Using different CocoaPods versions in different projects

By default the [CocoaPods](https://cocoapods.org) is a system gem but if you need to use a specific version of it the best way to go is using [Bundler](http://bundler.io/). Just follow these steps to configure the [CocoaPods](https://cocoapods.org) version to be used:

Create a Gemfile in your project's directory where you keep your Podfile. The Gemfile should include the [CocoaPods](https://cocoapods.org) version to use (the example shows how to use version 0.38.0)

	source 'https://rubygems.org'
	gem 'cocoapods', '0.38.0'

 When done simply run the following commands in the terminal:

    gem install bundler
    bundle install
    bundle exec pod install

As you can see simply by adding the `bundle exec` to your command you can use [Bundler](http://bundler.io/) to use the [CocoaPods](https://cocoapods.org) version that is specified in the Gemfile and is installed by the `bundle install` command and it executes the specified `pod install` line using this version.

# Using different Cocoapods versions on Bitrise

The Virtual Machines that [Bitrise](https://bitrise.io) uses have [Bundler](http://bundler.io/) installed already and the Run CocoaPods install step [https://github.com/bitrise-io/steps-cocoapods-and-repository-validator](https://github.com/bitrise-io/steps-cocoapods-and-repository-validator) also checks for a Gemfile so there are only two simple steps to follow if you don't want to use the latest version of [CocoaPods](https://cocoapods.org) for your project

1. Add the Gemfile to your repository where you keep your Podfile and make sure to stage, commit and push it
2. Add the [Run CocoaPods install](https://github.com/bitrise-io/steps-cocoapods-and-repository-validator) step to your workflow
+ The [Run CocoaPods install](https://github.com/bitrise-io/steps-cocoapods-and-repository-validator) step has an option *Update CocoaPods version?* that updates the system version of [CocoaPods](https://cocoapods.org). Since you are using a different version and you don't need the latest simply change this value to false