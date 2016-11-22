---
external help file: azuread.help.xml
online version: http://www.cloudidentity.com/blog/2013/09/12/active-directory-authentication-library-adal-v1-for-net-general-availability/
schema: 2.0.0
---

# New-AzureADApplicationKeyCredential

## SYNOPSIS
Create a new key credential for an application

## SYNTAX

```
New-AzureADApplicationKeyCredential -ObjectId <String> [-CustomKeyIdentifier <String>]
 [-StartDate <Nullable`1[DateTime]>] [-EndDate <Nullable`1[DateTime]>] [-Type <Nullable`1[KeyType]>]
 [-Usage <Nullable`1[KeyUsage]>] [-Value <String>]
```

## DESCRIPTION

## EXAMPLES

### This example shows how to create a new application key credential
```
$AppID = (Get-AzureADApplication -Top 1).objectid
New-AzureADApplicationKeyCredential -ObjectId $AppId -CustomKeyIdentifier "Test" -StartDate "11/7/2016" -Type "Symmetric" -Usage "Sign" -Value "123"

Output:

CustomKeyIdentifier : {84, 101, 115, 116}
EndDate             : 11/7/2017 12:00:00 AM
KeyId               : a5845538-3f67-402d-a03e-36d768f1441e
StartDate           : 11/7/2016 12:00:00 AM
Type                : Symmetric
Usage               : Sign
Value               : {49, 50, 51}
```

### This example shows how to use a certificate to add a new Application key credential
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2 #create a new certificate object
$cer.Import("C:\Users\nibansa\Desktop\abc.cer") #Path and filename of the certificate you want to use
$bin = $cer.GetRawCertData()
$base64Value = [System.Convert]::ToBase64String($bin)
$bin = $cer.GetCertHash()
$base64Thumbprint = [System.Convert]::ToBase64String($bin)
$keyid = [System.Guid]::NewGuid().ToString() 

New-AzureADApplicationKeyCredential -ObjectId 009d786a-3503-4217-b8ab-db03d71c179a -CustomKeyIdentifier  $base64Thumbprint  -Type AsymmetricX509Cert -Usage Verify -Value $base64Value  -StartDate $cer.GetEffectiveDateString() -EndDate cer.GetExpirationDateString()
```

## PARAMETERS

### -ObjectId
The unique identifier of an application in Azure Active Directory

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
The date and time at which the credential expires

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

[This cmdlet uses the adal library in azure Active Directory. To learn more about ADAL, please follow this link:](http://www.cloudidentity.com/blog/2013/09/12/active-directory-authentication-library-adal-v1-for-net-general-availability/)
