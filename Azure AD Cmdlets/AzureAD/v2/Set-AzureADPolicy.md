---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Set-AzureADPolicy

## SYNOPSIS

## SYNTAX

```
Set-AzureADPolicy -ObjectId <String> [-AlternativeIdentifier <String>]
 [-Definition <System.Collections.Generic.List`1[System.String]>] [-DisplayName <String>]
 [-IsTenantDefault <Boolean>]
 [-KeyCredentials <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.KeyCredential]>]
 [-Type <String>]
```

## DESCRIPTION

## EXAMPLES

### EXAMPLE 1
```
Set-AzureADPolicy -ObjectId <object id of policy> -DisplayName <string>
```

## PARAMETERS

### -ObjectId
The object Id of the Policy

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

### -AlternativeIdentifier
\[Optional\] Sets an alternative id to the policy

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
\[Optional\] The array of strinfied JSON that contains all the rules of the policy, e.g.
-Definition @("{"TokenLifetimePolicy":{"Version":1,"MaxInactiveTime":"20:00:00"}}")

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
String of the policy name

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

### -IsTenantDefault
\[Optional\] If true sets the policy as tenant's default policy, if false does nothing

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
@{Text=}

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.KeyCredential]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
\[Optional\] The type of policy, for token lifetimes always use "TokenLifetimePolicy"

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

## INPUTS

## OUTPUTS

## NOTES
Please note that this cmdlet is currently in Public Preview.
While a cmdlet is in Public Preview we may still need to make changes to the cmdlet which could potentially cause unexpected effects.
We discourage customers from using this cmdlet in a production environment.

## RELATED LINKS

