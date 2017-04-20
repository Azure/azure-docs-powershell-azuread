---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserOwnedDevice

## SYNOPSIS
Get registered devices owned by a user.

## SYNTAX

```
Get-AzureADUserOwnedDevice -ObjectId <String> [-All <Boolean>] [-Top <Int32>]
```

## DESCRIPTION
The Get-AzureADUserOwnedDevice cmdlet gets registered devices owned by the specified user in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Get devices owned by a user
```
PS C:\>Get-AzureADUserOwnedDevice -ObjectId "df19e8e6-2ad7-453e-87f5-037f6529ae16"
```

This command gets the registered devices owned by the specified user.

## PARAMETERS

### -All
If true, return all objects owned by this user.
If false, return the number of objects specified by the Top parameter

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -Top
Specifies the maximum number of records to return.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

