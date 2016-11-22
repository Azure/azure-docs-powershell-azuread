---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserRegisteredDevice

## SYNOPSIS
Get registered devices registered by the user.

## SYNTAX

```
Get-AzureADUserRegisteredDevice -ObjectId <String> [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the devices that are registered for a given user
```
$UserId = (Get-AzureADUser -Top 1).ObjectId
Get-AzureADUserRegisteredDevice -ObjectId  $UserId
```

## PARAMETERS

### -ObjectId
The unique identifier of a user in Azure Active Directory (UPN or ObjectId)

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

### -Top
The maximum number of records to return.
If no value is provided, 100 records are returned

```yaml
Type: Nullable`1[Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

