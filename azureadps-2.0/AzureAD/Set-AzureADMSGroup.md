---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADMSGroup

## SYNOPSIS
Sets the properties for an existing Azure AD group.

## SYNTAX

```
Set-AzureADMSGroup -Id <String> [-Description <String>] [-DisplayName <String>] [-IsAssignableToRole <Boolean>]
 [-MailEnabled <Boolean>] [-MailNickname <String>] [-SecurityEnabled <Boolean>]
 [-GroupTypes <System.Collections.Generic.List`1[System.String]>] [-Visibility <String>] [<CommonParameters>]
```

## DESCRIPTION
The Set-AzureADMSGroup cmdlet sets the properties for an existing Azure Active Directory (Azure AD) group.

## EXAMPLES

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
Specifies the object ID of a group.

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
Indicates whether this group is mail enabled.

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
Indicates whether the group is security enabled.

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
Specifies the visibility of the group's content and members list.
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

### -IsAssignableToRole
This property can only be set at the time of group creation and cannot be modified on an existing group.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
