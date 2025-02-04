---
description: Changelog for PowerShell Universal.
---

# Changelog

## 1.5.8 - 12/27/2020

{% hint style="warning" %}
Known Issue: The Universal PowerShell module included with 1.5.8 is 1.5.7 and will show a warning when running against the 1.5.8 server. This can be safely ignored.
{% endhint %}

* UniversalDashboard - v3.2.5
* UniversalDashboard - v2.9.9
* UniversalDashboard.Charts - 1.3.2
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Changed

#### Dashboard

* UDv3 - Fixed an issue with New-UDTable and PSCustomObject. 
* UniversalDashboard.Charts - Added MinValue and MaxValue to New-UDNivoChart -Calendar

## 1.5.7 - 12/18/2020

{% hint style="info" %}
Note that although it is listed that the MSI upgrade will not reset the service account, this will not actually take effect until the next version. 
{% endhint %}

* UniversalDashboard - v3.2.4
* UniversalDashboard - v2.9.9
* UniversalDashboard.Charts - 1.3.1
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Changed

#### Automation

* Fixed an issue where clicking the run button on the second page of scripts would execute the wrong script

#### Dashboard

* Fixed an issue where you would have to delete a dashboard twice to get it to delete
* Fixed an issue where adding a dashboard in the UI would enable auto-start even when it wasn't on
* UDv3 - Fixed an issue with blank pages. 
* UDv3 - Fixed an issue where New-UDTable would return an error when it only had 1 row. 

#### Platform

* Fixed an issue where authorization policies would run on every request when using Windows Auth outside of IIS.
* Fixed an issue where the Universal PowerShell module would show a warning when running in Windows PowerShell
* Fixed an issue where alternate security environments would not work
* Fixed an issue where upgrading via MSI would remove the configured service account
* Fixed an issue where Install-PSUServer would not work on Mac OS

## 

## 1.5.6 - 12/12/2020

### Includes

* UniversalDashboard - v3.2.3
* UniversalDashboard - v2.9.9
* UniversalDashboard.Charts - 1.3.1
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Changed

* Fixed an issue where subscription licenses could cause the server to hang on startup.

## 1.5.5 - 12/11/2020

### Includes

* UniversalDashboard - v3.2.3
* UniversalDashboard - v2.9.9
* UniversalDashboard.Charts - 1.3.1
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Changed

#### API

* Fixed an issue where variables would not be available in APIs are server restart

#### Automation

* Fixed an issue where calling a job from another job could fail

#### Dashboard

* UDv3 - Fixed an issue with New-UDButton and New-UDButtonIcon -Disabled not working properly
* UDv3 - Fixed an issue where passing a $null value to -Data of New-UDTable would cause a React error. 
* UDv3 - Fixed an issue where passing complex object properties to -Data of New-UDTable would result in a React error
* UDv2 - Fixed an issue where Set-UDElement -Content would not work with New-UDElement

#### Platform

* Fixed an issue where Get-PSUCache would throw an error when a key did not exist
* Default RedirectToHttps to false because there is no default HTTPS endpoint

## 1.5.4 - 12/04/2020

### Includes

* UniversalDashboard - v3.2.2
* UniversalDashboard - v2.9.8
* UniversalDashboard.Charts - 1.3.1
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Added

#### Dashboard

* Added cmdlet help

### Changed

#### API

* Fixed an issue where -UseDefaultCredentials would not work with an API running as a service with Windows Auth 

#### Automation

* Fixed an issue where triggers could not use the Management API
* Fixed an issue where the Execute role would not be able to login to the admin console.

#### Dashboard

* Fixed an issue where -DataPointHistory would not work on New-UDChartJSMonitor
* Set default values for -BaseUrl and -DashboardFramework on New-PSUDashboard
* Fixed an issue where -Role was not being enforced properly for authenticated dashboards
* Fixed an issue where authentication could not be enabled on a dashboard even with a license
* UDv3 - Fixed a regression with Set-UDElement and UDTextbox in a UDForm
* UDv3 - Added -FullWidth to New-UDAutocomplete

#### Platform

* Universal cmdlets will now show a warning if connecting to a mismatched server and module version
* Fixed an issue where Install-PSUServer wouldn't work for Linux or Mac. 

## 1.5.3 - 11/26/2020

