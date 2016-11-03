---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 7B30E5B5-27F3-41C3-9AFE-E2ACB4BAF8BA
---

# Set-MsolCompanyContactInformation

## SYNOPSIS
Sets company-level contact information.

## SYNTAX

```
Set-MsolCompanyContactInformation [-TechnicalNotificationEmails <String[]>]
 [-MarketingNotificationEmails <String[]>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The Set-MsolCompanyContactInformation cmdlet is used to set company-level contact preferences.
This includes email addresses for marketing and technical notifications about Microsoft Azure Active Directory.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Set-MsolCompanyContactInformation -TechnicalNotificationEmail tech@contoso.com

          None
```

Description

-----------

This command sets contact email addresses for the company.

## PARAMETERS

### -MarketingNotificationEmails
Company-level marketing information contact email address.

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

### -TechnicalNotificationEmails
Company-level technical information contact email address.

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

### -TenantId
The unique ID of the tenant to perform the operation on.
If this is not provided then the value will default to the tenant of the current user.
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


