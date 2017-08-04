---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureADMSGroupLifecyclePolicy

## SYNOPSIS
Updates a specific group Lifecycle Policy in Azure Active Directory

## SYNTAX

```
Set-AzureADMSGroupLifecyclePolicy -Id <String> [-GroupLifetimeInDays <Int32>] [-ManagedGroupTypes <String>]
 [-AlternateNotificationEmails <String>]
```

## DESCRIPTION
The Set-AzureADMSGroupLifecyclePolicy command updates a specific group Lifecycle Policy in Azure Active Directory

## EXAMPLES

### Example 1
```
PS C:\> Set-AzureADMSGroupLifecyclePolicy -Id "b4c908b0-3595-4add-91b4-c5400b31b57b" -GroupLifetimeInDays 200 -AlternateNotificationEmails "admingroup@contoso.com"
```

This command updates the specified groupLifecyclePolicy in Azure Active Directory

## PARAMETERS

### -AlternateNotificationEmails
Notification emails for groups that have no owners will be sent to these email addresses. List of email addresses separated by a ";".

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

### -GroupLifetimeInDays
The number of days a group can exist before it needs to be renewed

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies the ID of a groupLifecyclePolicies object in Azure Active Directory

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

### -ManagedGroupTypes
Allows the admin to select which office 365 groups the policy will apply to. "None" will create the policy in a disabled state. "All" will apply the policy to every Office 365 group in the tenant. "Selected" will allow the admin to choose specific Office 365 groups that the policy will apply to.

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