### Includes

* UniversalDashboard - v3.2.1
* UniversalDashboard - v2.9.8
* UniversalDashboard.Charts - 1.3.0
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Changed

#### Automation

* Fixed an issue where you couldn't create a schedule with Run As credentials
* Fixed an issue where you couldn't create two schedules for one script
* Fixed an issue where Run As credentials wouldn't be listed in the schedule table
* Fixed an issue where One Time jobs could run more than once
* Fixed an issue where scripts with absolute or nested paths would not be visible in the admin console 

#### Platform

* Fixed an issue where login page would not reload on server restart
* Fixed an issue where you could not change the Identity role within the admin console

### Added

#### API

* Added support for param block in API endpoints

### Removed

#### Platform

* Removed the Never expiration lifetime for app tokens. 

## 1.5.2 - 11/22/2020

### Includes

* UniversalDashboard - v3.2.1
* UniversalDashboard - v2.9.8
* UniversalDashboard.Charts - 1.3.0
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Changed

#### API

* Fixed an issue where non-global rate limits would not work
* Fixed an issue where New-PSURateLimit would call the incorrect REST API method

#### Automation

* Fixed an issue with Invoke-UAScript not working
* Fixed an issue where -ScriptBlock would not work on New-PSUScript when using single-file configuration.
* Fixed an issue where -TimeOut was an int instead of a double on New-PSUScript

#### Dashboard

* Fixed an issue where missing components could cause dashboards to fail to start or update from the UI
* Fixed an issue where dashboard could be started multiple times and would not stop properly

#### Platform

* Fixed an issue where Start-PSUServer wouldn't correctly identify the configuration script.
* Fixed an issue where Get-PSUEnvironment was not exported in the module manifest
* Fixed an issue where Grant-PSUAppToken would not generate custom tokens
* Fixed an issue where Remove-PSUEnvironment was not exported in the module manifest
* Added icon to the MSI

## 1.5.1 - 11/20/2020

### Includes

* UniversalDashboard - v3.2.1
* UniversalDashboard - v2.9.8
* UniversalDashboard.Charts - 1.3.0
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Added

#### Dashboard

* UDv3 - Added -Text parameter to New-UDCard
* UDv3 - Added -LoadNavigation to New-UDPage

### Changed

#### Automation

* Fixed an issue where automation jobs would not run as the selected user
* Fixed an issue where the Get-Job -Script parameter would not work

#### Dashboard

* UDv3 - Fixed an issue with -Disable didn't work for New-UDSelect
* UDv3 - Fixed an issue where -PageSize and -PageOptions would not work in New-UDTable
* UDv3 - Fixed an issue where export would not work
* UDv3 - Fixed an issue where search would not work
* Fixed an issue where multiple dashboard processes could be started for one dashboard.

#### Platform

* Fixed an issue where Start-PSUServer would located the Universal.Server.exe correctly
* Fixed an issue where Install-PSUServer didn't have a default parameter set.
* Fixed an issue where an upgrade from 1.4 to 1.5 would fail
* Fixed an issue where the login page customizations wouldn't work for certain license types
* Fixed an issue with the ZIP file created for Mac OS X systems
* Fixed an issue where Start-PSUServer would not work on Linux or Mac OS X
* Fixed an issue where Start-PSUServer would not call chmod +x on Linux and Mac OS X
* Fixed an issue where the New-PSUAuthorizationClaim cmdlet wasn't exported from the module manifest

## 1.5.0 - 11/17/2020

### Includes

* UniversalDashboard - v3.2.0
* UniversalDashboard - v2.9.8
* UniversalDashboard.Charts - 1.3.0
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Added

#### Automation

* Added timeout value to jobs 
* Added execute only role
* Added concurrent job limit for scripts
* Added support for string\[\] parameters in the UI

#### Dashboard

* Added $RemoteIpAddress, $LocalIpAddress, $LocalPort and $RemotePort automatic variables
* UDv3 - Added New-UDDateTime
* UDv3 - Added -Logo to New-UDDashboard and New-UDPage
* Added support for query string parameters 
* Added support for setting the dashboard to use the latest UD version. 
* Added $ClaimsPrincipal variable
* Added support for defining default documents for published folders
* UDv3 - Added New-UDErrorBoundary
* UDV3 - Added -DefaultTheme to New-UDDashboard
* Added New-UDChartJSMonitor and Out-UDChartJSMonitorData to UniversalDashboard.Charts.
* Added a Refresh context menu command to the dashboard log
* UDv3 - Added -Content parameter to Set-UDElement

