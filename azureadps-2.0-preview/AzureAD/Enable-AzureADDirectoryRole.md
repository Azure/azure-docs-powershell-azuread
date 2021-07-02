---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: 3719960D-7A77-414E-A20C-812B527F27AB
ms.custom: iamfeature=PowerShell
ms.reviewer: rodejo
online version:
schema: 2.0.0
---

# Enable-AzureADDirectoryRole

## SYNOPSIS
Activates an existing directory role in Azure Active Directory.

## SYNTAX

```
Enable-AzureADDirectoryRole [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [-RoleTemplateId <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-AzureADDirectoryRole** cmdlet activates an existing directory role in Azure Active Directory.

## EXAMPLES

### Example 1: Enable a directory role
```
# Retrieve the Template Role object for the Guest Inviter role 
$InviterRole = Get-AzureADDirectoryRoleTemplate | Where-Object {$_.DisplayName -eq "Guest Inviter"}

# Inspect the $Inviter variable to make sure we found the correct template role
$InviterRole

ObjectId                             DisplayName   Description
--------                             -----------   -----------
95e79109-95c0-4d8e-aee3-d01accf2d47b Guest Inviter Guest Inviter has access to invite guest users.

# Enable the Inviter Role
Enable-AzureADDirectoryRole -RoleTemplateId $InviterRole.ObjectId

ObjectId                             DisplayName   Description
--------                             -----------   -----------
03618579-3c16-4765-9539-86d9163ee3d9 Guest Inviter Guest Inviter has access to invite guest users.
```

The first command gets an inviter role that has the display name Guest Inviter by using the [Get-AzureADDirectoryRoleTemplate](./Get-AzureADDirectoryRoleTemplate.md) cmdlet. 
The command stores Guest Inviter in the $InviterRole variable. 

The second command displays the contents of $InviterRole.

The final command enables the directory role in $InviterRole.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADDirectoryRole](./Get-AzureADDirectoryRole.md)

[Get-AzureADDirectoryRoleTemplate](./Get-AzureADDirectoryRoleTemplate.md)
