---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834246
schema: 2.0.0
ms.assetid: 3A9B87BA-CB44-4055-812E-BFC3DF7A8018
updated_at: 3/14/2017 5:56 PM
ms.date: 3/14/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCollectionSetting.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCollectionSetting.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/ccf61168e86d4120cdc26f0ffd9b7560e92d36b5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCollectionSetting.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMCollectionSetting

## SYNOPSIS
Gets the settings for a collection.

## SYNTAX

### ByValue (Default)
```
Get-CMCollectionSetting [-CollectionType <CollectionType>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollectionSetting -CollectionId <String> [-CollectionType <CollectionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
Get-CMCollectionSetting -CollectionName <String> [-CollectionType <CollectionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCollectionSetting** cmdlet gets the settings for a collection.

## EXAMPLES

### Example 1: Get the settings for a collection by using the pipeline
```
PS C:\> Get-CMCollection -Id MP500014 | Get-CMCollectionSetting -CollectionType Device
```

This command gets the collection object with the ID of MP500014 and uses the pipeline operator to pass the object to **Get-CMCollectionSetting**, which gets the device collection settings for the collection object.

### Example 2: Get the settings for a collection by name
```
PS C:\> Get-CMCollectionSetting -CollectionName "Devicecol1"
```

This command gets the collection settings for the device collection named Devicecol1.

## PARAMETERS

### -CollectionId
Specifies the ID of a collection.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a collection.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionType
Specifies the collection type.
A collection type of User is 1.
A collection type of Device is 2.
You can specify the type by using either User or Device, or 1 or 2.

```yaml
Type: CollectionType
Parameter Sets: (All)
Aliases: 
Accepted values: User, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a collection object.
To obtain a collection object, use the Get-CMCollection, Get-CMDeviceCollection or Get-CMUserCollection cmdlets.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCollection](xref:ConfigurationManager/vlatest/Get-CMCollection.md)

[Get-CMDeviceCollection](xref:ConfigurationManager/vlatest/Get-CMDeviceCollection.md)

[Get-CMUserCollection](xref:ConfigurationManager/vlatest/Get-CMUserCollection.md)