#### Platform

* Added support for updating and retrieving configuration files through the management API
* Added support for setting the PSModulePath on environments
* Added support for Mac OS
* Added support for customizing login pages.
* Added support for disabling redirection from HTTP to HTTPS
* Added server-level cache support
* Added support for creating custom app tokens.
* Added support for disabling forms authentication

### Changed

#### API

* Fixed an issue with the API editor where it would lose characters
* Licensed API modals will default to authenticated

#### Automation

* Fixed an issue where using the same script multiple times would cause issues

#### Dashboard

* UDv3 - Fixed an issue with MaxWidth on Show-UDModal
* Fixed an issue where boolean $EventData variables would be hashtables rather than bools
* Fixed an issue where an error would be shown when a new runspace was created
* Automatically reload client's browsers when dashboards change
* Fixed an issue where the configuration reload would delete files 
* Marketplace won't let you install already installed modules
* Licensed dashboard modals will default to authenticated

#### Automation

* Fixed an issue where running as a service, you wouldn't be able to change the selected credential

#### Dashboard

* Fixed an issue with gRPC and Linux ARM
* Fixed an issue where deploying dashboard assets could fail during startup
* Fixed an issue where attempting to retrieve the highest dashboard version would fail 
* Optimized configuration loading behavior to only reload items that changed
* Moving some configuration data to an in-memory database for better performance

#### Platform

* Prevent custom roles from viewing the admin console
* Fixed an issue where standard cmdlets wouldn't work in authentication.ps1

## 1.4.9 - 11-10-2020

### Includes

* UniversalDashboard - v3.1.6
* UniversalDashboard - v2.9.8
* UniversalDashboard.Charts - 1.2.0
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Added

#### Dashboard

* Added support for RemoteIpAddress, LocalIpAddress, RemotePort, and LocalPort variables

### Changed

#### Platform

* Fixed an issue with web server performance on Windows

## 1.4.8 - 11-9-2020

### Includes

* UniversalDashboard - v3.1.6
* UniversalDashboard - v2.9.8
* UniversalDashboard.Charts - 1.2.0
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Added

#### Platform

* Added -PersistentRunspace to New-PSUEnvironment to prevent APIs from resetting runspaces per execution.

### Changed

#### API

* Fixed an issue where characters would be lost when saving API changes
* Fixed an issue where editor themes would conflict between the API editor and other editors
* Fixed an issue where the API host would fail to load the Universal module

#### Automation

* Fixed an issue where running as a service, you wouldn't be able to change the selected credential

#### Dashboard

* UDv2 - Fixed an issue where the session timeout modal would use the existing header of a modal 
* UDv2 - Fixed an issue where New-UDSideNav -Endpoint would not work
* Fixed an issue where dashboards could be marked as running when they actually were not
* Fixed an issue where the alt text for the View button was Global.
* Fixed an issue where Windows auth would not redirect correctly for dashboards
* UDv3 - Fixed an issue where -LoadingComponent would only work once

## 1.4.7 - 11-2-2020

### Includes

* UniversalDashboard - v3.1.5
* UniversalDashboard - v2.9.7
* UniversalDashboard.Charts - 1.2.0
* UniversalDashboard.Map - 1.0
* UniversalDashboard.CodeEditor - 1.0.4

### Added

#### Dashboard

* UDv3 - Added Debug-PSUDashboard
* UDv2 - Added session timeout modal 

#### Platform

* Added setting for RedirectToHttps

### Changed

#### Dashboard

* Improved error logging. 
* UDv3 - Fixed an issue with Set-UDElement not updating the form context for UDTextbox
* UDv3 - Fixed an issue where PSCustomObjects wouldn't work after a table refresh 
* UDv3 - Fixed an issue where server-side tables $EventData.properties field was not populated

#### Platform

* Fixed an issue where $ and " would not be escaped in variable values

## 1.4.6 - 10-27-2020

### Added

#### Dashboard

* UDv3 - Added -FullWidth parameter to New-UDTextbox

### Changed

#### API

