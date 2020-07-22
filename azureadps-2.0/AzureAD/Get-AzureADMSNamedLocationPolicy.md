---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADMSNamedLocationPolicy

## SYNOPSIS
Gets an Azure Active Directory named location policy.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSNamedLocationPolicy [<CommonParameters>]
```

### GetById
```
Get-AzureADMSNamedLocationPolicy -PolicyId <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows an admin to get the Azure Active Directory named location policy.
Named locations are custom rules that define network locations which can then be used in a Conditional Access policy.

## EXAMPLES

### Example 1: Retrieves a list of all named location policies in Azure AD.
```
PS C:\> Get-AzureADMSNamedLocationPolicy

          OdataType               : #microsoft.graph.ipNamedLocation
          Id                      : 06e4ff15-ca6b-4843-9c34-3fdd1ce8f739
          DisplayName             : IPv4 named location
          CreatedDateTime         : 2019-09-26T23:12:16.0792706Z
          ModifiedDateTime        : 2019-09-27T00:12:12.5986473Z
          IsTrusted               : false
          IpRanges                : {
                                      class IpRange {
                                        CidrAddress: 6.5.4.3/32
                                      }
                                    }
```

This command retrieves a list of all named location policies in Azure AD.

### Example 2: Retrieves a named location policy in Azure AD with given Id.
```
PS C:\> Get-AzureADMSNamedLocationPolicy -PolicyId 1b7f0916-7677-40d8-97a1-d606f4ed8fcf

          OdataType                           : #microsoft.graph.countryNamedLocation
          Id                                  : 1b7f0916-7677-40d8-97a1-d606f4ed8fcf
          DisplayName                         : Country named location
          CreatedDateTime                     : 2019-09-26T23:12:16.0792706Z
          ModifiedDateTime                    : 2019-09-27T00:12:12.5986473Z
          CountriesAndRegions                 : [
                                                  "US",
                                                  "CA"
                                                ]
          IncludeUnknownCountriesAndRegions   : false
```

This command retrieves a named location policy in Azure AD.

## PARAMETERS

### -PolicyId
Specifies the ID of a named location policy in Azure Active Directory.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
## RELATED LINKS

[New-AzureADMSNamedLocationPolicy]()

[Set-AzureADMSNamedLocationPolicy]()

[Remove-AzureADMSNamedLocationPolicy]()

