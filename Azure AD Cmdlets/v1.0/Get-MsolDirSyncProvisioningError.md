---
external help file: AzureADHelpMSOL.xml
online version: 942bef56-1526-4e08-b4a8-4b187c98bd77
schema: 2.0.0
---

# Get-MsolDirSyncProvisioningError

## SYNOPSIS
Checks for objects with synchronization provisioning errors in a tenant.

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-MsolDirSyncProvisioningError [-ErrorCategory <String>] [-PropertyName <String>] [-PropertyValue <String>]
 [-SearchString <String>] [-SortDirection] [-SortField] [-TenantId <Guid]>] [-All]
```

### UNNAMED_PARAMETER_SET_2
```
Get-MsolDirSyncProvisioningError [-ErrorCategory <String>] [-MaxResults <Int32>] [-PropertyName <String>]
 [-PropertyValue <String>] [-SearchString <String>] [-SortDirection] [-SortField] [-TenantId <Guid]>]
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
Parameter Sets: UNNAMED_PARAMETER_SET_1
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

### -MaxResults
Specifies the maximum number of results that this cmdlet returns.

```yaml
Type: Int32
Parameter Sets: UNNAMED_PARAMETER_SET_2
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

### -SortDirection
Specifies the sort direction of the provisioning errors.
The acceptable values for this parameter are:

-- Ascending
-- Descending

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Accepted values: Ascending, Descending

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SortField
Specifies the name field of the results that this cmdlet sorts by.
The acceptable values for this parameter are:

-- DisplayName
-- UserPrincipleName
-- None

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Accepted values: DisplayName, UserPrincipalName, None

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
Type: Guid]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True(ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-MsolHasObjectsWithDirSyncProvisioningErrors](942bef56-1526-4e08-b4a8-4b187c98bd77)