* Fixed issue where endpoint modal was not setting authentication setting correctly. 

#### Automation

* Fixed an issue where job logs would not update during job runs. 

#### Dashboard

* Fixed issue where session timeout was only honored on the cookie
* Fixed issue with dashboard modal not setting authentication setting correctly. 
* Fixed issue where the dashboard log may not be written and would throw an exception
* UDv3 - Fixed an issue where PSCustomObjects would not work in New-UDTable

#### Platform

* Fixed an issue where arguments were not correctly applied to Environments
* Fixed an issue where setting the ExecutionPolicy as an argument in Environments would not apply

## 1.4.5 - 10-20-2020

#### API

* Fixed an issue where Windows Auth outside of IIS would not work with APIs

#### Dashboard

* UDv3 - Fixed an issue with UDTable custom rendering performance
* Fixed an issue where if a dashboard was stopped, no statistics could be retrieved for any dashboards
* Fixed an issue with icons not working
* UDv2 Fixed issue an where Get-UDElement would not work. 
* UDv2 Fixed an issue where Write-UDLog would not work.
* UDv3 Fixed an issue where -Role was case sensitive for New-UDPage
* UDv2 Fixed an issue where -Role was missing on New-UDPage

#### Platform

* Fixed an issue where an exception could be thrown when using OpenID Connect
* Fixed issue where you couldn't set arguments in the UI for Environments

#### Breaking Change 

There was a breaking change made to `New-UDTableColumn` -Render. The `$Body`  variable is no longer available and you need to use `$EventData` instead. See the below example for the syntax that will be required. 

Prior to 1.4.5, the syntax would have been like this. 

```text
$Data = @(
    @{ link = "http://www.google.com" }
)

$Columns = @(
    New-UDTableColumn -Property Link -Render { 
      $Data = $Body | ConvertFrom-Json
      New-UDLink -Text 'Link' -Url $Data.link
    }
)

New-UDTable -Title 'Link' -Column $Column -Data $Data
```

1.4.5 and later, the syntax will be like this. `$EventData` is a special variable that will be available in the `-Render` parameter and does not require converting from JSON.

```text
$Data = @(
    @{ link = "http://www.google.com" }
)

$Columns = @(
    New-UDTableColumn -Property Link -Render { 
    New-UDLink -Text 'Link' -Url $EventData.link
    }
)

New-UDTable -Title 'Link' -Columns $Columns -Data $Data
```

## 1.4.4 - 10-13-2020

### Added

#### API

* Added -ErrorAction support to New-PSUEndpoint

### Changed

#### API

* Enhanced logging for endpoints that throw errors

#### Dashboard

* UDv3 - Fixed an issue with UDTable not working within UDCard.
* UDv3 - Fixed an issue where calling Set-UDElement on a UDTextbox would overlay the label.
* UDv2 - Fixed an issue where OpenID Connect and WS-Federation authentication would fail
* UDv2\UDv3 - Fixed an issue where client elements of UDElement would not rerender. 
* Fixed an issue where saving a component from the marketplace would return a 400 error

#### Platform

* Removed red dots in the menu when a license wasn't installed
* Fixed an issue where the WindowsCompatibility module would not work in Universal

## 1.4.3 - 10-06-2020

### Added

#### Platform

* Added a setting to disable checking for updates

### Changed

#### API

* Extra validation on endpoint URL
* Fixed issue with authentication setting not persisting from UI
* Fixed an issue where modifying variables or environments wouldn't change until service restart

#### Automation

* Fixed an issue where parameters for schedules were not formatted correctly in the UI
* Fixed an issue where updating the properties of a script in the UI would remove the environment parameter

#### Dashboard

* Fixed an issue where modifying variables or environments wouldn't change until service restart
* Fixed an issue where OnNodeClicked would not work with New-UDTreeView
* Fixed an issue that was preventing the dashboard from loading in IE11

#### Platform

* Fixes for accessibility of menus
* Fixed an issue where secrets may not be set correctly in an environment
* Fixed an issue that would cause the service to crash when dashboards were logging

## 1.4.2 - 10-02-2020

### Changed

#### Dashboard

* Fixed an issue where saving dashboards.ps1 configuration file would lose components
* Fixed an issue where upgrading would cause the loss of a one of the PS versions
* UDv3 - Fixed an issue where table would show an error if an object was passed to a column
* Fixed an issue where the Code Editor diff tool wouldn't work

