---
external help file: AdminUI.PS.Collections-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833619
schema: 2.0.0
ms.assetid: 44F60651-6890-4A51-96C1-D2A835D7E24F
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDeviceCollection.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDeviceCollection.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMDeviceCollection

## SYNOPSIS
Gets one or more device collections in the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
Get-CMDeviceCollection [-Name <String>] [<CommonParameters>]
```

### ById
```
Get-CMDeviceCollection -Id <String> [<CommonParameters>]
```

### ByDPGroupName
```
Get-CMDeviceCollection -DistributionPointGroupName <String> [<CommonParameters>]
```

### ByDPGroupId
```
Get-CMDeviceCollection -DistributionPointGroupId <String> [<CommonParameters>]
```

### ByDPGroup
```
Get-CMDeviceCollection -DistributionPointGroup <IResultObject> [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceCollection** cmdlet retrieves collections that contain computers or mobile devices.
For more information about collections, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Get a device collection by using an ID
```
PS C:\>Get-CMDeviceCollection -CollectionId "9990000D"
```

This command gets the device collection that has the ID 9990000D.

## PARAMETERS

### -DistributionPointGroup


```yaml
Type: IResultObject
Parameter Sets: ByDPGroup
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupId


```yaml
Type: String
Parameter Sets: ByDPGroupId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName


```yaml
Type: String
Parameter Sets: ByDPGroupName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id


```yaml
Type: String
Parameter Sets: ById
Aliases: CollectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name


```yaml
Type: String
Parameter Sets: ByName
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

[Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433)

[New-CMDeviceCollection](xref:ConfigurationManager/vlatest/New-CMDeviceCollection.md)


