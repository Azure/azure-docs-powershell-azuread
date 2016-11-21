---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADApplication

## SYNOPSIS
Delete an application by objectId.

## SYNTAX

```
Remove-AzureADApplication -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Remove an application form the directory
```
$App = get-azureadapplication -top 1
Remove-AzureADApplication -ObjectId $App.ObjectId
```

## PARAMETERS

### -ObjectId
The unique idenfier of an application in Azure Active Directory

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