#### Platform

* Fixed an issue where the configuration refresh endpoint would only work with cookie auth
* Fixed an issue where secrets would not be set in an environment

## 1.4.1 - 10-01-2020

### Changed

#### Platform

* Fixed an issue that would prevent forms based authentication form working. 

## 1.4.0 - 10-01-2020

### Added

#### API

* Added -ApiEnvironment parameter to Set-PSUSettings
* Added API rate limiting
* Added LocalIpAddress, RemoteIpAddress, LocalPort and RemotePort variables

#### Automation

* Continuous scheduling

#### Dashboard

* UDCodeEditor component is now included
* UDv3 - Added -Variant to New-UDDrawer
* UDv3 - Added -Anchor to New-UDDrawer
* UDv3 - Added -PageSize to New-UDTable
* UDv3 - Added -PageSizeOptions to New-UDTable
* UDv3 - Added -Padding to New-UDTable
* Role-based access for dashboards
* UDv3 - Role-based access for dashboard pages. 
* UDv3 - Display page when dashboard isn't running
* UDv2 - Fixed an issue where UDMonitor colors would not work
* Added ChartJS charts to the charts component library
* Added OnCancel to New-UDForm
* Added $EventData hashtable to events that take data. 
* UDv3 - Added -NavigationLayout and -Navigation to New-UDPage
* UDv3 - Added -Multiline, -Rows, -RowsMax to New-UDTextbox

#### Platform

* Added New-PSUAuthenticationResult and New-PSUAuthorizationClaim
* Added support for defining custom claims during authentication
* Added support for Environments
* Windows Authentication support without IIS
* Added a setting to hide the admin console
* Added a setting to configure CORS
* Aliases for all cmdlets that start with PSU

### Changed

#### API

* Redesigned APIs and API page

#### Automation

* Fixed an issue where the job processes would inherit the parent process's PSModulePath
* Fixed an issue where Switch parameters would not work correctly 
* Fixed an issue where -ForegroundColor on Write-Host would add an extra line

#### Dashboard

* Redesigned dashboard page
* Fixed an issue with UDCodeEditor were Get-UDElement would not work. 
* Fixed an issue where New-UDTabs wouldn't work with one tab.
* Fixed an issue that would prevent custom components from using additional assets \(like images in UDMap\)
* Fixed an issue with UDMap that prevented it from including default images
* Fixed an issue where OpenID Connect and WS-Federation would not redirect correctly

#### Platform

* Fixed an issue where logging level would not apply to file logging

### Removed

#### Platform

* PowerShell version has been removed and merged into Environments

## 1.3.2 - 9-15-2020

### Changed

#### Automation

* Fixed an issue where you couldn't set the concurrent job limit

#### Dashboard

* Fixed an issue where the broadcast parameter would not work on cmdlets
* Fixed an issue where the theme background would not be applied
* Fixed an issue where custom dark and light themes would not work 

## 1.3.1 - 8-26-2020

### Changed

#### API

* Fixed an issue where a self-referencing loop with an object would cause an exception during serialization.

#### Automation

* Fixed issue where responding to feedback wouldn't work in the UI
* Fixed an issue where deleting a schedule wouldn't stop the schedule from running.
* Fixed an issue where script files would not be deleted when deleting a script

#### Dashboard

* Added dashboard memory history
* UDv2 - Fixed UDMonitor default values
* UDv3 - Fixed UDTypography style parameter
* UDv3 - Fixed an issue with the UDIcon parameter. 
* UDv3 - Fixed an issue where -ReplaceToast on Show-UDToast would not work
* Fixed an issue where the dashboard runspace would attempt to set readonly variables
* Fixed an issue where dashboard files would not be deleted when deleting a dashboard

#### Platform

* All files are now written using UTF8 with BOM encoding
* Fixed an issue where AppTokens were being deleted
* Fixed swagger API docs. 
* Fixed an issue where the Admin Console would be blank after upgrades

## 1.3.0 - 7-30-2020

### Added

#### API

* Added support for Windows Authentication in APIs running under IIS
* Added a $Headers variable in the API to provide the calling header values
* Added a $URL variable in the API to provide the calling URL
* Added a $Data variable in the API to provide byte\[\] of the content
* Added New-PSUApiResponse to support returning custom responses from APIs

