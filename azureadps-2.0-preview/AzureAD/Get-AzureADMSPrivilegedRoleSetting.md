---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Get-AzureADMSPrivilegedRoleSetting

## SYNOPSIS
Get role settings

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSPrivilegedRoleSetting -ProviderId <String> [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSPrivilegedRoleSetting -ProviderId <String> -Id <String> [<CommonParameters>]
```

## DESCRIPTION
Get role settings

## EXAMPLES

### Example 1
```
PS C:\> Get-AzureADMSPrivilegedRoleSetting -ProviderId AzureResources -Filter "ResourceId eq 'e5e7d29d-5465-45ac-885f-4716a5ee74b5'"
```

Get role settings for a specific provider and resource

### Example 2
```
PS C:\> Get-AzureADMSPrivilegedRoleSetting -ProviderId AzureResources -Id 4b95b664-7434-48e6-8dec-34caf4d8c3bd
```

Get a role setting for a specific provider and Id

## PARAMETERS

### -Id
The unique identifier of the specific role setting

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Filter
The filter of Odata

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ProviderId
The unique identifier of the specific provider

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
The top count

```yaml
Type: Int32
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.String
### System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
