---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 800AD06B-DDC3-4594-A339-4135A525155F
---

# Get-AzureADTenantDetail

## SYNOPSIS
Gets the details of a tenant.

## SYNTAX

```
Get-AzureADTenantDetail [-Top <Int32>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADTenantDetail** cmdlet gets the details of a tenant in Azure Active Directory (AD).
## EXAMPLES

### Example 1: Get details for a tenant
```PowerShell
PS C:\>Get-AzureADTenantDetail

ObjectId                             DisplayName            VerifiedDomains
--------                             -----------            ---------------
85b5ff1e-0402-400c-9e3c-0f9e965325d1 Coho Vineyard & Winery {class VerifiedDomain {...
```

## PARAMETERS

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

### -InformationAction
Specifies how this cmdlet responds to an information event. The acceptable values for this parameter are:

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