#### Automation

* Fixed an issue where jobs would time out after 30 minutes and another job would be started in their place.
* Fixed an issue where cancelling a job wouldn't totally cancel the job
* Fixed an issue where you could not schedule a one time script

#### Dashboard

* UDv2 - Fixed an issue where custom components wouldn't load correctly
* Fixed an issue where saving the PowerShell Version wouldn't work from the UI
* Fixed an issue where dashboards would fail to start because assets would deploy after attempting to start dashboards
* UDv3 - Added support for custom stylesheets and scripts
* UDv3 - Added Test-UDForm to manually invoke form validation
* UDv3 - Added support for validation in UDStepper
* UDv3 - Added New-UDUpload for uploading files. Works with UDForm and UDStepper.
* UDv2 - Fixed an issue with UDFooter where it wouldn't load successfully
* Fixed an issue where errors with components would present a blank page. Now errors will be shown on the page. 
* UDv2 - Added NavBarLogo, NavBarColor and NavBarFontColor to New-UDDashboard
* Dashboards now have access to the $Cache:Pages variable that will return a list of the pages for the dashboard

#### Platform

* Fixed an issue where granting an app token would grant roles twice
* PowerShell host for API and Dashboard now implements the basics of Raw UI to avoid errors. 
* Added support for setting parameters for scheduled jobs

#### Dashboard

* Added Debug-PSUDashboard to run dashboards in a local PowerShell process
* Added Get-PSUDashboardEndpointRunspace to find runspaces based on an endpoint ID 
* Added a marketplace page to get new components directly from the marketplace 
* Added support for published folders
* Added support for Nivo bubble charts

### Changed

#### Dashboard

* UDv3 - Fixed the autocomplete component
* UDv3 - Add padding on the back\next buttons for the stepper control

#### Platform

* Added 404 page to the admin console 
* Various fixes to role access to particular sections of the admin console
* Fixed an issue where Windows Auth would not evaluate roles correctly
* Added HasClaim support to role policy ClaimsPrincipal class
* Revoked and expired app tokens are now groomed from the database
* Added SUPPRESSBROWSER property to MSI to allow hiding the browser after install

## 1.2.10 - 7-22-2020

### Changed

#### Dashboard

* Fixed an issue where the $Roles variable would not be populated in authenticated dashboards 

## 1.2.9 - 7-15-2020

### Added

#### API

* Added $Identity variable that will include the identity name if authentication is used 

### Changed

#### API

* PowerShell host for API and Dashboard now implements the basics of Raw UI to avoid errors. 

#### Automation

* Fixed an issue where jobs would time out after 30 minutes and another job would be started in their place.
* Fixed an issue where cancelling a job wouldn't totally cancel the job
* Fixed an issue where you could not schedule a one time script

#### Dashboard

* UDv2 - Fixed an issue where custom components wouldn't load correctly
* Fixed an issue where saving the PowerShell Version wouldn't work from the UI
* Fixed an issue where dashboards would fail to start because assets would deploy after attempting to start dashboards
* PowerShell host for API and Dashboard now implements the basics of Raw UI to avoid errors. 
* Fixed an issue where the server could crash sometimes when dashboard were restarting

#### Platform

* Fixed an issue where granting an app token would grant roles twice

## 1.2.8 - 7-7-2020

### Changed

#### Automation

* Fixed an issue where secret variables would not be set within scripts

## 1.2.7 - 7-6-2020

### Changed

#### API

* Fixed an issue where cookie authentication would not work with APIs

#### Automation

* Fixed an issue where you couldn't start jobs using Azure AD credentials
* Fixed an issue where you couldn't specify the PowerShell version for schedules
* Fixed an issue where secret variable names with non-standard characters would cause errors

#### Dashboard

* Fixed an issue where components and frameworks would be blocked when running from a ZIP on Windows
* Fixed issue where Set-UDClipboard would not work

#### Platform

