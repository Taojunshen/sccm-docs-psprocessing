---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834257
schema: 2.0.0
ms.assetid: 009BA9A5-AB9A-4512-99D9-D2788C7FE02A
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Sync-CMSoftwareUpdate.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Sync-CMSoftwareUpdate.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Sync-CMSoftwareUpdate.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Sync-CMSoftwareUpdate

## SYNOPSIS
Synchronizes software updates.

## SYNTAX

```
Sync-CMSoftwareUpdate -FullSync <Boolean> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Sync-CMSoftwareUpdate** cmdlet retrieves metadata for software updates.
Software updates synchronization in Configuration Manager uses Microsoft Update to retrieve software updates metadata.
You can use this cmdlet to retrieve metadata for all software updates or only recent changes to software updates.

## EXAMPLES

### Example 1: Perform a full synchronization for all software updates
```
PS C:\> Sync-CMSoftwareUpdate -FullSync $True
```

This command performs a complete metadata synchronization for all software updates.

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

### -FullSync
Indicates whether to perform a complete synchronization of all updates or a delta synchronization.

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

[Get-CMSoftwareUpdate](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdate.md)

[Save-CMSoftwareUpdate](xref:ConfigurationManager/vlatest/Save-CMSoftwareUpdate.md)

[Set-CMSoftwareUpdate](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdate.md)


