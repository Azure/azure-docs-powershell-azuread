---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: 93C48D95-DB26-4F76-8078-CF845E9BCC8D
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolContact

## SYNOPSIS
Gets contacts from Azure Active Directory.

## SYNTAX

### ListContacts__0 (Default)
```
Get-MsolContact [-HasErrorsOnly <Boolean>] [-SearchString <String>] [-MaxResults <Int32>] [-TenantId <Guid>]
 [<CommonParameters>]
```

### GetContact__0
```
Get-MsolContact -ObjectId <Guid> [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolContact [-HasErrorsOnly <Boolean>] [-SearchString <String>] [-All] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolContact** cmdlet gets a contact object or list of contacts.
Specify the _ObjectId_ parameter to get a single contact.

## EXAMPLES

### Example 1: Get a contact
```
PS C:\> Get-MsolContact -ObjectId adc41dc7-4130-4215-adfb-2403bc9f844e
```

This command retrieves a contact.

### Example 2: Get contacts that match a string
```
PS C:\> Get-MsolContact -SearchString "Patti"
```

This command retrieves a list of contacts with a display name or email address starting with Patti.

## PARAMETERS

### -All
Indicates that this cmdlet returns all results that it finds.
Do not specify this parameter and the _MaxResults_ parameter.

```yaml
Type: SwitchParameter
Parameter Sets: All__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HasErrorsOnly
Indicates that this cmdlet returns contacts that have validation errors.

```yaml
Type: Boolean
Parameter Sets: ListContacts__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxResults
Specifies the maximum number of results that this cmdlet returns.
The default value is 500.

```yaml
Type: Int32
Parameter Sets: ListContacts__0
Aliases:

Required: False
Position: Named
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectId
Specifies the unique object ID of the contact to get.

```yaml
Type: Guid
Parameter Sets: GetContact__0
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
Specifies a string.
This cmdlet returns contacts with a display name or email address that start with this string.

```yaml
Type: String
Parameter Sets: ListContacts__0, All__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.Contact
This cmdlet returns contact objects, which include the following information:

* City. The contact's city.

* Country. The contact's country.

* Department. The contact's department.

* DisplayName. The contact's display name.

* Fax. The contact's fax number.

* FirstName. The contact's first name.

* LastDirSyncTime. Returns the date and time of the last sync (only returned from contacts synced with Active Directory synchronization).

* LastName. The contact's last name.

* MobilePhone. The contact's mobile phone number.

* ObjectId. The unique ID of the contact.

* Office. The contact's office number.

* Phone Number. The contact's phone number.

* Postal Code. The contact's postal code.

* Proxy Addresses. The proxy addresses associated with this contact.

* State. The contact's state.

* StreetAddress. The contact's street address.

* Title. The contact's title.

* UserPrincipalName. The user ID of the contact.

* ValidationStatus. Whether or not the contact has any errors.

## NOTES

## RELATED LINKS
[Remove-MsolContact](./Remove-MsolContact.md)
