---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
ms.assetid: FD2AE118-42DC-4DA4-A705-17972ECCA1E7
online version: 
schema: 2.0.0
---

# Remove-AzureADGroupMember

## SYNOPSIS
Removes a member from a group.

## SYNTAX

```
Remove-AzureADGroupMember -ObjectId <String> -MemberId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-AzureADGroupMember** cmdlet removes a member from a group in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove a member
```
PS C:\>Remove-AzureADGroupMember -ObjectId "62438306-7c37-4638-a72d-0ee8d9217680" -MemberId "0a1068c0-dbb6-4537-9db3-b48f3e31dd76"
```

This command removes the specified member from the specified group.

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

### -MemberId
Specifies the ID of the member to remove.

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

### -ObjectId
Specifies the object ID of a group in Azure AD.

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

[Add-AzureADGroupMember](./Add-AzureADGroupMember.md)

[Get-AzureADGroupMember](./Get-AzureADGroupMember.md)
