---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
Module Name: AzureADPreview
online version:
schema: 2.0.0
---

# Remove-AzureADMSNamedLocationPolicy

## SYNOPSIS
Deletes an Azure Active Directory named location policy by PolicyId.

## SYNTAX

```
Remove-AzureADMSNamedLocationPolicy -PolicyId <String> [<CommonParameters>]
```

## DESCRIPTION
This cmdlet allows an admin to delete the Azure Active Directory named location policy.
Named locations are custom rules that define network locations which can then be used in a Conditional Access policy.

## EXAMPLES

### Example 1: Deletes a named location policy in Azure AD with given PolicyId.
```
PS C:\> Remove-AzureADMSNamedLocationPolicy -PolicyId 76fdfd4d-bd80-4c1e-8fd4-6abf49d121fe
```

This command deletes a named location policy in Azure AD.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES
## RELATED LINKS

[New-AzureADMSNamedLocationPolicy](New-AzureADMSNamedLocationPolicy.md)

[Set-AzureADMSNamedLocationPolicy](Set-AzureADMSNamedLocationPolicy.md)

[Get-AzureADMSNamedLocationPolicy](Get-AzureADMSNamedLocationPolicy.md)
