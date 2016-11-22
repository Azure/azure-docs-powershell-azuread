---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADApplicationPasswordCredential

## SYNOPSIS
Remove a password credential from an application

## SYNTAX

```
Remove-AzureADApplicationPasswordCredential -ObjectId <String> -KeyId <String>
```

## DESCRIPTION

## EXAMPLES

### Removes an application password credentail
```
$AppID = (Get-AzureADApplication -top 1).objectId
$KeyIDs = Get-AzureADApplicationPasswordCredential -ObjectId $AppId
Remove-AzureADApplicationPasswordCredential -ObjectId $AppId -KeyId $KeyIds[0].KeyId
```

## PARAMETERS

### -ObjectId
The unique identifier of the application in Azure Active Directory

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

### -KeyId
The KeyId of the password credential that is removed

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

