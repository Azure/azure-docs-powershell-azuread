---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# Remove-AzureADApplicationPasswordCredential

## SYNOPSIS
Removes a password credential from an application.

## SYNTAX

```
Remove-AzureADApplicationPasswordCredential -ObjectId <String> -KeyId <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Remove-AzureADApplicationPasswordCredential cmdlet removes a password credential from an application in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Remove an application password credential
```
PS C:\> $AppID = (Get-AzureADApplication -Top 1).objectId
PS C:\> $KeyIDs = Get-AzureADApplicationPasswordCredential -ObjectId $AppId
PS C:\> Remove-AzureADApplicationPasswordCredential -ObjectId $AppId -KeyId $KeyIds[0].KeyId
```

The first command gets the ID of an application by using the Get-AzureADApplication (./Get-AzureADApplication.md)cmdlet, and then stores it in the $AppID variable.

The second command gets the password credential for the application identified by $AppID by using the Get-AzureADApplicationPasswordCredential (./ Get-AzureADApplicationPasswordCredential.md)cmdlet. 
The command stores it in the $KeyId variable.

The final command removes the application password credential for the application identified by $AppID.

## PARAMETERS

### -InformationAction
Specifies how this cmdlet responds to an information event.

The acceptable values for this parameter are:

- Continue
- Ignore
- Inquire
- SilentlyContinue
- Stop
- Suspend

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Specifies an information variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
@{Text=}

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

### -ObjectId
Specifies the ID of the application in Azure AD.

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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADApplication]()

[Get-AzureADApplicationPasswordCredential]()

[Remove-AzureADApplicationPasswordCredential]()

