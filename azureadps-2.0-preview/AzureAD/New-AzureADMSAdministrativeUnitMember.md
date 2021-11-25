---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# New-AzureADMSAdministrativeUnitMember

## SYNOPSIS
Create a new object as a member of the administrativeUnit.
Currently only group objects are supported.

## SYNTAX

```
New-AzureADMSAdministrativeUnitMember -Id <String> [-OdataType <String>]
 [-AssignedLabels <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AssignedLabel]>]
 [-Description <String>] -DisplayName <String> [-IsAssignableToRole <Boolean>] -MailEnabled <Boolean>
 -MailNickname <String> [-ProxyAddresses <System.Collections.Generic.List`1[System.String]>]
 -SecurityEnabled <Boolean> [-GroupTypes <System.Collections.Generic.List`1[System.String]>]
 [-MembershipRule <String>] [-MembershipRuleProcessingState <String>] [-Visibility <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The New-AzureADMSAdministrativeUnitMember cmdlet creates an Azure Active Directory (Azure AD) object as a member of an administrativeUnit.

Currently only Azure Active Directory groups are supported to be created as administrativeUnit members.

For information about creating dynamic groups, see [Using attributes to create advanced rules](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/).

## EXAMPLES

### Example 1: Create a dynamic group in an administrativeUnit
```
PS C:\> New-AzureADMSAdministrativeUnitMember -Id "5c99c435-43de-42a3-a420-a5c90b7ccc5a" -OdataType "Microsoft.Graph.Group" -DisplayName  "testGroupInAU10" -Description "testGroupInAU10" -MailEnabled $True -MailNickname "testGroupInAU10" -SecurityEnabled $False -GroupTypes @("Unified","DynamicMembership") -MembershipRule "(user.department -contains 'Marketing')" -MembershipRuleProcessingState "On"

Id                                   DisplayName     Description
--                                   -----------     -----------
89df76f0-b37a-4f41-8cd5-c5800ca89bd2 testGroupInAU10 testGroupInAU10
```

This command creates a new dynamic group in an administrativeUnit with the following rule:

\`user.department -contains "Marketing"\`

The double quotation marks are replaced with single quotation marks.

The processing state is On. 
This means that all users in the directory that qualify the rule are added as members to the group.
Any users that do not qualify are removed from the group.

## PARAMETERS

### -Id
Specifies the ID of an Active Directory administrative unit.

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

### -OdataType
Specifies the odata type of the object to create in the administrativeUnit.

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
This parameter determines the visibility of the group's content and members list.
This parameter can take one of the following values:

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

### -AssignedLabels
This parameter allows the assignment of sensitivity labels to groups. For more information on how sensitivity labels can be assigned to groups, refer to [Assign sensitivity labels](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/)

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.AssignedLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### -IsAssignableToRole
Flag indicates whether group can be assigned to a role. This property can only be set at the time of group creation and cannot be modified on an existing group.

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

### -ProxyAddresses
Sets the [proxyAddresses attribute](https://docs.microsoft.com/en-us/troubleshoot/azure/active-directory/proxyaddresses-attribute-populate).

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).


## RELATED LINKS

[Add-AzureADMSAdministrativeUnitMember](https://docs.microsoft.com/en-us/powershell/module/azuread/add-azureadmsadministrativeunitmember)

[Get-AzureADMSAdministrativeUnitMember](https://docs.microsoft.com/en-us/powershell/module/azuread/get-azureadmsadministrativeunitmember)

[Remove-AzureADMSAdministrativeUnitMember](https://docs.microsoft.com/en-us/powershell/module/azuread/remove-azureadmsadministrativeunitmember)

[New-AzureADMSGroup](https://docs.microsoft.com/en-us/powershell/module/azuread/new-azureadmsgroup)
