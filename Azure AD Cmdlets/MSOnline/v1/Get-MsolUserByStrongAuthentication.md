---
external help file: Microsoft.Online.Administration.Automation.PSModule.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: CC0818E5-CAAD-4066-A736-4E41CE9E7C27
---

# Get-MsolUserByStrongAuthentication

## SYNOPSIS

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

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

### -All
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


