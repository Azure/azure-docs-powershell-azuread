---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 089BACA3-BA23-479B-BA92-06280F96AC48
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
The Set-MsolPartnerInformation cmdlet is used by partners to set partner-specific properties.
These properties can be viewed by all tenants that the partner has access to.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Set-MsolPartnerInformation -PartnerHelpUrl "http://www.help.com"

          none
```

Description

-----------

Updates the help URL for this partner.

## PARAMETERS

### -PartnerCommerceUrl
URL for the partner's commerce website.

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
URL for the partner's Help website.

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
Support email address for the partner.

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
Support telephone numbers for the partner.

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
URL for the partner's support website.

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
The unique ID of the tenant to perform the operation on.
If this is not provided, then the value will default to the tenant of the current user.
This parameter is only applicable to partner users.

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


