---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: A98FA4E7-3662-433C-A28D-CAF4D60592A1
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
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

### Example 1: Add a license to a user based on a template user
```
PS C:\> $LicensedUser = Get-AzureADUser -ObjectId "TemplateUser@contoso.com"  
PS C:\> $User = Get-AzureADUser -ObjectId "User@contoso.com"  
PS C:\> $License = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicense 
PS C:\> $License.SkuId = $LicensedUser.AssignedLicenses.SkuId 
PS C:\> $Licenses = New-Object -TypeName Microsoft.Open.AzureAD.Model.AssignedLicenses 
PS C:\> $Licenses.AddLicenses = $License 
PS C:\> Set-AzureADUserLicense -ObjectId $User.ObjectId -AssignedLicenses $Licenses
```

The first command gets a user by using the [Get-AzureADUser](./Get-AzureADUser.md) cmdlet, and then stores it in the $LicensedUser variable.

The second command gets another user by using **Get-AzureADUser**, and then stores it in the $User variable.

The third command creates an **AssignedLicense** type, and then stores it in the $License variable.

The fourth command set the **SkuId** property of $License to the same value as the **SkuId** property of $LicensedUser.

The fifth command creates an **AssignedLicenses** object, and stores it in the $Licenses variable.

The sixth command adds the license in $License to $Licenses.

The final command assigns the licenses in $Licenses to the user in $User.
The licenses in $Licenses includes $License from the third and fourth commands.

## PARAMETERS

### -AssignedLicenses
Specifies a list of licenses to assign or remove.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADUser](./Get-AzureADUser.md) 
