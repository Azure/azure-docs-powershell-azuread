---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Remove-AzureADUserManager

## SYNOPSIS
Removes a user's manager.

## SYNTAX

```
Remove-AzureADUserManager -ObjectId <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>]
```

## DESCRIPTION
The Remove-AzureADUserManager cmdlet removes a user's manager in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove the manager of a user
```
PS C:\> $User = Get-AzureADUser -Top 1
PS C:\> Remove-AzureADUserManager -ObjectId $User.ObjectId
```

The first command gets a user by using the Get-AzureADUser (./Get-AzureADUser)cmdlet, and then stores it in the $User variable.

The second command removes the user in $User.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event.
The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the ID of a user (as a UPN or ObjectId) in Azure AD.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADUserManager]()

[Set-AzureADUserManager]()

