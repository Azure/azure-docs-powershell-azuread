---
external help file: Microsoft.Open.MS.GraphV10.PowerShell.dll-Help.xml
Module Name: AzureAD
online version:
schema: 2.0.0
---

# Get-AzureADMSRoleAssignment

## SYNOPSIS
Gets information about role assignments in Azure AD.

## SYNTAX

### GetQuery (Default)
```
Get-AzureADMSRoleAssignment [-All <Boolean>] [-Top <Int32>] [-Filter <String>] [<CommonParameters>]
```

### GetVague
```
Get-AzureADMSRoleAssignment [-SearchString <String>] [-All <Boolean>] [<CommonParameters>]
```

### GetById
```
Get-AzureADMSRoleAssignment -Id <String> [-All <Boolean>] [<CommonParameters>]
```

## DESCRIPTION
The Get-AzureADMSRoleAssignment cmdlet gets information about role assignments in Azure Active Directory (Azure AD). To get a role assignment, specify the Id parameter. Specify the SearchString or Filter parameter to find a particular role assignment.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-AzureADMSRoleAssignment -Filter "roleDefinitionId eq '62e90394-69f5-4237-9190-012177145e34'"

RoleDefinitionId                     PrincipalId                          ResourceScope Id
----------------                     -----------                          ------------- --
62e90394-69f5-4237-9190-012177145e34 69584002-b4d1-4055-9c94-320542efd653 /             lAPpYvVpN0KRkAEhdxReEAJAWGnRqAVAnJQyBBLv1lM-1
62e90394-69f5-4237-9190-012177145e34 3f5e48d2-6bf4-4bf3-a4ff-8bbd9f23ed0b /             lAPpYvVpN0KRkAEhdxReENJPEj_0a_NLpP-LvZ8D7Qs-1
```

### Example 2
```powershell
PS C:\> Get-AzureADMSRoleAssignment -Filter "principalId eq '69584002-b4d1-4055-9c94-320542efd653'"

RoleDefinitionId                     PrincipalId                          ResourceScope Id
----------------                     -----------                          ------------- --
89c55b63-78c3-478b-b79e-074d0e87269e 69584002-b4d1-4055-9c94-320542efd653 /             Y1vFBcN4i0e3ngdNDocmngJAWGnRtGDAnJQyBBLv1lM-1
62e90394-69f5-4237-9190-012177145e34 69584002-b4d1-4055-9c94-320542efd653 /             lAPpYvVpN0KRkAEhdxReEAJAWGnRtGDAnJQyBBLv1lM-1
eb1d8c90-acf5-460d-8424-c1f1a6fbdb85 69584002-b4d1-4055-9c94-320542efd653 /             NIwd6_WsDUaEJMHxpvvbhQJAWGnRtGDAnJQyBBLv1lM-1
```

## PARAMETERS

### -Id
Specifies the ID of the role assignment.

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
If true, return all role assignments. If false, return the number of objects specified by the Top parameter.

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
Specifies an oData v3.0 filter string to match a set of role assignments.

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

### Microsoft.Open.MSGraph.Model.DirectoryRoleAssignment
## NOTES

## RELATED LINKS
