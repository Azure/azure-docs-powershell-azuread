---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: A98FA4E7-3662-433C-A28D-CAF4D60592A1
online version: 
schema: 2.0.0
ms.reviewer: rodejo
ms.custom: Evergreen
---

# Set-AzureADUserLicense

## SYNOPSIS
Adds or removes licenses for a Microsoft online service to the list of assigned licenses for a user.

## SYNTAX

```
Set-AzureADUserLicense -ObjectId <String> -AssignedLicenses <AssignedLicenses>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureADUserLicense** adds or removes licenses for a Microsoft online service to the list of assigned licenses for a user.

## EXAMPLES

### Example 1: Add or remove a license for a user

```powershell
# Create the objects we'll need to add and remove licenses
$license = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense
$licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses

# Find the SkuID of the license we want to add - in this exmample we'll use the O365_BUSINESS_PREMIUM license
$license.SkuId = (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value "O365_BUSINESS_PREMIUM" -EQ).SkuID

# Set the OFFice license as the license we want to add in the $licenses object
$licenses.AddLicenses = $license

# Call the Set-AzureADUserLicense cmdlet to set the license.
Set-AzureADUserLicense -ObjectId "Violeta.Collias@drumkit.onmicrosoft.com" -AssignedLicenses $licenses

$Licenses.AddLicenses = @()
$Licenses.RemoveLicenses =  (Get-AzureADSubscribedSku | Where-Object -Property SkuPartNumber -Value "O365_BUSINESS_PREMIUM" -EQ).SkuID
Set-AzureADUserLicense -ObjectId "Violeta.Collias@drumkit.onmicrosoft.com" -AssignedLicenses $licenses 
```

## PARAMETERS

### -AssignedLicenses
Specifies a list of licenses to assign or remove. This parameter takes an object of the type Microsoft.Open.AzureAD.Model.AssignedLicenses, as shown in the example above. This contains two attributes that we'll be using here: 
+ AddLicenses is list that contians objects of the type Microsoft.Open.AzureAD.Model.AssignedLicense
+ RemoveLicenses is a list that contains obejcts of the type String

To add new licenses to a user, specify these in the AddLicenses property, to remove licenses add them to the list in the RemoveLicenses property. Licenses that are assigned to a user but are not mentioned in the RemoveLicenses or AddLicenses proeprties are not changed.

```yaml
Type: AssignedLicenses
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the ID of a user (as a UPN or ObjectId) in Azure AD. 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADUser](./Get-AzureADUser.md) 
