---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version:
schema: 2.0.0
ms.assetid: CC0818E5-CAAD-4066-A736-4E41CE9E7C27
ms.reviewer: rodejo
ms.custom: iamfeature=PowerShell
---

# Get-MsolUserByStrongAuthentication

## SYNOPSIS
Gets users based on strong authentication type.

## SYNTAX

### ListUsersByStrongAuthentication__0 (Default)
```
Get-MsolUserByStrongAuthentication [-RoleObjectId <Guid>] [-Requirements <StrongAuthenticationRequirement[]>]
 [-RequirementUnsetOnly] [-SearchString <String>] [-MaxResults <Int32>] [-TenantId <Guid>] [<CommonParameters>]
```

### All__0
```
Get-MsolUserByStrongAuthentication [-RoleObjectId <Guid>] [-Requirements <StrongAuthenticationRequirement[]>]
 [-RequirementUnsetOnly] [-SearchString <String>] [-All] [-TenantId <Guid>] [<CommonParameters>]
```

## DESCRIPTION
The **Get-MsolUserByStrongAuthentication** cmdlet gets users in Azure Active Directory based on strong authentication type.

## EXAMPLES


## PARAMETERS

### -All
Indicates that this cmdlet returns all results that it finds.
Do not specify this parameter and the _MaxResults_ parameter.

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

### -MaxResults
Specifies the maximum number of results that this cmdlet returns.

```yaml
Type: Int32
Parameter Sets: ListUsersByStrongAuthentication__0
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequirementUnsetOnly
Indicates that this cmdlet gets only users that have no strong authentication requirement.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Requirements
Specifies an array of strong authentication requirements for which this cmdlet gets users.

```yaml
Type: StrongAuthenticationRequirement[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleObjectId
Specifies the unique object ID of the role for which this cmdlet gets users.


```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SearchString
Specifies a string.
This cmdlet returns users that start with this string.

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

### -TenantId
Specifies the unique ID of the tenant on which to perform the operation.
The default value is the tenant of the current user.
This parameter applies only to partner users.

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
[Get-MsolUser](./Get-MsolUser.md)
