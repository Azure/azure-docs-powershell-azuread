---
external help file: azuread.help.xml
online version: http://www.cloudidentity.com/blog/2013/09/12/active-directory-authentication-library-adal-v1-for-net-general-availability/
schema: 2.0.0
---

# New-AzureADGroupAppRoleAssignment

## SYNOPSIS
Assign a group of users to an application role.

## SYNTAX

```
New-AzureADGroupAppRoleAssignment -ObjectId <String> -Id <String> -PrincipalId <String> -ResourceId <String>
```

## DESCRIPTION

## EXAMPLES

### Example 1
```
$OwnerAppRole = new-object Microsoft.Open.AzureAD.Model.AppRole -Property @{IsEnabled = $True; Description = "Owner Role"; AllowedMemberTypes = "user"; DisplayName = "MyApp Owner"; Id = [guid]::NewGuid(); Value="MyAppOwner"} 
$MyApp = New-AzureADApplication -DisplayName "MyApp" -IdentifierUris "http://MyNewApp.contoso.com" -AppRoles $OwnerAppRole
$ServicePrincipal = new-azureadserviceprincipal -AccountEnabled $true -AppId $MyApp.Id -ApproleAsignmentRequired $True -DisplayName "MyApp"
$Group = get-azureadgroup -top 1
New-AzureADUserAppRoleAssignment -ObjectId $Group.ObjectId -PrincipalId $Group.ObjectId -ResourceId $ServicePrincipal.ObjectId -Id $Role.Id
```

## PARAMETERS

### -ObjectId
The unique identifier of a group in Azure Active Directory (ObjectId)

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Id
The role id that was assigned to the principal.
This role must be declared by the target resource application resourceId in its appRoles property.
Where the resource does not declare any permissions, a default id (zero GUID) must be specified.

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

### -PrincipalId
The unique identifier (objectId) for the principal being granted the access.

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

### -ResourceId
The unique identifier (objectId) for the target resource (service principal) for which the assignment was made

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

