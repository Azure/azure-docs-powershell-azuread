---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Set-AzureADUserLicense

## SYNOPSIS
Add and remove one or more licenses for a Microsoft online service to the list of assigned licenses for the user.

## SYNTAX

```
Set-AzureADUserLicense -ObjectId <String> -AssignedLicenses <AssignedLicenses>
```

## DESCRIPTION

## EXAMPLES

### Add a license to a user based on a template user
```
# Get the License SkuId from a template user that we want to apply to the new user 
$licensedUser = Get-AzureADUser -ObjectId "TemplateUser@contoso.com"  
# Get the new User we want to apply the license too 
$user = Get-AzureADUser -ObjectId "newuser@contoso.com"  
# Create the new License object 
$license = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense 
$license.SkuId = $licensedUser.AssignedLicenses.SkuId 
# Create the Licenses Table and add the license from above 
$licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses 
$licenses.AddLicenses = $license 
# Apply the license to the new user 
Set-AzureADUserLicense -ObjectId $user.ObjectId -AssignedLicenses $licenses
```

## PARAMETERS

### -ObjectId
The unique identifier of a user in Azure Active Directory (UPN or ObjectId)

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -AssignedLicenses
A list of licenses to be assigned and those to be removed.

Note that this parameter takes a complex type as a value - to create this type, use the New-Object cmdlet, as in:

$license = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense

```yaml
Type: AssignedLicenses
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

