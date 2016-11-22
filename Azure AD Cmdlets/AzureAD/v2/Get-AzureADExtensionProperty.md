---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADExtensionProperty

## SYNOPSIS
A collection that contains the extension properties registered with the directory.

## SYNTAX

```
Get-AzureADExtensionProperty [-IsSyncedFromOnPremises <Nullable`1[Boolean]>]
```

## DESCRIPTION
A collection that contains the extension properties registered with the directory.

## EXAMPLES

### Get all ExtensionProperties that have been synced from on premises AD throuhg Azure AD Connect
```
Get-AzureADExtensionProperty -IsSyncedFromOnPremises $true

ObjectId                             Name                                                          TargetObjects
--------                             ----                                                          -------------
b3c7b2c2-bb9a-4e30-a9fc-46adbe8c0899 extension_6e151e1a9cf44f8689a410023ac39235_weather            {User}
05af194f-1068-4539-83c9-06e03a1a1f44 extension_6e151e1a9cf44f8689a410023ac39235_extension_location {User}
9bf6f631-e6a6-41d1-b0a3-777f2acea2d1 extension_ed192e9284d44baf997d1e190a81f28e_extension_4A3UwDDC {User}
```

Note: Specifying the IsSyncedFromOnPremises parameter will return only extension properties that have been synced from on-premises

## PARAMETERS

### -IsSyncedFromOnPremises
true to specify that only extension properties that are synced from the on-premises directory should be returned; false to specify that only extension properties that are not synced from the on-premises directory should be returned.
If the parameter is omitted then all extension properties (both synced and non-synced) are returned.

```yaml
Type: Nullable`1[Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

