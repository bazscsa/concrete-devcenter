---
title: Virtual Machines / Box change log
---

# Virtual Machines / Box #changelog


## Sep 5, 2015

* installed with Homebrew:
    * __git__: `2.5.0` -> `2.5.1`
    * __xctool__: `0.2.4` -> `0.2.5`
    * __go__: `1.4.2` -> `1.5`
* __Xcode__:
    * __-beta__: `7.0 beta 5 (build version: 7A176x)` -> `7.0 beta 6 (build version: 7A192o)`
* [bitrise CLI](https://github.com/bitrise-io/bitrise){:target="_blank"}: **new**, `0.9.11`
* [bitrise-bridge](https://github.com/bitrise-io/bitrise-bridge){:target="_blank"}: **new**, `0.9.1`


## Aug 15, 2015

* installed with Homebrew:
    * __mercurial__: `3.4.2` -> `3.5`
* __Xcode__:
    * __-beta__: `7.0 beta 4 (build version: 7A165t)` -> `7.0 beta 5 (build version: 7A176x)`


## Aug 1, 2015

* installed with Homebrew:
    * __git__: `2.4.5` -> `2.5.0`
* __Xcode__:
    * __-beta__: `7.0 beta 3 (build version: 7A152u)` -> `7.0 beta 4 (build version: 7A165t)`
* __Ruby Gems__, *installed for the default Ruby version*
    * [CocoaPods](http://cocoapods.org/){:target="_blank"}: `0.37.2` -> `0.38.2`
    * [bundler](http://bundler.io/){:target="_blank"}: `1.10.5` -> `1.10.6`
* [XcodeUnitTestMiniserver](https://github.com/bitrise-io/xcodebuild-unittest-miniserver){:target="_blank"}: __REMOVED__


## July 18, 2015

* installed with Homebrew:
    * __coreutils__: `8.23` -> `8.24`
    * __NodeJS__: `v0.12.5` -> `v0.12.7`
    * __NPM__: `2.11.2` -> `2.12.1`
* __Xcode__:
    * __-stable__: `6.4 (build version: 6E35b)` (no change)
    * __-beta__: `7.0 beta2 (build version: 7A121l)` -> `7.0 beta3 (build version: 7A152u)`

## July 11, 2015

* OS X: `10.10.3` -> `10.10.4`
* installed with Homebrew:
    * __git__: `2.4.3` -> `2.4.5`
    * __mercurial__: `3.4.1` -> `3.4.2`
    * __xctool__: `0.2.3` -> `0.2.4`
    * __NodeJS__: `v0.12.4` -> `v0.12.5`
    * __NPM__: `2.10.1` -> `2.11.2`
    * [ansible](http://www.ansible.com/home){:target="_blank"}: `1.9.1` -> `1.9.2`
* __Xcode__:
    * __-stable__: `6.3.2 (build version: 6D2105)` -> `6.4 (build version: 6E35b)`
    * __-beta__: `7.0 beta2 (build version: 7A121l)`
* __Ruby Gems__, *installed for the default Ruby version*
    * [bundler](http://bundler.io/){:target="_blank"}: `1.10.3` -> `1.10.5`


## June 13, 2015

* coreutils: **new**, `8.23`, installed with [Homebrew](http://brew.sh/){:target="_blank"}, this means that all the tools are prefixed with the letter `g`. For example `timeout` is available as `gtimeout`.
* git: `2.3.6` -> `2.4.3`
* mercurial: `3.3.3` -> `3.4.1`
* NodeJS: `v0.12.2` -> `v0.12.4`
* NPM: `2.7.5` -> `2.10.1`
* [ansible](http://www.ansible.com/home){:target="_blank"}: `1.9.0.1` -> `1.9.1`
* Xcode:
  * -stable: `6.3.1 (6D1002)` -> `6.3.2 (6D2105)`
  * -beta: no beta Xcode installed
* Ruby Gems, *installed for the default Ruby version*
  * [CocoaPods](http://cocoapods.org/){:target="_blank"}: `0.37.0` -> `0.37.2`
  * [nomad-cli](http://nomad-cli.com/){:target="_blank"}: `2.4.6` -> `2.4.8`
  * [bundler](http://bundler.io/){:target="_blank"}: `1.10.3`


## May 4, 2015

* [CocoaPods](http://cocoapods.org/){:target="_blank"}: 0.36.4 - installed for the default Ruby version -> 0.37.0


## May 2, 2015

* git: 2.3.5 -> 2.3.6
* Xcode:
  * -stable: 6.3 -> 6.3.1 (6D1002)
  * -beta: no beta Xcode installed
* Rubies installed with RVM
  * 2.1.6
  * 2.2.2
  * 2.1.5 (p273), set as default
  * [CocoaPods](http://cocoapods.org/){:target="_blank"}: 0.36.3 - pre-installed for the default Ruby version -> 0.36.4
  * bundler installed for the default Ruby version
* [cmd-bridge](https://github.com/bitrise-io/cmd-bridge){:target="_blank"}: **new**, v0.9.2 installed and auto-started in server mode (with LaunchAgent)


## April 18, 2015

* Will include the **final version of Xcode 6.3** (6D570)
* Xcode 6.2 and Xcode 6.3 beta 4 **will be removed**.
* OS X: 10.10.2 -> 10.10.3
* mercurial: 3.3.2 -> 3.3.3
* NPM: 2.7.4 -> 2.7.5


## April 4, 2015

* git: 2.3.3 -> 2.3.5
* NodeJS: v0.12.0 -> v0.12.2
* NPM: 2.5.1 -> 2.7.4
* [ansible](http://www.ansible.com/home){:target="_blank"}: 1.8.4 -> 1.9.0.1
* Xcode:
  * -beta: 6.3 beta 3 (6D543q) -> beta 4 (6D554n)
* [RVM](http://rvm.io/){:target="_blank"}: 1.26.10 -> 1.26.11
  * Ruby 2.1.5p273 installed with RVM, 2.1.5 is set as default
  * [CocoaPods](http://cocoapods.org/){:target="_blank"}: 0.36.0 -> 0.36.3 *// pre-installed for the default Ruby version*


## March 21, 2015

* Xcode 6.3 beta 2 (Build version 6D532l) -> Xcode 6.3 beta 3 (Build version 6D543q)
* git: 2.3.2 -> 2.3.3
* *Platform note*: we'll increase the RAM of the virtual machines from 3GB to 4GB


## March 14, 2015

* Xcode 6.1.1 -> Xcode 6.2 (6C131e)
* mercurial: 3.3 -> 3.3.2
* wget: 1.16.2 -> 1.16.3
* CocoaPods: 0.35.0 -> 0.36.0


## March 10, 2015

* git: 2.3.1 -> 2.3.2
* xctool: 0.2.2 -> 0.2.3


## March 7, 2015

* OS X: 10.10.1 -> 10.10.2
* Xcode naming change: instead of storing Xcodes with the version number included in the Xcode app's name we'll use a couple of state indicators:
  * Xcode-stable.app : latest stable release (6.1.1)
  * Xcode-beta.app : latest beta release (6.3b2)
* xctool: 0.2.1 -> 0.2.2
* git: 2.2.0 -> 2.3.1
* mercurial: 3.2.1 -> 3.3
* go: 1.3.3 -> 1.4.2
* NodeJS: 0.10.33 -> v0.12.0
* NPM: 2.1.10 -> 2.5.1
* wget: 1.16 -> 1.16.2
* ansible: 1.8.1 -> 1.8.4
* nomad-cli: 2.4.3 -> 2.4.6
* RVM: 1.26.3 -> 1.26.10
* Ruby: 2.1.5 installed with RVM, 2.1.5 is set as default
* XcodeUnitTestMiniserver: 1.1.1 -> 1.2.0


## Dec. 13, 2014

* [Homebrew](http://brew.sh/){:target="_blank"}: 0.9.5
* git: 2.2.0
* mercurial: 3.2.1
* xctool: 0.2.1
* go: 1.3.3
* NodeJS: 0.10.33
* NPM: 2.1.10
* wget: 1.16
* [ansible](http://www.ansible.com/home){:target="_blank"}: 1.8.1
* [nomad-cli](http://nomad-cli.com/){:target="_blank"}: 2.4.3
* Xcode: 6.1.1 (Build version 6A2008a)
* [RVM](http://rvm.io/){:target="_blank"}: 1.26.3
  * Ruby 2.1.2, 2.1.3, 2.1.4, 2.1.5 installed, 2.1.5 is set as default
  * [CocoaPods](http://cocoapods.org/){:target="_blank"}: 0.35.0 - pre-installed for the default Ruby version
* [XcodeUnitTestMiniserver](https://github.com/bitrise-io/xcodebuild-unittest-miniserver){:target="_blank"}: 1.1.1