* Fixed an issue where Windows Authentication would not evaluate roles correctly
* Fixed an issue with Grant-UAAppToken where it would not report the Role or Expiration back to the server
* Renamed Connect-UAServer to Connect-PSUServer. Alias added for backwards compatibility
* Renamed Grant-UAAppToken to Connect-PSUAppToken. Alias added for backwards compatibility
* Renamed Get-UAAppToken to Get-PSUAppToken. Alias added for backwards compatibility
* Renamed Get-UDDashboard to Get-PSUDashboard. Alias added for backwards compatibility
* Fixed an issue with Grant-PSUAppToken where it wouldn't allow custom roles.
* Auto reload feature ignores .git folder

### Removed

#### Platform

* Removed Enable-UAAuthentication as it is not required to use this cmdlet. Authentication is always enabled.

## 1.2.6 - 6-29-2020

### Changed

#### Automation

* Fixed an issue where jobs could not be started as a different user in IIS on a domain joined machine

#### Dashboard

* UDv3 Fixed an issue where tables would cause the page to not load
* UDv2 Fixed an issue where navigation links would not have the correct URL
* UDv2 Fixed an issue where the footer was set to absolute positioning

## 1.2.5 - 6-26-2020

### Changed

#### Platform

* Fixed an issue where a Universal license wouldn't correctly license Automation
* Fixed an issue where roles could be updated by any user
* Fixed an issue where roles could not be edited in the UI
* Hide menu items that users don't have access to
* Fixed an issue where deleting an identity that had apptokens would cause the apptoken page to not load
* Fixed an issue where deleting an identity that ran a job would cause the job page to not load

## 1.2.4 - 6-24-2020

### Changed

#### Dashboard

* Fixed an issue where importing a dashboard couple overwrite the dashboard being imported.

## 1.2.3 - 6-24-2020

### Added

#### Automation

* The identity of the user that started the job is now show in the table and job page 

#### Dashboard

* Added an Import Dashboard button
* Added -DisableAutostart to New-PUSDashboard to prevent dashboards from starting on server startup. 

#### Platform

* Added support for Git sync with default credentials

### Changed

#### APIs

* The API process will restart if it crashes for whatever reason.
* Fixed an issue where the API process wouldnt always start
* Fixed an issue where responses over a certain size wouldn't be returned. 

#### Automation

* Fixed an error that would be shown when run as another account and looking up secrets
* Fixed an issue where jobs would only work with one feedback request
* Fixed an error where an invalid schedule would cause an error in the UI.
* Fixed an issue where Automation would attempt to start and invalid job

#### Dashboard

* Fixed an issue where terminating errors would not be shown in the dashboard
* UDv3 - Fixed an issue where errors in components wouldn't be shown
* Fixed an issue where using the ZIP on Windows would fail to load the UD framework because it was blocked
* Dashboards now start asynchronously when the server is starting so the server starts faster
* Fixed an issue where dashboards wouldnt always start
* When adding a dashboard, the frameworks are now sorted newest first. 

#### Platform

* Fixed an issue where adding an invalid license would totally break everything
* If HTTP\(S\) is not specified when using the ComputerName parameter of the cmdlets, HTTP will be added automatically
* Fixed an issue where navigating to any URL that started with /admin would always go to the admin page
* Fixed an issue where Git sync would not work with a bare remote repository
* Redirect stdout to main process so you can see background process stdout. 

## 1.2.2 - 6-16-2020

### Changed

#### Automation

* Fix an issue where setting parameters would not allow a script to run

## 1.2.1 - 6-16-2020

### Added

#### APIs

#### Automation

#### Dashboard

#### Platform

* Added a -SecurityPowerShellVersion parameter to Set-PSUSetting to allow for customization of the security process's PS version
* Released a Docker image
* Added delete button to Identity table

### Changed

#### APIs

* Errors will now return status code 500 from APIs
* Fixed an issue where running APIs in Windows PowerShell would not work

#### Automation

* Fixed an issue where saving a full path for a script would not work
* Scripts are run based on path and not content

#### Dashboard

* Fixed an issue where the dashboard would restart every 60 seconds
* Fixed unhandled exceptions that would be thrown when trying to access a dashboard that didn't start correctly
* Start\Stop button now indicates whether it is in progress
* Fixed a bug where the dashboard would not restart if settings where changed in the dashboards.ps1
* UDv2 - Fixed page styling
* UDv2 - Fixed error shown when a UDInput only had a single field
* Fixed an issue with the Console where it would not show terminating errors
* Fixed an issue with the Console where if a dashboard wasnt running it would return nothing
* Display dashboard framework version in dashboard table

