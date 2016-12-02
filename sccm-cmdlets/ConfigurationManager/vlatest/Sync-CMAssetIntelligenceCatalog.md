---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834247
schema: 2.0.0
ms.assetid: 9C1E92FE-A79C-4759-8B60-CF71B83AEECB
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Sync-CMAssetIntelligenceCatalog.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Sync-CMAssetIntelligenceCatalog.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Sync-CMAssetIntelligenceCatalog

## SYNOPSIS
Synchronizes the Asset Intelligence catalog with System Center Online.

## SYNTAX

```
Sync-CMAssetIntelligenceCatalog [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Sync-CMAssetIntelligenceCatalog** cmdlet synchronizes the local Asset Intelligence catalog with System Center Online to retrieve the latest software title categorization.
The Asset Intelligence catalog contains categorization and identification information for software titles.
System Center Online accepts only one manual synchronization request in a 12-hour period.

Microsoft System Center Configuration Manager updates the asset Intelligence catalog by using the Asset Intelligence synchronization point site system role.
You must install an Asset Intelligence synchronization point site system role before you can synchronize the Asset Intelligence catalog with System Center Online.
You can use the Add-CMAssetIntelligenceSynchronizationPoint cmdlet to install an Asset Intelligence synchronization point site system role.

When you manually request catalog synchronization with System Center Online, it could take 15 minutes or longer to complete the synchronization process with System Center Online.

## EXAMPLES

### Example 1: Update the Asset Intelligence catalog
```
PS C:\>Sync-CMAssetIntelligenceCatalog -SiteCode "CM2" -SiteSystemServerName "Contoso-west02"
```

This command the updates the Asset Intelligence catalog on the System Center Configuration Manager site that has the site code CM2 on the site system server named Contoso-west02.

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMAssetIntelligenceSynchronizationPoint](xref:ConfigurationManager/vlatest/Add-CMAssetIntelligenceSynchronizationPoint.md)

[Get-CMAssetIntelligenceSynchronizationPoint](xref:ConfigurationManager/vlatest/Get-CMAssetIntelligenceSynchronizationPoint.md)

[Send-CMAssetIntelligenceCatalogUpdateRequest](xref:ConfigurationManager/vlatest/Send-CMAssetIntelligenceCatalogUpdateRequest.md)

[Set-CMAssetIntelligenceSynchronizationPoint](xref:ConfigurationManager/vlatest/Set-CMAssetIntelligenceSynchronizationPoint.md)


