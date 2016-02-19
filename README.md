# Office365Connectivity.ps1 #
A script to simeltaneously connect to each o365 service with your provided credentials

The script will attempt to check for module availability and load as it goes

* MSOL
* SharePoint Online
* Skype for Business Online
* Exchange Online
* Exchange Online Protection

### Function Usage ###

 ./Connect-o365

Prompts for credentials and tries to import modules and log you in


./Connect-o365 -getprereq

Downloads the x64 version of pre-requisite files to c:\temp\connecto365prereq

* .NET Framework 4.5.2 Offline Installer URL
* Microsoft Online Services Sign-In Assistant for IT Professionals RTW URL
* Sharepoint Online Management Shell URL
* Skype for Business Online Windows PowerShell Module URL


./Connect-o365 -Credential $variable

Pass a username/password combo variable created with get-credential to the script for use, useful when you
have multiple tenants to manage, and store credentials in clixml objects or load in with your $profile


./Disconnect-o365

Attempts to clean up all pssessions that we created
