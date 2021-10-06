---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Add-AzureADMSServicePrincipalDelegatedPermissionClassification

## SYNOPSIS
Add a classification for a delegated permission.

## SYNTAX

```
Add-AzureADMSServicePrincipalDelegatedPermissionClassification -ServicePrincipalId <String>
 -Classification <ClassificationEnum> -PermissionId <String> -PermissionName <String> [<CommonParameters>]
```

## DESCRIPTION
The Add-AzureADMSServicePrincipalDelegatedPermissionClassification cmdlet creates a delegated permission classification for the given permission on service principal.

## EXAMPLES

### Example 1: Create Delegated Permission Classification
```
PS C:\> Add-AzureADMSServicePrincipalDelegatedPermissionClassification -ServicePrincipalId "95f56359-0165-4f80-bffb-c89d06cf2c6f" -PermissionId "b340eb25-3456-403f-be2f-af7a0d370277" -Classification Low -PermissionName "User.ReadBasic.All"

Classification : Low
Id             : 5XBeIKarUkypdm0tRsSAQwE
PermissionId   : b340eb25-3456-403f-be2f-af7a0d370277
PermissionName : User.ReadBasic.All
```

This command creates a delegated permission classification for the given permission on the service principal.

## PARAMETERS

### -ServicePrincipalId
The unique identifier of a service principal object in Azure Active Directory.

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

### -PermissionId
The id for a delegated permission.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PermissionName
The name for a delegated permission.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Classification
The classification for a delegated permission.
This parameter can take one of the following values:

* "Low" - Specifies a classification for a permission as low impact.
* "Medium" - Specifies a classification for a permission as medium impact.
* "High" - Specifies a classification for a permission as high impact.

```yaml
Type: ClassificationEnum
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.Online.Administration.DelegatedPermissionClassification
## NOTES
## RELATED LINKS
