---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.Custom.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-AzureADApplicationPasswordCredential

## SYNOPSIS
Creates a password credential for an application.

## SYNTAX

```
New-AzureADApplicationPasswordCredential -ObjectId <String> [-CustomKeyIdentifier <String>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Value <String>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>]
```

## DESCRIPTION
The New-AzureADApplicationPasswordCredential cmdlet creates a password credential for an application in Azure Active Directory (AD).

## EXAMPLES

### Example 1: Create a password credential
```
PS C:\>New-AzureADApplicationPasswordCredential -ObjectId "3ddd22e7-a150-4bb3-b100-e410dea1cb84"

CustomKeyIdentifier :
EndDate             : 9/28/2017 3:57:10 PM
KeyId               :
StartDate           : 9/28/2016 3:57:10 PM
Value               : ZJ0V1Yg4cp4eWIey9DrYspqVdX1pdvY437P/ueGxVLU=
```

## PARAMETERS

### -CustomKeyIdentifier
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -EndDate
@{Text=}

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

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

### -ObjectId
Specifies the ID of a user in Azure AD.

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

### -StartDate
@{Text=}

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureADApplicationPasswordCredential]()

[Remove-AzureADApplicationPasswordCredential]()

