---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADMSRoleDefinition

## SYNOPSIS
Gets information about role definitions in Azure AD.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSRoleDefinition [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADMSRoleDefinition [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSRoleDefinition -Id <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADMSRoleDefinition cmdlet gets information about role definitions in Azure Active Directory (Azure AD). To get a role definition, specify the Id parameter. Specify the SearchString or Filter parameter to find particular role definition.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-AzureADMSRoleDefinition

Id              : 690e93e9-da28-4b25-9d0d-2f0b4e6b2ff9
OdataType       :
Description     : SampleRoleDefinition1.
DisplayName     : SampleRoleDef
IsBuiltIn       : False
ResourceScopes  : {/}
IsEnabled       : True
RolePermissions : {class RolePermission {
                  AllowedResourceActions:
                  microsoft.directory/applications/create
                    Condition:
                  }
                  }
Id              : 1a327991-10cb-4266-877a-998fb4df78ec
OdataType       :
Description     :
DisplayName     : SampleRoleDefinition2.
IsBuiltIn       : False
ResourceScopes  : {/}
IsEnabled       : True
RolePermissions : {class RolePermission {
                  AllowedResourceActions:
                  microsoft.directory/applications/create
                    Condition:
                  }
                  }
TemplateId      : f2ef992c-3afb-46b9-b7cf-a126ee74c451
Version         :
```

### Example 2
```powershell
PS C:\> Get-AzureADMSRoleDefinition -Id 1a327991-10cb-4266-877a-998fb4df78ec

Id              : 1a327991-10cb-4266-877a-998fb4df78ec
OdataType       :
Description     :
DisplayName     : SampleRoleDefinition2.
IsBuiltIn       : False
ResourceScopes  : {/}
IsEnabled       : True
RolePermissions : {class RolePermission {
                  AllowedResourceActions:
                  microsoft.directory/applications/create
                    Condition:
                  }
                  }
TemplateId      : f2ef992c-3afb-46b9-b7cf-a126ee74c451
Version         :
```

### Example 3
```powershell
PS C:\> Get-AzureADMSRoleDefinition -Filter "startswith(displayName, 'Sample')"

Id              : 690e93e9-da28-4b25-9d0d-2f0b4e6b2ff9
OdataType       :
Description     : SampleRoleDefinition1.
DisplayName     : SampleRoleDef
IsBuiltIn       : False
ResourceScopes  : {/}
IsEnabled       : True
RolePermissions : {class RolePermission {
                  AllowedResourceActions:
                  microsoft.directory/applications/create
                    Condition:
                  }
                  }
Id              : 1a327991-10cb-4266-877a-998fb4df78ec
OdataType       :
Description     :
DisplayName     : SampleRoleDefinition2.
IsBuiltIn       : False
ResourceScopes  : {/}
IsEnabled       : True
RolePermissions : {class RolePermission {
                  AllowedResourceActions:
                  microsoft.directory/applications/create
                    Condition:
                  }
                  }
TemplateId      : f2ef992c-3afb-46b9-b7cf-a126ee74c451
Version         :
```

## PARAMETERS

### -Id
Specifies the ID of the role definition.

```yaml
Type: String
Parameter Sets: GetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -All
If true, return all role definitions. If false, return the number of objects specified by the Top parameter.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Top
Specifies the maximum number of records that this cmldet gets. The default value is 100.

```yaml
Type: Int32
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Filter
Specifies an oData v3.0 filter string to match a set of role definitions.

```yaml
Type: String
Parameter Sets: GetQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -SearchString
Specifies a search string.

```yaml
Type: String
Parameter Sets: GetVague
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### string
### bool?
### int?
### string
## OUTPUTS

### Microsoft.Open.MSGraph.Model.DirectoryRoleDefinition

## NOTES

See the [migration guide for Get-AzureADMSRoleDefinition](./migrate/Get-AzureADMSRoleDefinition.md) to the Microsoft Graph PowerShell.

## RELATED LINKS
