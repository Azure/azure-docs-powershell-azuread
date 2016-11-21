---
external help file: azuread.help.xml
online version: http://www.cloudidentity.com/blog/2013/09/12/active-directory-authentication-library-adal-v1-for-net-general-availability/
schema: 2.0.0
---

# New-AzureADServicePrincipalKeyCredential

## SYNOPSIS
Create a new key credential for a service principal

## SYNTAX

```
New-AzureADServicePrincipalKeyCredential -ObjectId <String> [-CustomKeyIdentifier <String>]
 [-StartDate <Nullable`1[DateTime]>] [-EndDate <Nullable`1[DateTime]>] [-Type <Nullable`1[KeyType]>]
 [-Usage <Nullable`1[KeyUsage]>] [-Value <String>]
```

## DESCRIPTION

## EXAMPLES

### EXAMPLE 1
```
New-AzureADServicePrincipalKeyCredential
```

## PARAMETERS

### -ObjectId
The object Id of the service principal

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

### -CustomKeyIdentifier
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -StartDate
The date and time at which the credential becomes valid

```yaml
Type: Nullable`1[DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -EndDate
The date and time at which the credential expires.

```yaml
Type: Nullable`1[DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Type
The type of key credential; for example, "Symmetric".

```yaml
Type: Nullable`1[KeyType]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Usage
A string that describes the purpose for which the key can be used; for example, "Verify".

```yaml
Type: Nullable`1[KeyUsage]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Value
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

