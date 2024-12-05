---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureADPreview
ms.assetid: CAA240EC-E380-4CDB-A1CC-56BBD28DFB82
ms.custom: iamfeature=PowerShell
ms.reviewer: stevemutungi
online version:
schema: 2.0.0
---

# Get-AzureADDirectoryRole

## SYNOPSIS
Gets a directory role.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADDirectoryRole [-Filter <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADDirectoryRole -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADDirectoryRole** cmdlet gets a directory role from Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a directory role by ID
```
PS C:\>Get-AzureADDirectoryRole -ObjectId "87166072-c682-42c6-8d6b-68c8fb88a868"

ObjectId                             DisplayName                        Description
--------                             -----------                        -----------
87166072-c682-42c6-8d6b-68c8fb88a868 Directory Writers              Can read and write basic directory information. For granting access to applications, not intended for users.
```

### Example 2: Get all directory roles
```
PS C:\>Get-AzureADDirectoryRole

ObjectId                             DisplayName                        Description
--------                             -----------                        -----------
87166072-c682-42c6-8d6b-68c8fb88a868 Directory Writers                  Can read and write basic directory information. For granting access to applications, not intended for users.
67efd1ad-1046-4fb8-bb57-1d2e4f66c74e Directory Readers                  Can read basic directory information. Commonly used to grant directory read access to applications and guests.

```

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

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
Specifies the ID of a directory role in Azure AD.

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Filter
{{ Fill Filter Description }}

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
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

[Enable-AzureADDirectoryRole](./Enable-AzureADDirectoryRole.md)
