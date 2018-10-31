---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: FF8B1BBA-6FF1-4739-A554-B83079EA4FEC
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolDirSyncProvisioningError

## SYNOPSIS
Checks for objects with synchronization provisioning errors in a tenant.

## SYNTAX

### ListDirSyncProvisioningErrors__0 (Default)
```
Get-MsolDirSyncProvisioningError [-ErrorCategory <String>] [-PropertyName <String>] [-PropertyValue <String>]
 [-SearchString <String>] [-SortField <SortField>] [-SortDirection <SortDirection>] [-MaxResults <Int32>]
 [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolDirSyncProvisioningError [-ErrorCategory <String>] [-PropertyName <String>] [-PropertyValue <String>]
 [-SearchString <String>] [-SortField <SortField>] [-SortDirection <SortDirection>] [-All] [-TenantId <Guid>]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolDirSyncProvisioningError** cmdlet checks for objects with synchronization provisioning errors in a tenant.

All parameter arguments for this cmdlet are case sensitive.

## EXAMPLES

### Example 1: Get all objects with provisioning errors
```
PS C:\>Get-MsolDirSyncProvisioningError -ErrorCategory PropertyConflict
```

This command gets all objects with DirSyncProvisioningErrors due to a PropertyConflict in the tenant.

### Example 2: Get all objects with provisioning errors using the UserPrincipalName attribute
```
PS C:\>Get-MsolDirSyncProvisioningError -ErrorCategory PropertyConflict -PropertyName UserPrincipalName
```

This command gets all objects with DirSyncProvisioningErrors due to a PropertyConflict on the UserPrincipalName attribute.

### Example 3: Get provisioning errors by property value
```
PS C:\>Get-MsolDirSyncProvisioningError -ErrorCategory PropertyConflict -PropertyName UserPrincipalName -PropertyValue "User@contoso.com"
```

This command gets all objects with DirSyncProvisioningErrors due to a PropertyConflict on the UserPrincipalName attribute with the property value of User@contoso.com.

### Example 4: Get provisioning errors by search string
```
PS C:\>Get-MsolDirSyncProvisioningError -ErrorCategory PropertyConflict -SearchString "PattiFul"
```

This command gets all objects with DirSyncProvisioningErrors with a PropertyConflict that uses the display name attribute starting with PattiFul.

### Example 56: Get a maximum number of provisioning errors5
```
PS C:\>Get-MsolDirSyncProvisioningError -ErrorCategory PropertyConflict -MaxResults 5
```

This command gets a maximum of five objects with DirSyncProvisioningErrors.

## PARAMETERS

### -All
Indicates that this cmdlet returns all provisioning errors.

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

### -ErrorCategory
Specifies the error category of the provisioning errors.
PropertyConflict is the only supported value and must be included.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyName
Specifies the property name of the tenant.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyValue
Specifies the property value for which this cmdlet searches the provisioning errors.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchString
Specifies a search string in which this cmdlet searches the list of provisioning errors.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SortField
Specifies the name field of the results that this cmdlet sorts by.
The acceptable values for this parameter are:

- DisplayName
- UserPrincipleName
- None

```yaml
Type: SortField
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SortDirection
Specifies the sort direction of the provisioning errors.
The acceptable values for this parameter are:

- Ascending
- Descending

```yaml
Type: SortDirection
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxResults
Specifies the maximum number of results that this cmdlet returns.

```yaml
Type: Int32
Parameter Sets: ListDirSyncProvisioningErrors__0
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Specifies the unique ID of the tenant to perform the operation on.
If you do not specify this parameter the cmdlet will use the ID of the current user.
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

[Get-MsolHasObjectsWithDirSyncProvisioningErrors](./Get-MsolHasObjectsWithDirSyncProvisioningErrors.md)


