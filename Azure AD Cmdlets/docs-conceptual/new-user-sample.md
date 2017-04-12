# Creating a new user in Azure AD

This example shows how you can create a new user in Azure AD. In this example we will create a new user called "Abby Brown" in a directory called "contoso.com".

The cmdlet used is [New-AzureADUser](). This cmdlet has many parameters that you can use to decorate the new user object in Azure AD. In this example we'll only look at the mandatory parameters:
 
+ DisplayName - contains the display name for the new user, in our example this is "Abby Brown"
+ MailNickName - contains the email alias of the new user, we'll set it to "AbbyB"
+ UserPrincipalName - contains the UserPrincipalName (UPN) of this user. The UPN is what the user will use when they sign in into Azure AD. The common structure is <MailNickName>@<directory name>, so for Abby Brown in Contoso.com, the UPN would be "AbbyB@contoso.com"
+ AccountEnabled - this indicates whether the account is enabled for sign in. If you set it to $False, the user will not be able to use the account, but you can set it ti $True right now or do that later if you need to perform other configuration tasks for the new user, such as assigning licenses or applications.
+ PasswordProfile - Specifies the user's password profile. Note that the parameter type for this parameter is "PasswordProfile". in order to pass a parameter of this type, you first need to create a variable in PowerShell with that type. We can do that with the New-Object cmdlet:

```powershell $PasswordProfile = New-Object -TypeName Microsoft.Open.AzureAD.Model.PasswordProfile```

Then you can proceed to set the value of the password in this variable:

``` powershell $PasswordProfile.Password = "<Password>" ```

To create the user, call the New-AzureADUser cmdlet with the parameter values:

```powershell New-AzureADUser -AccountEnabled $True -DisplayName "Abby Brown" -PasswordProfile $PasswordProfile -MailNickName "AbbyB" -UserPrincipalName "AbbyB@contoso.com"```

PowerShell will return the new user object you just created and show the ObjectId:

```powershell 
ObjectId                             DisplayName UserPrincipalName                 UserType
--------                             ----------- -----------------                 --------
f36634c8-8a93-4909-9248-0845548bc515 New User    NewUser32@drumkit.onmicrosoft.com Member

```