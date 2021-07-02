---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Set-AzureADTenantDetail

## SYNOPSIS
Set contact details for a tenant

## SYNTAX

```
Set-AzureADTenantDetail [-MarketingNotificationEmails <System.Collections.Generic.List`1[System.String]>]
 [-PrivacyProfile <PrivacyProfile>]
 [-SecurityComplianceNotificationMails <System.Collections.Generic.List`1[System.String]>]
 [-SecurityComplianceNotificationPhones <System.Collections.Generic.List`1[System.String]>]
 [-TechnicalNotificationMails <System.Collections.Generic.List`1[System.String]>] [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is used to set various contact details for a tenant.

## EXAMPLES

### Example 1
```
PS C:\WINDOWS\system32> Set-AzureADTenantDetail -MarketingNotificationEmails "amy@contoso.com","henry@contoso.com" -SecurityComplianceNotificationMails "john@contoso.com","mary@contoso.com" -SecurityComplianceNotificationPhones "1-555-625-9999", "1-555-233-5544" -TechnicalNotificationMails "peter@contoso.com"
```

THis example shows how to set the various tenant details

## PARAMETERS

### -MarketingNotificationEmails
The email address that is used to send marketing notification emails

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityComplianceNotificationMails
The email address that is used to send security compliance emails

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityComplianceNotificationPhones
The phone number(s) that are used for security compliance

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TechnicalNotificationMails
The email address(es) that are used for technical notification emails

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivacyProfile
{{ Fill PrivacyProfile Description }}

```yaml
Type: PrivacyProfile
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

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
