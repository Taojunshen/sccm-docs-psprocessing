---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833929
schema: 2.0.0
ms.assetid: 62D4DFB1-3F7B-49A2-AEA8-8FA5747B743F
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateSummarizationSchedule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateSummarizationSchedule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMSoftwareUpdateSummarizationSchedule

## SYNOPSIS
Displays the Configuration Manager schedule for software update summarization.

## SYNTAX

```
Get-CMSoftwareUpdateSummarizationSchedule [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateSummarizationSchedule** cmdlet displays the current schedule for software update summarization for Microsoft System Center Configuration Manager.
You can use the Set-CMSoftwareUpdateSummarizationSchedule cmdlet to change the schedule.
You can use the Invoke-CMSoftwareUpdateSummarization cmdlet to run the summarization immediately.

## EXAMPLES

### Example 1: Display the summarization schedule
```
PS C:\>Get-CMSoftwareUpdateSummarizationSchedule
                               Interval                                    Unit
                               --------                                    ----
                                     12                                   Hours
```

This command displays the summarization schedule for software updates.
In this case, the schedule is every 12 hours.

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

### -PassThru


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

[Set-CMSoftwareUpdateSummarizationSchedule](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdateSummarizationSchedule.md)

[Invoke-CMSoftwareUpdateSummarization](xref:ConfigurationManager/vlatest/Invoke-CMSoftwareUpdateSummarization.md)


