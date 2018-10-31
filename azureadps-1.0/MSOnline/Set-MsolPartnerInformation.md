---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 089BACA3-BA23-479B-BA92-06280F96AC48
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolPartnerInformation

## SYNOPSIS
Sets company information for partners.

## SYNTAX

```
Set-MsolPartnerInformation [-ObjectId <Guid>] [-CompanyType <CompanyType>] [-PartnerCompanyName <String>]
 [-PartnerSupportTelephones <String[]>] [-PartnerSupportEmails <String[]>] [-PartnerCommerceUrl <String>]
 [-PartnerSupportUrl <String>] [-PartnerHelpUrl <String>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-MsolPartnerInformation** cmdlet is used by partners to set partner-specific properties.
These properties can be viewed by all tenants that the partner has access to.

## EXAMPLES

### Example 1: Update the help URL
```
PS C:\> Set-MsolPartnerInformation -PartnerHelpUrl "http://www.help.contoso.com"
```

This command updates the help URL for this partner.

## PARAMETERS

### -PartnerCommerceUrl
Specifies the URL for the partner's commerce website.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartnerHelpUrl
Specifies the URL for the partner's Help website.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartnerSupportEmails
Specifies the support email address for the partner.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartnerSupportTelephones
Specifies the support telephone numbers for the partner.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartnerSupportUrl
Specifies the URL for the partner's support website.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CompanyType
Specifies the partner's company type.

```yaml
Type: CompanyType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the partner.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PartnerCompanyName
Specifies the partner's company name.


```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
[Get-MsolPartnerInformation](./Get-MsolPartnerInformation.md)
