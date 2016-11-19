---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: DD253761-F1BB-4EF1-B0CB-586C0040DECE
online version: 
schema: 2.0.0
---

# Get-AzureADDirectoryRoleMember

## SYNOPSIS
Gets members of a directory role.

## SYNTAX

```
Get-AzureADDirectoryRoleMember -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADDirectoryRoleMember** cmdlet gets the members of a directory role in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get members by role ID
```
PS C:\>Get-AzureADDirectoryRoleMember -ObjectId "019ea7a2-1613-47c9-81cb-20ba35b1ae48"

ObjectId                             ObjectType
--------                             ----------
ba6752c4-6a2e-4be5-a23d-67d8d5980796 User
df19e8e6-2ad7-453e-87f5-037f6529ae16 User
c13dd34a-492b-4561-b171-40fcce2916c5 User
0558a23b-438a-48aa-8e30-5042e0746f69 User
1fbae2b2-bb4b-48f9-bb38-83e9e1ad4bff User
```

This command gets the members of the specified role.

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

[Add-AzureADDirectoryRoleMember](./Add-AzureADDirectoryRoleMember.md)
[Remove-AzureADDirectoryRoleMember](./Remove-AzureADDirectoryRoleMember.md)

