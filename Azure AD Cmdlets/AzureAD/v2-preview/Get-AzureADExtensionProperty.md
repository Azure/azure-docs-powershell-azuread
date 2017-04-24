---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADExtensionProperty

## SYNOPSIS
Gets  extension properties registered with Azure AD.

## SYNTAX

```
Get-AzureADExtensionProperty [-IsSyncedFromOnPremises <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-AzureADExtensionProperty** cmdlet gets a collection that contains the extension properties registered with Azure Active Directory (Azure AD) through Azure AD Connect. 
You can get extension properties that are synced with on-premises Azure AD, those that are not synced with on-premises Azure AD, or both types. 

## EXAMPLES

### Example 1: Get extension properties synced from on-premises Azure AD
```
PS C:\> Get-AzureADExtensionProperty -IsSyncedFromOnPremises $True

ObjectId                             Name                                                          TargetObjects
--------                             ----                                                          -------------
b3c7b2c2-bb9a-4e30-a9fc-46adbe8c0899 extension_6e151e1a9cf44f8689a410023ac39235_weather            {User}
05af194f-1068-4539-83c9-06e03a1a1f44 extension_6e151e1a9cf44f8689a410023ac39235_extension_location {User}
9bf6f631-e6a6-41d1-b0a3-777f2acea2d1 extension_ed192e9284d44baf997d1e190a81f28e_extension_4A3UwDDC {User}
```

This command gets extension properties that have been synced from on-premises Azure AD. 

## PARAMETERS

### -IsSyncedFromOnPremises
Specifies whether this cmdlet gets extension properties that are synced or not synced.
- $True. Get extension properties that are synced from the on-premises Azure AD.
- $False. Get extension properties that are not synced from the on-premises Azure AD.
- No value. Get all extension properties.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

