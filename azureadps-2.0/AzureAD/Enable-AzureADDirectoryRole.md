---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: 3719960D-7A77-414E-A20C-812B527F27AB
online version: 
schema: 2.0.0
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Enable-AzureADDirectoryRole

## SYNOPSIS
Activates an existing directory role in Azure Active Directory.

## SYNTAX

```
Enable-AzureADDirectoryRole [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-DirectoryRole <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-AzureADDirectoryRole** cmdlet activates an existing directory role in Azure Active Directory.

## EXAMPLES

### Example 1: Enable a directory role
```
# Get Guest Inviter directory role template
$roleTemplate = Get-AzureADDirectoryRoleTemplate | ? { $_.DisplayName -eq "Guest Inviter" }

# Enable an instance of the DirectoryRole template
Enable-AzureADDirectoryRole -RoleTemplateId $roleTemplate.ObjectId
```

The first command gets an inviter role that has the display name Guest Inviter by using the [Get-AzureADDirectoryRoleTemplate](./Get-AzureADDirectoryRoleTemplate.md) cmdlet. The command stores Guest Inviter in the $roleTemplate variable. 

The second command instantiates an instance of the directory role in $roleTemplate.

## PARAMETERS

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
Specifies a variable in which to store an information event message.

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

### -RoleTemplateId
The ID of the Role template to enable

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADDirectoryRole](./Get-AzureADDirectoryRole.md)

[Get-AzureADDirectoryRoleTemplate](./Get-AzureADDirectoryRoleTemplate.md)
