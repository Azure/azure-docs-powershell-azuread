---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Enable-AzureADDirectoryRole

## SYNOPSIS
Activates an existing directory role in Azure Active Directory

## SYNTAX

```
Enable-AzureADDirectoryRole -DirectoryRole <DirectoryRole>
```

## DESCRIPTION

## EXAMPLES

### Enable a directory role
```
$InviterRole = Get-AzureADDirectoryRoleTemplate | Where-Object {$_.DisplayName -eq "Guest Inviter"}
$InviterRole

ObjectId                             DisplayName   Description
--------                             -----------   -----------
95e79109-95c0-4d8e-aee3-d01accf2d47b Guest Inviter Guest Inviter has access to invite guest users.

$Role = New-Object Microsoft.Open.AzureAD.Model.DirectoryRole
$Role.RoleTemplateId = $InviterRole.ObjectId
Enable-AzureADDirectoryRole -DirectoryRole $Role

ObjectId                             DisplayName   Description
--------                             -----------   -----------
03618579-3c16-4765-9539-86d9163ee3d9 Guest Inviter Guest Inviter has access to invite guest users.
```

## PARAMETERS

### -DirectoryRole
Azure active directory role. 
Only the roleTemplateId is required - see the eample given below

```yaml
Type: DirectoryRole
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

