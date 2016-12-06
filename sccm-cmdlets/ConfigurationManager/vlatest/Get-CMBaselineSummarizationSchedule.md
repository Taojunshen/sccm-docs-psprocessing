---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834138
schema: 2.0.0
ms.assetid: 5DC5CD9E-DF35-4BB7-9AA4-79476C013FF4
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMBaselineSummarizationSchedule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMBaselineSummarizationSchedule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMBaselineSummarizationSchedule

## SYNOPSIS
Gets the summarization schedule for configuration baseline data.

## SYNTAX

```
Get-CMBaselineSummarizationSchedule [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBaselineSummarizationSchedule** cmdlet gets the schedule by which the configuration baseline data in the Microsoft System Center Configuration Manager is updated with the latest information from the site database.

## EXAMPLES

### Example 1: Get the update schedule for configuration baseline data
```
PS C:\>Get-CMBaselineSummarizationSchedule
```

This command gets the update schedule for configuration baseline data.

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

[Set-CMBaselineSummarizationSchedule](xref:ConfigurationManager/vlatest/Set-CMBaselineSummarizationSchedule.md)

[Invoke-CMBaselineSummarization](xref:ConfigurationManager/vlatest/Invoke-CMBaselineSummarization.md)


