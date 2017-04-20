---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipalPolicy

## SYNOPSIS

## SYNTAX

```
Get-AzureADServicePrincipalPolicy -Id <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>]
```

## DESCRIPTION
The Get-AzureADServicePrincipalPolicy cmdlet gets the policy of a service principal in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get a policy
```
PS C:\>Get-AzureADServicePrincipalPolicy -ObjectId "<object id of service principal>"
```

This command get the policy for the specified service principal.

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

### -Id
The ID of the Service Principal for which you want to retrieve the policy

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

[Add-AzureADServicePrincipalPolicy]()

[Remove-AzureADServicePrincipalPolicy]()