#### Platform

* Run Authentication\Authorization in process by default
* Fixed an issue where loading configuration files could result in a "Authorization Failed" exception
* Fixed an issue where if loading a configuration file on start up failed the server wouldn't start\
* Fixed an issue where hiding Automation would still default to the scripts page. 
* Fixed an error when starting PSU on linux. 
* Fixed an issue where settings wouldn't reload sometimes 
* Fixed a bug where the login page would not display an error if the login failed. 
* Log an error during startup if .NET Framework v4.7.2 or later is missing on Windows. 
* Fixed an issue where saving or deleting PowerShell versions in the UI wouldn't persist. 
* Fixed an issue where saving or deleting Dashboard Frameworks in the UI wouldn't persist. 
* Fixed an issue where the installer would not elevate correctly
* Fixed an issue where you couldn't uninstall from Add\Remove programs
* Fixed an issue where the installer would not upgrade successfully sometimes
* Fixed an issue wehere the installer would have the wrong version listedn in Add\remove programs

## 1.2.0 - 6-8-2020

### Added

#### APIs

* Added Support for REST APIs

#### Automation

* Added configuration options for InformationPreference, VerbosePreference and DebugPreference for scripts 

#### Dashboard

* UDv3 - Added support for themes
* Added Dashboard Components page in UI
* In-Browser editor for dashboard files

#### Platform

* Idempotent Configuration using PS cmdlets rather than classes
* Added Install-PSUServer cmdlet
* Added Start-PSUServer cmdlet
* Added the ability to configure which menu items are shown.
* WS-Federation support
* Added Swagger documentation
* Added link to help under settings

### Changed

#### APIs

#### Automation

* Fixed an issue where setting Mandatory = $false would make the parameter mandatory in the UI

#### Dashboard

* Remove file path from Add Dashboard modal. A default dashboard will be created. 
* UDv3 - Fixed an issue with expansion panels not working if you had a single expansion panel in a group.
* UDv2 - Fixed an issue where New-UDFooter was missing
* UDv2 - Fixed an issue where New-UDFooter wouldn't remove the "Created with UD" text 
* UDv2 - Fixed an issue where New-UDRow would not set the ID
* UDv2\UDv3 - Added error boundaries so controls in an error state do not prevent the dashboard from loading.
* UDv3 - Fixed Show-UDToast styles
* UDv2 - Fixed an issue where New-UDInput was missing
* UDv2 - Fixed an issue where New-UDMonitor was missing 
* Fixed an issue where logging into the dashboard wouldn't redirect to the dashboard
* Universal app tokens can now automatically be added to users' sessions to access the Universal API from dashboards

#### Platform

* Git Sync is Optional
* Fixed an issue where you couldn't delete a license
* Moved trial information to license page
* Fixed is with localization of dates and times
* Session timing out will redirect you to login
* Auto reload of entire platform when configuration changes

## 1.1.1 - 25-05-2020

### Changes

* Sign dashboard framework modules
* Unblock dashboard files before executing them
* Set execution policy on Windows
* Change default web.config to use correct settings
* Fixed a scoping issue with v2 New-UDPage
* Added debug logging to dashboard logging
* Fixed an issue where assigning a dashboard with a baseurl of "/" would break Universal
* Fixed custom component loading
* Added Nivo, Sparklines, and Map components
* Fixed an issue that would prevent adding dashboards after selecting a PS version
* Fixed a scoping issue with UD endpoints
* Linux Support

## 1.1.0 - 18-05-2020

### Changes

– Fixed an issue that prevented cmdlets from loading PSv5.1 – Add-UDDashboardFramework now returns pipeline output – Default endpoint now listens on all addresses, not just localhost – Fixed an issue with dashboard pages and spaces – Fixed an issue with the UDv2 grid not loading

### Added

– Added -Version to Add-UDDashboardFramework – Added support for UD scheduled endpoints – Added memory usage and session count to dashboard page – Added theme support for UDv2 – Added custom log path appsettings.json – Added UD Admin Terminal – Roles are now sync’d to git – Auth Methods are now sync’d to git – Session diagnostics for UD – Endpoint diagnostics for UD – Dashboard frameworks are now persisted across installs

