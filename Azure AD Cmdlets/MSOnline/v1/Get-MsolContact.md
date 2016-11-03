---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 93C48D95-DB26-4F76-8078-CF845E9BCC8D
---

# Get-MsolContact

## SYNOPSIS
Retrieves a contact from Microsoft Azure Active Directory.

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
The Get-MsolContact cmdlet can be used to retrieve a contact object, or list of contacts.
A single contact will be retrieved if the ObjectId is used.

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
Get-MsolContact -ObjectId <id>

          Returns the contact object.
```

Description

-----------

This command retrieves a contact.

### -------------------------- EXAMPLE 2 --------------------------
```
Get-MsolContact -SearchString "Melissa"

          Returns a list of contacts.
```

Description

-----------

This command retrieves a list of contacts with a display name or email address starting with 'Melissa'.

## PARAMETERS

### -All
If present then all results will be returned. 
Cannot be used with MaxResults parameter.

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
The filter for only contacts with validation errors.

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
The maximum number of results returned for a search.
If not specified, 500 results will be returned.

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
The unique ID of the contact to retrieve.

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
The string to search on.
Only contacts with a display name or email address starting with this string will be returned.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.Contact
This cmdlet returns contact objects, which include the following information:

            City: The contact's city.

            Country: The contact's country.

            Department: The contact's department.

            DisplayName: The contact's display name.

            Fax: The contact's fax number.

            FirstName: The contact's first name.

            LastDirSyncTime: Returns the date and time of the last sync (only returned from contacts synced with Active Directory synchronization).

            LastName: The contact's last name.

            MobilePhone: The contact's mobile phone number.

            ObjectId: The unique ID of the contact.

            Office: The contact's office number.

            Phone Number: The contact's phone number.

            Postal Code: The contact's postal code.

            Proxy Addresses - the proxy addresses associated with this contact.

            State: The contact's state.

            StreetAddress: The contact's street address.

            Title: The contact's title.

            UserPrincipalName: The user ID of the contact.

            ValidationStatus: Whether or not the contact has any errors.

## NOTES

## RELATED LINKS


