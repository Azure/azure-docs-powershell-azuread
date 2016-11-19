---
external help file: AzureAD.Help.xml
online version: https://go.microsoft.com/fwLink/?LinkID=519265&clcid=0x409
schema: 2.0.0
---

# New-AzureADMSGroup

## SYNOPSIS

## SYNTAX

```
New-AzureADMSGroup [-Description <String>] -DisplayName <String> -MailEnabled <Boolean> -MailNickname <String>
 -SecurityEnabled <Boolean> [-GroupTypes <System.Collections.Generic.List`1[System.String]>]
 [-MembershipRule <String>] [-MembershipRuleProcessingState <String>]
```

## DESCRIPTION

## EXAMPLES

### Create a new Dynamic group
```
New-AzureADMSGroup -DisplayName "My first Dynamic Group" -Description "Dynamic group created from PS" -MailEnabled $false -MailNickName "group" -SecurityEnabled $true -GroupTypes "DynamicMembership" -MembershipRule "(user.department -contains ""Marketing"")" -MembershipRuleProcessingState "On"
```

This cmdlet creates a new dynamic group with the rule 'user.department -contains "Marketing"'.
The processing state is set ot "On", which means that all users in the directory that qualify the rule will get added as members to the group and any users that do not qualify are removed from the group.


You can learn more about dynamic groups here: https://go.microsoft.com/fwLink/?LinkID=519265&clcid=0x409


Id                            : 9126185e-25df-4522-a380-7ab697a7241c Description                   : Dynamic group created from PS OnPremisesSyncEnabled         : DisplayName                   : My first Dynamic Group OnPremisesLastSyncDateTime    : Mail                          : MailEnabled                   : False MailNickname                  : group OnPremisesSecurityIdentifier  : ProxyAddresses                : {} SecurityEnabled               : True GroupTypes                    : {} MembershipRule                : (user.department -eq "Marketing") MembershipRuleProcessingState : Paused

## PARAMETERS

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

Required: True
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

Required: True
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

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityEnabled
This paramter indicated that the group is security enabled.
For security groups this value must be set to True

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
This paramter indicates the rule processing state.
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

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[More information about dynamic group rules](https://go.microsoft.com/fwLink/?LinkID=519265&clcid=0x409)

