---
external help file: azuread.help.xml
online version: http://www.cloudidentity.com/blog/2013/09/12/active-directory-authentication-library-adal-v1-for-net-general-availability/
schema: 2.0.0
---

# New-AzureADDevice

## SYNOPSIS
Create a new device in Azure Active Directory

## SYNTAX

```
New-AzureADDevice -AccountEnabled <Nullable`1[Boolean]> -AlternativeSecurityIds <List`1[AlternativeSecurityId]>
 [-ApproximateLastLogonTimeStamp <Nullable`1[DateTime]>] -DeviceId <String>
 [-DeviceObjectVersion <Nullable`1[Int32]>] -DeviceOSType <String> -DeviceOSVersion <String>
 [-DevicePhysicalIds <List`1[String]>] -DisplayName <String> [-IsCompliant <Nullable`1[Boolean]>]
 [-IsManaged <Nullable`1[Boolean]>]
```

## DESCRIPTION

## EXAMPLES

### Create a new device object
```
New-AzureADDevice -AccountEnabled $true -DisplayName "My new device" -AlternativeSecurityIds $altsecid -DeviceId $guid -DeviceOSType "OS/2" -DeviceOSVersion "9.3"

Output:


ObjectId                             DeviceId                             DisplayName 
--------                             --------                             ----------- 
99a1915d-298f-42d1-93ae-71646b85e2fa 5547679b-809d-4e2c-9820-3c4401a573a8 My new device
```

## PARAMETERS

### -AccountEnabled
@{Text=}

```yaml
Type: Nullable`1[Boolean]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AlternativeSecurityIds
Contains a collection of alternative security ID's associated with a device.

```yaml
Type: List`1[AlternativeSecurityId]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApproximateLastLogonTimeStamp
@{Text=}

```yaml
Type: Nullable`1[DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceId
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceObjectVersion
@{Text=}

```yaml
Type: Nullable`1[Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceOSType
The Operating System type of the new device

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceOSVersion
The version of the operating system on the device

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DevicePhysicalIds
@{Text=}

```yaml
Type: List`1[String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
The display name of the new device

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsCompliant
true if the device complies with Mobile Device Management (MDM) policies; otherwise, false.

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

### -IsManaged
true if the device is managed by a Mobile Device Management (MDM) app such as Intune; otherwise, false.

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

