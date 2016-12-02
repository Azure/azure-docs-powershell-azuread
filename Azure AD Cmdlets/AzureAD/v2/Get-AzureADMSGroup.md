---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADMSGroup

## SYNOPSIS
Gets information about groups in Azure AD.

## SYNTAX


### UNNAMED_PARAMETER_SET_1
```
Get-AzureADMSGroup [-Filter <String>] [-Top <Int32>]
```

### UNNAMED_PARAMETER_SET_2
```
Get-AzureADMSGroup -Id <String>
```

### UNNAMED_PARAMETER_SET_3
```
Get-AzureADMSGroup [-SearchString <String>]
```

## DESCRIPTION
The **Get-AzureADMSGroup** cmdlet gets information about groups in Azure Active Directory (Azure AD).
To get a group, specify the _Id_ parameter. 
Specify the _SearchString_ or _Filter_ parameter to find particular groups. 
If you specify no parameters, this cmdlet gets all groups.

## EXAMPLES

### Example 1: Get all groups 
```
PS C:\> Get-AzureADMSGroup

Id                            : d539a25e-2db2-482a-9dcb-2a0b27fe4f27 
Description                   : 
OnPremisesSyncEnabled         : 
DisplayName                   : 
ADSyncOperators 
OnPremisesLastSyncDateTime    : 
Mail                          : 
MailEnabled                   : False
MailNickname                  : ADSyncOperators 
OnPremisesSecurityIdentifier  : S-1-5-21-2695029449-1154706203-1063139792-1243 
ProxyAddresses                : {} 
SecurityEnabled               : True 
GroupTypes                    : {} 
MembershipRule                : 
MembershipRuleProcessingState :


Id                            : d98ddc78-6e8d-4f0d-8a3f-b923c6ebc14b 
Description                   : 
OnPremisesSyncEnabled         : 
DisplayName                   : Project Icarus 
OnPremisesLastSyncDateTime    : 
Mail                          : 
MailEnabled                   : False 
MailNickname                  : 60f3d02c-0c6e-41da-bb64-128c73b4d9e6 
OnPremisesSecurityIdentifier  : 
ProxyAddresses                : {} 
SecurityEnabled               : True 
GroupTypes                    : {DynamicMembership} 
MembershipRule                : (user.jobtitle -eq "Sales manager") -or ((user.department -eq "Marketing") -and (user.country -eq "Greece")) 
MembershipRuleProcessingState : On
```

This command gets all groups in Azure AD.

### Example 2: Get a specific group by using an ID
```
PS C:\> Get-AzureADMSGroup -Id "d98ddc78-6e8d-4f0d-8a3f-b923c6ebc14b"

Id                            : d98ddc78-6e8d-4f0d-8a3f-b923c6ebc14b 
Description                   : 
OnPremisesSyncEnabled         : 
DisplayName                   : Project Icarus 
OnPremisesLastSyncDateTime    : 
Mail                          : 
MailEnabled                   : False 
MailNickname                  : 60f3d02c-0c6e-41da-bb64-128c73b4d9e6 
OnPremisesSecurityIdentifier  : 
ProxyAddresses                : {} 
SecurityEnabled               : True 
GroupTypes                    : {DynamicMembership} 
MembershipRule                : (user.jobtitle -eq "Sales manager") -or ((user.department -eq "Marketing") -and (user.country -eq "Greece")) 
MembershipRuleProcessingState : On
```

This command gets information for the group that has the specified ID.

## PARAMETERS

### -Filter
Specifies an oData v3.0 filter string to match a set of groups.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Id
Specifies the ID of the group that this cmdlet gets.

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string. 
This cmdlet gets groups that have **DisplayName** or **Description** attributes that match the search string. 

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_3
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records that this cmldet gets.
The default value is 100.

```yaml
Type: Int32
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

### System.String
System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]

## OUTPUTS

### System.Object

## NOTES
This cmdlet is currently in Public Preview.
While a cmdlet is in Public Preview, we may make changes to the cmdlet which could have unexpected effects.
We recommend that you do not use this cmdlet in a production environment.


## RELATED LINKS
[New-AzureADMSGroup](./New-AzureADMSGroup.md)

[Remove-AzureADMSGroup](./Remove-AzureADMSGroup.md)

[Set-AzureADMSGroup](./Set-AzureADMSGroup.md)

[#AzureAD: Certificate based authentication for iOS and Android now in preview!](https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/)
