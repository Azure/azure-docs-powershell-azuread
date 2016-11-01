---
external help file: Microsoft.Open.AzureAD16.Graph.PowerShell.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 0DF2C468-53D8-4BC5-AFC8-7E8EDF38C347
---

# New-AzureADDevice

## SYNOPSIS
Create a new device in Azure Active Directory

## SYNTAX

```
New-AzureADDevice [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 -AccountEnabled <Boolean>
 -AlternativeSecurityIds <System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AlternativeSecurityId]>
 [-ApproximateLastLogonTimeStamp <DateTime>] -DeviceId <String> [-DeviceObjectVersion <Int32>]
 -DeviceOSType <String> -DeviceOSVersion <String>
 [-DevicePhysicalIds <System.Collections.Generic.List`1[System.String]>] -DisplayName <String>
 [-IsCompliant <Boolean>] [-IsManaged <Boolean>] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### -------------------------- EXAMPLE 1 --------------------------
```
PS C:\>New-AzureADDevice -AccountEnabled $true -DisplayName "My new device" -AlternativeSecurityIds $altsecid -DeviceId $guid -DeviceOSType "OS/2" -DeviceOSVersion "9.3"
```

Output:

ObjectId                             DeviceId                             DisplayName
--------                             --------                             -----------
99a1915d-298f-42d1-93ae-71646b85e2fa 5547679b-809d-4e2c-9820-3c4401a573a8 My new device

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

### -AccountEnabled
@{Text=}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AlternativeSecurityIds
@{Text=}

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Open.AzureAD.Model.AlternativeSecurityId]
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
Type: DateTime
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
Type: Int32
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

### -DevicePhysicalIds
@{Text=}

```yaml
Type: System.Collections.Generic.List`1[System.String]
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
@{Text=}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsManaged
@{Text=}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


