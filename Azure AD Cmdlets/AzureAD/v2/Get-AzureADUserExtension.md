---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADUserExtension

## SYNOPSIS

## SYNTAX

```
Get-AzureADUserExtension -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve extension attributes for a given user
```
$UserID = (get-azureaduser -top 1).ObjectId
Get-AzureADUserExtension -ObjectId $UserId

Key                            Value 
---                            ----- 
odata.metadata                 https://graph.windows.net/85b5ff1e-0402-400c-9e3c0f9e965325d1$metadata#directoryObjects/Microsoft.Director... 
odata.type                     Microsoft.DirectoryServices.User
deletionTimestamps
signInNames                    [] 
companyName 
creationType 
facsimileTelephoneNumber 
isCompromised 
refreshTokensValidFromDateTime 11/7/2016 10:11:09 PM 
showInAddressList
```

The examples retrieves all extension attributes that have a value assigned to them for the given user

## PARAMETERS

### -ObjectId
@{Text=}

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

