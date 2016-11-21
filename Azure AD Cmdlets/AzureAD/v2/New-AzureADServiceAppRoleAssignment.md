---
external help file: azuread.help.xml
online version: http://www.cloudidentity.com/blog/2013/09/12/active-directory-authentication-library-adal-v1-for-net-general-availability/
schema: 2.0.0
---

# New-AzureADServiceAppRoleAssignment

## SYNOPSIS
Assign a service principal to an application role.

## SYNTAX

```
New-AzureADServiceAppRoleAssignment -ObjectId <String> -Id <String> -PrincipalId <String> -ResourceId <String>
```

## DESCRIPTION

## EXAMPLES

### Example 1
```
$OwnerAppRole = new-object Microsoft.Open.AzureAD.Model.AppRole -Property @{IsEnabled = $True; Description = "Owner Role"; AllowedMemberTypes = "user"; DisplayName = "MyApp Owner"; Id = [guid]::NewGuid(); Value="MyAppOwner"} 
$MyApp = New-AzureADApplication -DisplayName "MyApp" -IdentifierUris "http://MyNewApp.contoso.com" -AppRoles $OwnerAppRole
$ServicePrincipal = new-azureadserviceprincipal -AccountEnabled $true -AppId $MyApp.Id -ApproleAsignmentRequired $True -DisplayName "MyApp"
$SP = get-azureadserviceprincipal -top 1
New-AzureADUserAppRoleAssignment -ObjectId $SP.ObjectId -PrincipalId $SP.ObjectId -ResourceId $ServicePrincipal.ObjectId -Id $Role.Id
```

## PARAMETERS

### -ObjectId
The unique idenfier of an service principal in Azure Active Directory

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
@{Text=}

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
@{Text=}

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
@{Text=}

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

