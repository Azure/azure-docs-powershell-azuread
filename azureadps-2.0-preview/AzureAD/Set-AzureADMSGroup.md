---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.Custom.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Set-AzureADMSGroup

## SYNOPSIS
{{Fill in the Synopsis}}

## SYNTAX

```
Set-AzureADMSGroup -Id <String> [-LabelId <String>] [-Description <String>] [-DisplayName <String>]
 [-IsAssignableToRole <Boolean>] [-MailEnabled <Boolean>] [-MailNickname <String>] [-SecurityEnabled <Boolean>]
 [-GroupTypes <System.Collections.Generic.List`1[System.String]>] [-MembershipRule <String>]
 [-MembershipRuleProcessingState <String>] [-Visibility <String>] [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADMSGroup -Id "9126185e-25df-4522-a380-7ab697a7241c" -DisplayName "Dynamic Group 01" -Description "Group created from PS" -MailEnabled $False -MailNickname "group" -SecurityEnabled $True -GroupTypes "" -MembershipRule "" -MembershipRuleProcessingState ""

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

Group updated.

### Example 2
```
PS C:\> Set-AzureADMSGroup -Id "9126185e-25df-4522-a380-7ab697a7241c" -IsAssignableToRole $true
        Bad Request.
```

IsassignableToRole property cannot be set for an existing group.

### Example 3
```
PS C:\> Set-AzureADMSGroup -Id "11111111-1111-1111-1111-111111111111" -LabelId "00000000-0000-0000-0000-000000000000"
```

The label is assigned to the group.

### Example 4
```
PS C:\> Set-AzureADMSGroup -Id "11111111-1111-1111-1111-111111111111" -LabelId ""
```

The label is removed from the group.

## PARAMETERS

### -Description
{{Fill Description Description}}

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
{{Fill DisplayName Description}}

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
{{Fill GroupTypes Description}}

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
{{Fill Id Description}}

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

### -IsAssignableToRole
Flag indicates whether Azure Active directory group can be assigned to a role.
This flag cannot be set for an existing group.

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

### -LabelId
Specifies a comma separated list of label identifiers to assign to the group.

Currently, only one label could be assigned to a group.

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

### -MailEnabled
{{Fill MailEnabled Description}}

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
{{Fill MailNickname Description}}

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
{{Fill MembershipRule Description}}

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
{{Fill MembershipRuleProcessingState Description}}

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
{{Fill SecurityEnabled Description}}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
