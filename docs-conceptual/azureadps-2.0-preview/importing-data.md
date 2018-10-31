---
services: active-directory
documentationcenter: ''

ms.service: active-directory
ms.workload: identity
ms.tgt_pltfrm: na
ms.devlang: powershell
ms.topic: article
ms.date: 07/10/2017
ms.author: rodejo
ms.custom: posh-docs-conceptual
ms.reviewer: rodejo
---
# Importing data into my directory
There are several ways you can use PowerShell to import data into your directory, but the most commonly used method is to use a CSV file. This file can either be manually created, for example using Excel, or it can be exported from an existing data source such as a SQL database or an HR application. Here are some common scenarios for import data into Azure Active Directory:

## Bulk creation of new users
If you want to bulk create users in Azure Active Directory and you have a csv file that contains information about the new users you want to create, here are some considerations:

1. You need to establish or implement a Naming Convention for usernames, display names and aliases. An example would be: Usernames are constructed from the last name of the user, followed by a period, followed by the first name. So "John Smith" in contoso.com would have a Username of "Smith.John@contoso.com". You will need to implement similar rules for display names - perhaps you want to add the department name to the display name, as in "John Smith (Accounting)" - and for alias.
2. You need to implement a convention for the initial password of the newly created user, and you need to figure out a way for the new users to receive their password in a secure way. Methods commonly used for this are generating a random password and emailing it to the new user or their manager.

Assuming you have established these, let's have a look at what the CSV file we're using to create the new users needs to contain. Here is an example of the CSV file we're using in this article:

```powershell
Firstname,MiddleInitials,Lastname,Department,JobTitle
Peter,S,Fischer,Development,Manager
James,T,McGuire,Research,Assistant
Karen,R,Cristo,Sales,Director
```

To bulk create these users using PowerShell we'll need to take several steps:

1. Setup a PowerShell session with your directory - we'll use the ```Connect-AzureAD``` cmdlet for this.
2. Import the data from the CSV file in your PowerShell session using the ```Import-CSV``` cmdlet.
3. For each line in the file, create the required parameters to create a new user 
4. Execute the cmdlet to create the new user using the ```New-AzureADUser``` cmdlet

If you were to use this script in a production environment, you'd probably also would like to add some additional parts, such as:

+ Error handling - what to do if a user cannot be created
+ Execution reporting - when the script has finished, provide an overview of what it did: number of users created etc.

We'll skip these parts for now and concentrate on the core functionality.

Here is the script that you can use to import the CSV file as shown and create new users. For this script to work in your environment you will need to update the values in the first section to the correct values for your own environment.

> Note: The password of the new users needs to conform to the password complexity rules you have set for your directory.
> Note: The Admin account you are specifying here needs to be an administrator in the directory you are specifying

```powershell
###
### These are vairable you need to update to reflect your environment
###

$Admin = "Admin@contoso.com"
$AdminPassword = "my password"
$Directory = "contoso.com"
$NewUserPassword = "newuserspasswords"
$CsvFilePath = "C:\work\users.csv"


###
### Create a PowerShell connection to my directory. If you do not want to specify the password in the script, you can simply replace this with "Connect-AzureAD", which will prompt for a username and password.
###

$SecPass = ConvertTo-SecureString $AdminPassword -AsPlainText -Force
$Cred = New-Object System.Management.Automation.PSCredential ($Admin, $SecPass)
Connect-AzureAD -Credential $cred

###
### Create a new Password Profile for the new users. We'll be using the same password for all new users in this example
###

$PasswordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile
$PasswordProfile.Password = $NewUserPassword

###
### Import the csv file. You will need to specify the path and file name of the CSV file in this cmdlet
###

$NewUsers = import-csv -Path $CsvFilePath

###
### Loop through all new users in the file. We'll use the ForEach cmdlet for this.
###

Foreach ($NewUser in $NewUsers) { 

###
### Construct the UserPrincipalName, the MailNickName and the DisplayName from the input data in the file 
###

    $UPN = $NewUser.Firstname + "." + $NewUser.LastName + "@" + $DirectoryName
    $DisplayName = $NewUser.Firstname + " " + $NewUser.Lastname + " (" + $NewUser.Department + ")"
    $MailNickName = $NewUser.Firstname + "." + $NewUser.LastName

###
### Now that we have all the necessary data for to create the new user, we can execute the New-AzureADUser cmdlet  
###

    New-AzureADUser -UserPrincipalName $UPN -AccountEnabled $true -DisplayName $DisplayName -GivenName $NewUser.FirstName -MailNickName $MailNickName -Surname $NewUser.LastName -Department $Newuser.Department -JobTitle $NewUser.JobTitle -PasswordProfile $PasswordProfile

###
### End the Foreach loop
###
    }
```powershell

> Note: After succesfully executing this script the new users will have been created in your Azure Active Directory. Not ethat since we have specified -AccountEnabled = $True, the new users can immediately use their password to sign in to the directory. If you do not want the users accounts to be active directly after running the script, you can specify -AccountEnabled = $False, and enable the accounts later using the Set-AzureADUser cmdlet.
