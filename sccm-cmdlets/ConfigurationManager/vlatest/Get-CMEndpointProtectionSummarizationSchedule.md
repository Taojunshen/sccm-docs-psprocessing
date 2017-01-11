---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833684
schema: 2.0.0
ms.assetid: 27AABF04-9A90-4997-8859-7D3BD360830B
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMEndpointProtectionSummarizationSchedule.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMEndpointProtectionSummarizationSchedule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMEndpointProtectionSummarizationSchedule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMEndpointProtectionSummarizationSchedule

## SYNOPSIS
Gets an Endpoint Protection summarization schedule.

## SYNTAX

```
Get-CMEndpointProtectionSummarizationSchedule [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEndpointProtectionSummarizationSchedule** cmdlet gets a System Center 2016 Endpoint Protection summarization schedule.
For more information about Endpoint Protection summarization schedules, see [How to Monitor Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268428) on TechNet.

## EXAMPLES

### Example 1: Get an Endpoint Protection summarization schedule
```
PS C:\> Get-CMEndpointProtectionSummarizationSchedule
```

This command gets an Endpoint Protection summarization schedule.

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

[Set-CMEndpointProtectionSummarizationSchedule](xref:ConfigurationManager/vlatest/Set-CMEndpointProtectionSummarizationSchedule.md)


