---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-AzureADMSGroup

## SYNOPSIS
Creates an Azure AD group.

## SYNTAX

```
New-AzureADMSGroup [-Description <String>] -DisplayName <String> -MailEnabled <Boolean> -MailNickname <String>
 -SecurityEnabled <Boolean> [-GroupTypes <System.Collections.Generic.List`1[System.String]>]
 [-MembershipRule <String>] [-MembershipRuleProcessingState <String>] [-Visibility <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADMSGroup cmdlet creates an Azure Active Directory (Azure AD) group.

For information about creating dynamic groups, see Using attributes to create advanced rules (https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/).

## EXAMPLES

### Example 1: Create a dynamic group
```
PS C:\> New-AzureADMSGroup -DisplayName "Dynamic Group 01" -Description "Dynamic group created from PS" -MailEnabled $False -MailNickName "group" -SecurityEnabled $True -GroupTypes "DynamicMembership" -MembershipRule "(user.department -contains ""Marketing"")" -MembershipRuleProcessingState "On"

Id                            : 9126185e-25df-4522-a380-7ab697a7241c
Description                   : Dynamic group created from PS
OnPremisesSyncEnabled         : 
DisplayName                   : Dynamic Group 01
OnPremisesLastSyncDateTime    : 
Mail                          : 
MailEnabled                   : False 
MailNickname                  : group 
OnPremisesSecurityIdentifier  : 
ProxyAddresses                : {} 
SecurityEnabled               : True 
GroupTypes                    : {} 
MembershipRule                : (user.department -eq "Marketing") MembershipRuleProcessingState : Paused
```

This command creates a new dynamic group with the following rule:

\`user.department -contains "Marketing"\`

The double quotation marks are replaced with single quotation marks.

The processing state is On. 
This means that all users in the directory that qualify the rule are added as members to the group.
Any users that do not qualify are removed from the group.

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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

Required: True
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES
This cmdlet is currently in Public Preview.
While a cmdlet is in Public Preview, we may make changes to the cmdlet which could have unexpected effects.
We recommend that you do not use this cmdlet in a production environment.

## RELATED LINKS

[Get-AzureADMSGroup]()

[Remove-AzureADMSGroup]()

[Set-AzureADMSGroup]()

[Using attributes to create advanced rules](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/)

