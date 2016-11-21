---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Select-AzureADGroupIdsContactIsMemberOf

## SYNOPSIS
From a list of groups Ids select those that the contact is a member of.

## SYNTAX

```
Select-AzureADGroupIdsContactIsMemberOf -ObjectId <String>
 -GroupIdsForMembershipCheck <GroupIdsForMembershipCheck>
```

## DESCRIPTION

## EXAMPLES

### Get the group membership of a group for a given contact
```
$Groups = New-Object Microsoft.Open.AzureAD.Model.GroupIdsForMembershipCheck
$groups.GroupIds = (Get-AzureADGroup -Top 1).ObjectId
$ContactID = (Get-azureadContact -top 1).ObjectId
Select-AzureADGroupIdsContactIsMemberOf  -ObjectId $GroupId -GroupIdsForMembershipCheck $Groups

OdataMetadata                                                                                   Value
-------------                                                                                   -----
https://graph.windows.net/85b5ff1e-0402-400c-9e3c-0f9e965325d1/$metadata#Collection(Edm.String) {093fc0e2-1d6e-4a1b-9bf8-effa0196f1f7}
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

### -GroupIdsForMembershipCheck
A list of groups object ids.

```yaml
Type: GroupIdsForMembershipCheck
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

