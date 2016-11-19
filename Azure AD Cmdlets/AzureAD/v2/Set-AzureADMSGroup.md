---
external help file: AzureAD.Help.xml
online version: https://go.microsoft.com/fwLink/?LinkID=519265&clcid=0x409
schema: 2.0.0
---

# Set-AzureADMSGroup

## SYNOPSIS
Set a group's attributes

## SYNTAX

```
Set-AzureADMSGroup [-Id <String>] [-Description <String>] [-DisplayName <String>] [-MailEnabled <Boolean>]
 [-MailNickname <String>] [-SecurityEnabled <Boolean>]
 [-GroupTypes <System.Collections.Generic.List`1[System.String]>] [-MembershipRule <String>]
 [-MembershipRuleProcessingState <String>]
```

## DESCRIPTION
This cmdlet is used to change  attribute values on a group.

## EXAMPLES

### Update the description of a group
```
Set-AzureADMSGroup -Id ce0a2213-bd57-4e2f-b9fa-408582e2e260 -description "Another group"
```

This cmdlet sets the description of the group with id ce0a2213-bd57-4e2f-b9fa-408582e2e260 to the value "Another group"


This cmdlet has no output

### Update the membership processing state of a group
```
Set-AzureADMSGroup -Id ce0a2213-bd57-4e2f-b9fa-408582e2e260 -MembershipRuleProcessingState "Paused"
```

This command sets the membership rule processing state of the group with Id ce0a2213-bd57-4e2f-b9fa-408582e2e260 to the value "Paused".
Group members are no longer updates when the membership rule processing state is set to "Paused"


This cmdlet has no output

### Set the dynamic membership rule on a group
```
Set-AzureADMSGroup -Id ce0a2213-bd57-4e2f-b9fa-408582e2e260 -MembershipRule "(user.department -eq ""Sales"")"
```

This cmdlet sets the membership rule of the group with Id ce0a2213-bd57-4e2f-b9fa-408582e2e260 to the value "(user.department -eq ""Sales"")"


Please note the use of the double quotes inside the rule - these are converted to single quotes when the rule is set on the group.

## PARAMETERS

### -Id
The id of the group for which attribute values are set

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Description
The description of the group

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
The displayname of the group

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

### -MailEnabled
Boolean value indicating whether or not this group is mail enabled.
Note that creation of mail enabled groups is currently not possible in Azure AD

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
The mail naickname of the group.
This is a mandatory value even when Mailenabled is false

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
This parameter indicated that the group is security enabled.
For security groups this value must be set to True

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

### -GroupTypes
This parameter indicates that the group is a dynamic group. 
To create a dynamic group, set this value to "DynamicMembership"

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
This parameter contains the membership rule for a dynamic group.
Learn more about the rules you can use for dynamic groups here: https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/

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
This parameter indicates the rule processing state.
Set this to "Paused" to stop processing the group's rule.
The members list will remain unchanged.
Set this to "On" to process the rule.

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

## INPUTS

### System.String

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

