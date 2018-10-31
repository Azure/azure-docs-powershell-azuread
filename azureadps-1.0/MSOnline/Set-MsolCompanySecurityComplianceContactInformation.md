---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 5EFA8894-F622-48D0-97D4-3D673E08FF37
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Set-MsolCompanySecurityComplianceContactInformation

## SYNOPSIS
**This cmdlet is not in use by any online service, so please consider it deprecated.**  


## SYNTAX

```
Set-MsolCompanySecurityComplianceContactInformation [-SecurityComplianceNotificationEmails <String[]>]
 [-SecurityComplianceNotificationPhones <String[]>] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
**This cmdlet is not in use by any online service, so please consider it deprecated.**  
For more information about how to properly configure security contact details in Azure Security Center, see [Provide security contact details in Azure Security Center](https://aka.ms/azuresecuritycontact).

The **Set-MsolCompanySecurityComplianceContactInformation** cmdlet sets company-level security and compliance contact preferences.
These preferences include email addresses and phone numbers of the tenant’s security and compliance contacts.
The contact is used for notification purposes.


## EXAMPLES

### Example 1: Set contact information
```
Set-MsolCompanySecurityComplianceContactInformation -SecurityComplianceNotificationEmails "EvanNarvaez@contoso.com", "ElisaDaugherty@contoso.com" -SecuritComplianceNotificationPhones "555-555-0012","555-555-0199"
```
**This cmdlet is not in use by any online service, so please consider it deprecated.**  
For more information about how to properly configure security contact details in Azure Security Center, see [Provide security contact details in Azure Security Center](https://aka.ms/azuresecuritycontact).

This command sets multiple email addresses as company-level security and compliance contacts and respective phone numbers for each contact.


## PARAMETERS

### -SecurityComplianceNotificationEmails
Specifies an array of company-level security and compliance contact email addresses.

**This cmdlet is not in use by any online service, so please consider it deprecated.**  
For more information about how to properly configure security contact details in Azure Security Center, see [Provide security contact details in Azure Security Center](https://aka.ms/azuresecuritycontact).

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

### -SecurityComplianceNotificationPhones
Specifies an array of company-level security and compliance contact phone numbers.

**This cmdlet is not in use by any online service, so please consider it deprecated.**  
For more information about how to properly configure security contact details in Azure Security Center, see [Provide security contact details in Azure Security Center](https://aka.ms/azuresecuritycontact).

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
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.

**This cmdlet is not in use by any online service, so please consider it deprecated.**  
For more information about how to properly configure security contact details in Azure Security Center, see [Provide security contact details in Azure Security Center](https://aka.ms/azuresecuritycontact).


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

### System.String[]
System.Nullable`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## OUTPUTS

### System.Object

## NOTES
**This cmdlet is not in use by any online service, so please consider it deprecated.**  
For more information about how to properly configure security contact details in Azure Security Center, see [Provide security contact details in Azure Security Center](https://aka.ms/azuresecuritycontact).

## RELATED LINKS
