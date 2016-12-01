---
external help file: AzureAD.Help.xml
online version: https://channel9.msdn.com/Series/Azure-Active-Directory-Videos-Demos/ManageAppsAzureADPowerShell
schema: 2.0.0
---

# Revoke-AzureADUserAllRefreshToken

## SYNOPSIS
Invalidates all of the user's refresh tokens issued to applications (as well as session cookies in a user's browser), by resetting the refreshTokensValidFromDateTime user property to the current date-time

## SYNTAX

```
Revoke-AzureADUserAllRefreshToken -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Revoke all refresh tokens for a given user
```
Revoke-AzureADUserAllRefreshToken -ObjectId a1d91a49-70c6-4d1d-a80a-b74c820a9a33
```

## PARAMETERS

### -ObjectId
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

