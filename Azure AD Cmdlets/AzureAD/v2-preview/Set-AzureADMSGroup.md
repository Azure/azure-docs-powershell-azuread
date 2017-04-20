---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureADMSGroup

## SYNOPSIS
Changes attribute values on an Azure AD group.

## SYNTAX

```
Set-AzureADMSGroup -Id <String> [-Description <String>] [-DisplayName <String>] [-MailEnabled <Boolean>]
 [-MailNickname <String>] [-SecurityEnabled <Boolean>]
 [-GroupTypes <System.Collections.Generic.List`1[System.String]>] [-MembershipRule <String>]
 [-MembershipRuleProcessingState <String>] [-Visibility <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureADMSGroup** cmdlet changes attribute values on an Azure Active Directory (Azure AD) group.

## EXAMPLES

### Example 1: Update the description of a group
```
PS C:\> Set-AzureADMSGroup -Id "ce0a2213-bd57-4e2f-b9fa-408582e2e260" -Description "Contoso Group 12"
```

This command changes the description of the group that has the specified ID to be Contoso Group 12.

### Example 2: Update the membership processing state of a group
```
PS C:\> Set-AzureADMSGroup -Id ce0a2213-bd57-4e2f-b9fa-408582e2e260 -MembershipRuleProcessingState "Paused"
```

This command changes the membership rule processing state of the group that has the specified ID to be Paused.
Group members are no longer updated when the membership rule processing state is Paused.

### Example 3: Set the dynamic membership rule on a group
```
Set-AzureADMSGroup -Id "ce0a2213-bd57-4e2f-b9fa-408582e2e260" -MembershipRule "(user.department -eq ""Sales"")"
```

This command changes the membership rule of the group that has the specified ID to the value (user.department -eq ""Sales"").

The sequence of two quotation marks in the rule are converted to single quotation marks when the rule is set on the group.

## PARAMETERS

### -Description
Specifies a description for the group.

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

### -DisplayName
Specifies a display name for the group.

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

### -GroupTypes
Specifies that the group is a dynamic group. 
To create a dynamic group, specify a value of DynamicMembership.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies the ID of the group for which attribute values are modified.

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

### -MailEnabled
Specifies whether this group is mail enabled.

Currently, you cannot create mail enabled groups in Azure AD.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MailNickname
Specifies a mail nickname for the group.
If _MailEnabled_ is $False, you must specify a mail nickname.

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

### -MembershipRule
Specifies the membership rule for a dynamic group.

For more information about the rules that you can use for dynamic groups, see [Using attributes to create advanced rules](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/).

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

### -MembershipRuleProcessingState
Specifies the rule processing state.
The acceptable values for this parameter are:

* On. Process the group rule.
* Paused. Stop processing the group rule. 
The members list remains unchanged.
This parameter determines the visibility of the group's content and members list. This parameter can take one of the following values:

"Public" - Anyone can view the contents of the group
"Private" - Only members can view the content of the group
"HiddenMembership" - Only members can view the content of the group and only members, owners, Global/Company Administrator, User Administrator and Helpdesk Administrators can view the members list of the group.

If no value is provided, the default value will be "Public".

Notes:

1. This parameter is only valid for groups that have the groupType set to "Unified".
2. If a group has this attribute set to "HiddenMembership" it cannot be changed later.
3. Anyone can join a group that has this attribute set to "Public". If the attribute is set to Private or HiddenMembership, only owner(s) can add new members to the group and requests to join the group need approval of the owner(s).

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

### -SecurityEnabled
Specifies whether the group is security enabled.
For security groups, this value must be $True.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Visibility
{{Fill Visibility Description}}

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

### System.String

## OUTPUTS

### System.Object

## NOTES
This cmdlet is currently in Public Preview.
While a cmdlet is in Public Preview, we may make changes to the cmdlet which could have unexpected effects.
We recommend that you do not use this cmdlet in a production environment.

## RELATED LINKS

[Get-AzureADMSGroup](./Get-AzureADMSGroup.md)

[New-AzureADMSGroup](./New-AzureADMSGroup.md)

[Remove-AzureADMSGroup](./Remove-AzureADMSGroup.md)

[Using attributes to create advanced rules](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/)
