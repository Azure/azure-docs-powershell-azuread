---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADTenantDetail

## SYNOPSIS
Retrieves the details of a tenant in Azure Active Directory

## SYNTAX

```
Get-AzureADTenantDetail [-Top <Nullable`1[Int32]>]
```

## DESCRIPTION

## EXAMPLES

### Retrieve the details of a tenant
```
Get-AzureADTenantDetail

Output:


ObjectId                             DisplayName            VerifiedDomains 
--------                             -----------            --------------- 
85b5ff1e-0402-400c-9e3c-0f9e965325d1 Coho Vineyard & Winery {class VerifiedDomain {...
```

## PARAMETERS

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

