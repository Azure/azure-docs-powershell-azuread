---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Remove-AzureADContactManager

## SYNOPSIS
Deletes the contact's manager in Azure Active Directory

## SYNTAX

```
Remove-AzureADContactManager -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Removes the manager from a contact
```
$Contact = Get-AzureADContact -top 1
Remove-AzureADContactManager -ObjectId $Contact.ObjectId
```

## PARAMETERS

### -ObjectId
The unique identifier of a contact in Azure Active Directory (ObjectId)

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

