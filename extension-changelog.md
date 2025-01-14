---
description: Changelog for the Visual Studio Code extension for PowerShell Universal.
---

# Extension Changelog

## 1.7.2 - 12/30/2020

**Added**

* Settings for controlling the sample browser

**Changed**

* Improved the error message returned when attempting to automatically grant an app token and it fails. 

## 1.7.1 - 12/29/2020

#### Added

* Added a Sample Browser for inserting samples from the PowerShell Universal Samples Repository

## 1.7.0 - 12/28/2020

{% hint style="warning" %}
Breaking Change: This version of the extension only works with version 1.5.0 or later of PowerShell Universal 
{% endhint %}

**Added**

* Added a version check for notification there is a new version of Universal
* Added a URL setting for connecting to PowerShell Universal
* Added new connection workflow to make it easier and more clear on how to connect to Universal.

**Changed**

* The extension now uses the REST API to make changes to configuration scripts
* Deprecated the Port and Computer name settings in favor of the URL setting
* The extension no longer automatically downloads PowerShell Universal

## \[1.6.1\]

#### Changed

* Fixed issue when attempting to download on Windows or Mac
* Fixed issue where extension would not work with Mac OS X

## \[1.6.0\]

#### Added

* Added support for Debug-PSUDashboard

#### Changed

* Replaced PowerShell Versions with Environments in the configuration tree view

## \[1.5.1\]

#### Changed

* Fixed an issue where the extension wouldn't activate correctly.

## \[1.5.0\]

#### Added

* Add a command for manually refreshing the PSU configuration

#### Changed

* Fixed an issue where components wouldn't import correctly

## \[1.4.0\]

#### Added

* Added a setting to disable starting the PowerShell Universal server on extension activation.

#### Changed

* Extension will fail to activate after a number of retries while connecting to the Universal server.

## \[1.3.0\]

* Added support configuration files. 

## \[1.2.0\]

* Added support for scripts and jobs.

## \[1.1.0\]

* Added support for APIs

## \[1.0.0\]

* Initial release

