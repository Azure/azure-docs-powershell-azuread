---
external help file: azuread.help.xml
online version: https://blogs.technet.microsoft.com/enterprisemobility/2016/07/18/azuread-certificate-based-authentication-for-ios-and-android-now-in-preview/
schema: 2.0.0
---

# Set-AzureADGroup

## SYNOPSIS
Updates a specific group in Azure Active Directory

## SYNTAX

```
Set-AzureADGroup -ObjectId <String> [-Description <String>] [-DisplayName <String>]
 [-MailEnabled <Nullable`1[Boolean]>] [-MailNickName <String>] [-SecurityEnabled <Nullable`1[Boolean]>]
```

## DESCRIPTION

## EXAMPLES

### Set a new description for a group
```
$GroupId = (Get-AzureADGroup -Top 1).ObjectId
Set-AzureADGroup -ObjectId $GroupId -Description "This is my new group"
```

## PARAMETERS

### -ObjectId
The unique identifier of a group in Azure Active Directory (ObjectId)

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

### -Description
@{Text=}

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

### -DisplayName
@{Text=}

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

### -MailEnabled
@{Text=}

```yaml
Type: Nullable`1[Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MailNickName
@{Text=}

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

### -SecurityEnabled
@{Text=}

```yaml
Type: Nullable`1[Boolean]
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

## RELATED LINKS

