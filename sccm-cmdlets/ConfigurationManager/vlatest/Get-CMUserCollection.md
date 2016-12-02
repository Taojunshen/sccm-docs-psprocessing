---
external help file: AdminUI.PS.Collections-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833980
schema: 2.0.0
ms.assetid: 8AD90CCA-3F40-4D64-8FD9-C9028A0E15E7
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMUserCollection.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMUserCollection.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMUserCollection

## SYNOPSIS
Gets one or more user collections in the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
Get-CMUserCollection [-Name <String>] [<CommonParameters>]
```

### ById
```
Get-CMUserCollection -Id <String> [<CommonParameters>]
```

### ByDPGroupName
```
Get-CMUserCollection -DistributionPointGroupName <String> [<CommonParameters>]
```

### ByDPGroupId
```
Get-CMUserCollection -DistributionPointGroupId <String> [<CommonParameters>]
```

### ByDPGroup
```
Get-CMUserCollection -DistributionPointGroup <IResultObject> [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserCollection** cmdlet retrieves collections that contain users in Microsoft System Center Configuration Manager.
For more information about collections, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Get a user collection
```
PS C:\>Get-CMUserCollection -CollectionId "9990000D"
```

This command gets the user collection that has the ID 9990000D.

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

[New-CMUserCollection](xref:ConfigurationManager/vlatest/New-CMUserCollection.md)


