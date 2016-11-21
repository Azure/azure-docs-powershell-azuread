---
external help file: azuread.help.xml
online version: 
schema: 2.0.0
---

# Get-AzureADServicePrincipal

## SYNOPSIS
Get a service principal by objectId

## SYNTAX

### UNNAMED_PARAMETER_SET_1
```
Get-AzureADServicePrincipal [-Top <Nullable`1[Int32]>] [-Filter <String>]
```

### UNNAMED_PARAMETER_SET_2
```
Get-AzureADServicePrincipal [-SearchString <String>]
```

### UNNAMED_PARAMETER_SET_3
```
Get-AzureADServicePrincipal -ObjectId <String>
```

## DESCRIPTION

## EXAMPLES

### Retrieve all Service Principal objects from the directory
```
Get-AzureADServicePrincipal

Output:

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
00221b6f-4387-4f3f-aa85-34316ad7f956 e5e29b8a-85d9-41ea-b8d1-2162bd004528 Tenant Schema Extension App
012f6450-15be-4e45-b8b4-e630f0fb70fe 00000005-0000-0ff1-ce00-000000000000 Microsoft.YammerEnterprise
06ab01eb-3e77-4d14-ae31-322c7730a65b 09abbdfd-ed23-44ee-a2d9-a627aa1c90f3 ProjectWorkManagement
092aaf41-23e8-46eb-8c3d-fc0ee91cc62f 507bc9da-c4e2-40cb-96a7-ac90df92685c Office365Reports
0ac66e69-5502-4406-a294-6dedeadc8cab 2cf9eb86-36b5-49dc-86ae-9a63135dfa8c AzureTrafficManagerandDNS
0c0a6d9d-48c0-4aa7-b484-4e46f77d8ed9 0f698dd4-f011-4d23-a33e-b36416dcb1e6 Microsoft.OfficeClientService
0cbef08e-a4b5-4dd9-865e-8f521c1c5fb4 0469d4cd-df37-4d93-8a61-f8c75b809164 Microsoft Policy Administration Service
0ea80ff0-a9ea-43b6-b876-d5989efd8228 00000009-0000-0000-c000-000000000000 Microsoft Power BI Reporting and Analytics
```

### Retrieve a Service Principal by it's Object Id
```
$ServicePrincipalId = (Get-AzureADServicePrincipal -Top 1).ObjectId
Get-AzureADServicePrincipal $ServicePrincipalId

ObjectId                             AppId                                DisplayName
--------                             -----                                -----------
00221b6f-4387-4f3f-aa85-34316ad7f956 e5e29b8a-85d9-41ea-b8d1-2162bd004528 Tenant Schema Extension App
```

## PARAMETERS

### -Top
The maximum number of records to return.
If no value is provided, 100 records are returned

```yaml
Type: Nullable`1[Int32]
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -Filter
The filter parameter can be used to filter returned objects of a cmdlet using an Odata filter statement.
An example would be 

Get-AzureADServicePrincipal -Filter "DisplayName eq 'TestName'"

which would only return ServicePrincipal objects for which the DisplayName equals "TestName".

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_1
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -SearchString
The SearchString parameter allows you to search for specific objects.
This includes the DisplayName and Description attribute as well as addtional string attributes for an object

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_2
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue, ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
The unique idenfier of an service principal in Azure Active Directory

```yaml
Type: String
Parameter Sets: UNNAMED_PARAMETER_SET_3
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

