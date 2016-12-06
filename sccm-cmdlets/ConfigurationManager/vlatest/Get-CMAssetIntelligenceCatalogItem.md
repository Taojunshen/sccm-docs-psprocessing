---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834110
schema: 2.0.0
ms.assetid: C36B760A-9281-44FA-A120-B4D57F9BD142
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAssetIntelligenceCatalogItem.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAssetIntelligenceCatalogItem.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMAssetIntelligenceCatalogItem

## SYNOPSIS
Gets an item from the Asset Intelligence catalog.

## SYNTAX

### SearchByName (Default)
```
Get-CMAssetIntelligenceCatalogItem [-CategoryName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAssetIntelligenceCatalogItem -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAssetIntelligenceCatalogItem** cmdlet gets software categories, software families, and custom software labels from the Asset Intelligence catalog in Microsoft System Center Configuration Manager.

The Asset Intelligence catalog contains categorization and identification information for software titles.
The catalog includes predefined categories and families.
Predefined items cannot be modified.
In addition to predefined software categories and software families, you can create custom categories and families.
You can also create custom software labels.

For more information about the Asset Intelligence catalog, see [Introduction to Asset Intelligence in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=262650) on TechNet.

## EXAMPLES

### Example 1: Get catalog items by category name
```
PS C:\>Get-CMAssetIntelligenceCatalogItem -CategoryName "Browsers"
```

This command gets Asset Intelligence catalog items by category name.

### Example 2: Get catalog items by category ID
```
PS C:\>Get-CMAssetIntelligenceCatalogItem -Id "1211"
```

This command gets Asset Intelligence catalog items by category ID.

## PARAMETERS

### -CategoryName
Specifies the name of a category, family, or label in the Asset Intelligence catalog.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
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

### -Id
Specifies an array of IDs of asset intelligence catalog items.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CategoryId
Required: True
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

[New-CMAssetIntelligenceCatalogItem](xref:ConfigurationManager/vlatest/New-CMAssetIntelligenceCatalogItem.md)

[Remove-CMAssetIntelligenceCatalogItem](xref:ConfigurationManager/vlatest/Remove-CMAssetIntelligenceCatalogItem.md)

[Set-CMAssetIntelligenceCatalogItem](xref:ConfigurationManager/vlatest/Set-CMAssetIntelligenceCatalogItem.md)


