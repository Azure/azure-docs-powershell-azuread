---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADMSGroup

## SYNOPSIS
Updates a specific unified group in Azure AD.

## SYNTAX

```
Set-AzureADMSGroup -Id <String> [-Description <String>] [-DisplayName <String>] [-MailEnabled <Boolean>]
 [-MailNickname <String>] [-SecurityEnabled <Boolean>]
 [-GroupTypes <System.Collections.Generic.List`1[System.String]>] [-Visibility <String>] [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADMSGroup cmdlet updates an Azure Active Directory (Azure AD) group.

## EXAMPLES

### Example 1: Change group to be dynamic
```
PS C:\> Set-AzureADMSGroup -Id "9126185e-25df-4522-a380-7ab697a7241c" -GroupTypes "DynamicMembership" -MembershipRule "(user.department -eq "Sales")" -MembershipRuleProcessingState "On"
```

For information about updating dynamic groups, see Using attributes to create advanced rules (https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/).

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
Set-AzureADMSGroup -ObjectId "11fa5e1e-737c-40c5-835e-416ae3959606" 

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
Specifies the ID of the group that this cmdlet updates.

```yaml
Type: String

=======
Parameter Sets: GetById
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MailNickname
Specifies a mail nickname for the group.
If MailEnabled is $False you must still specify a mail nickname.

```yaml
Type: String
Parameter Sets: (All)

Aliases:
=======
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MembershipRule
Specifies the membership rule for a dynamic group.

For more information about the rules that you can use for dynamic groups, see Using attributes to create advanced rules (https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/).

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

* "On". Process the group rule.
* "Paused". Stop processing the group rule.

Changing the value of the processing state does not change the members list of the group.

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Visibility
This parameter determines the visibility of the group's content and members list. This parameter can take one of the following values:

* "Public" - Anyone can view the contents of the group
* "Private" - Only members can view the content of the group
* "HiddenMembership" - Only members can view the content of the group and only members, owners, Global/Company Administrator, User Administrator and Helpdesk Administrators can view the members list of the group.

If no value is provided, the default value will be "Public".

Notes:

* This parameter is only valid for groups that have the groupType set to "Unified".
* If a group has this attribute set to "HiddenMembership" it cannot be changed later.
* Anyone can join a group that has this attribute set to "Public". If the attribute is set to Private or HiddenMembership, only owner(s) can add new members to the group and requests to join the group need approval of the owner(s).

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

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

=======

[Get-AzureADMSGroup](get-azureadmsgroup.md)

[Remove-AzureADMSGroup](remove-azureadmsgroup.md)

[New-AzureADMSGroup](new-azureadmsgroup.md)

[Using attributes to create advanced rules](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/)

