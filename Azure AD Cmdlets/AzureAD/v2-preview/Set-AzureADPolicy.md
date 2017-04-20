---
external help file: Microsoft.Open.MS.GraphBeta.PowerShell.dll-Help.xml
ms.assetid: 1575D032-020F-4471-A408-2487C93940AF
online version: 
schema: 2.0.0
---

# Set-AzureADPolicy

## SYNOPSIS
Updates a policy.

## SYNTAX

```
Set-AzureADPolicy -Id <String> [-AlternativeIdentifier <String>]
 [-Definition <System.Collections.Generic.List`1[System.String]>] [-DisplayName <String>]
 [-IsOrganizationDefault <Boolean>]
 [-KeyCredentials <System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.KeyCredential]>]
 [-Type <String>] [<CommonParameters>]
```

## DESCRIPTION
The **Set-AzureADPolicy** cmdlet sets a policy in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Update a policy
```
PS C:\>Set-AzureADPolicy -ObjectId <object id of policy> -DisplayName <string>
```

This command updates the specified policy in Azure AD.

## PARAMETERS

### -AlternativeIdentifier
Specifies an alternative ID for the policy.

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

### -Definition
Specifies the array of stringfied JSON that contains all the rules of the policy. For example
*-Definition @("{"TokenLifetimePolicy":{"Version":1,"MaxInactiveTime":"20:00:00"}}")*.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
Specifies the display name.

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

### -IsOrganizationDefault
True if this policy is the organisational default

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

### -KeyCredentials
Specifies the key credentials.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.MSGraph.Model.KeyCredential]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Specifies the type of policy. For token lifetimes, use "TokenLifetimePolicy".

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

### -Id
The Id pf the policy for which you want to set values.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADPolicy](./Get-AzureADPolicy.md)

[New-AzureADPolicy](./New-AzureADPolicy.md)

[Remove-AzureADPolicy](./Remove-AzureADPolicy.md)
