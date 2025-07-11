---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADMSNamedLocationPolicy

## SYNOPSIS
Updates a named location policy in Azure Active Directory by PolicyId.

## SYNTAX

```
Set-AzureADMSNamedLocationPolicy -PolicyId <String> [-OdataType <String>] [-Id <String>]
 [-DisplayName <String>] [-IpRanges <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.IpRange]>]
 [-IsTrusted <Boolean>]
 [-CountriesAndRegions <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.CountriesAndRegion]>]
 [-IncludeUnknownCountriesAndRegions <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows an admin to update a named location policy in Azure Active Directory by PolicyId.
Conditional access policies are custom rules that define an access scenario.

## EXAMPLES

### Example 1: Update an ip named location policy in Azure AD by PolicyId.
```
PS C:\> Set-AzureADMSNamedLocationPolicy -PolicyId 1aaaaaa1-2bb2-3cc3-4dd4-5eeeeeeeeee5 -OdataType "#microsoft.graph.ipNamedLocation" -IsTrusted $false
```

This command updates an ip named location policy in Azure AD by PolicyId.

### Example 2: Update a country or region named location policy in Azure AD by PolicyId.
```
PS C:\> Set-AzureADMSNamedLocationPolicy -PolicyId 2bbbbbb2-3cc3-4dd4-5ee5-6ffffffffff6 -OdataType "#microsoft.graph.countryNamedLocation" -IncludeUnknownCountriesAndRegions $true
```

This command updates a country or region named location policy in Azure AD by PolicyId.

## PARAMETERS

### -PolicyId
Specifies the ID of a named location policy in Azure Active Directory.

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

### -OdataType
Specifies the odata type of a named location policy object in Azure Active Directory.

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
Specifies the display name of a named location policy in Azure Active Directory.

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

### -IpRanges
Specifies the ip ranges of the named location policy in Azure Active Directory.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.IpRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsTrusted
Specifies the isTrusted value for the named location policy in Azure Active Directory.

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

### -CountriesAndRegions
Specifies the countries and regions for the named location policy in Azure Active Directory.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.CountriesAndRegion]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeUnknownCountriesAndRegions
Specifies the includeUnknownCountriesAndRegions value for the named location policy in Azure Active Directory.

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

### -Id
{{ Fill Id Description }}

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

See the [migration guide for Set-AzureADMSNamedLocationPolicy](./migrate/Set-AzureADMSNamedLocationPolicy.md) to the Microsoft Graph PowerShell.

## RELATED LINKS

[Get-AzureADMSNamedLocationPolicy](Get-AzureADMSNamedLocationPolicy.md)

[New-AzureADMSNamedLocationPolicy](New-AzureADMSNamedLocationPolicy.md)

[Remove-AzureADMSNamedLocationPolicy](Remove-AzureADMSNamedLocationPolicy.md)
