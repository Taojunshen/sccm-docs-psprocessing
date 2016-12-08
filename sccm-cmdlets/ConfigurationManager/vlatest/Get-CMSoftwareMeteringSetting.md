---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833895
schema: 2.0.0
ms.assetid: 9DD38462-DD7F-42F1-956D-43142B02AA7D
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareMeteringSetting.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareMeteringSetting.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMSoftwareMeteringSetting

## SYNOPSIS
Gets Configuration Manager software metering settings.

## SYNTAX

```
Get-CMSoftwareMeteringSetting [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareMeteringSetting** cmdlet gets a software metering settings object in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get software metering setting object
```
PS C:\> Get-CMSoftwareMeteringSetting

ClientComponentName : Software Metering Agent
FileType            : 2
Flags               : 1
ItemName            : Software Metering Agent
ItemType            : Client Component
PropLists           : 
Props               : 
RegMultiStringLists : 
SiteCode            : CM1
```

This command gets a software metering setting object.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSoftwareMeteringSetting](xref:ConfigurationManager/vlatest/Set-CMSoftwareMeteringSetting.md)


