---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834173
schema: 2.0.0
ms.assetid: C6C21CFF-2DF9-4D17-BC99-6367B2E90120
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMSoftwareUpdateSummarization.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMSoftwareUpdateSummarization.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Invoke-CMSoftwareUpdateSummarization

## SYNOPSIS
Runs the Configuration Manager software update summarization.

## SYNTAX

```
Invoke-CMSoftwareUpdateSummarization [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMSoftwareUpdateSummarization** cmdlet runs the software update summarization in Microsoft System Center Configuration Manager immediately.
System Center Configuration Manager summarizes software update status on a regular schedule.
This cmdlet does not reset the time for the next automatic summarization.

You can use the Get-CMSoftwareUpdateSummarizationSchedule cmdlet to view the current schedule and the Set-CMSoftwareUpdateSummarizationSchedule cmdlet to change the schedule.

## EXAMPLES

### Example 1: Run software update summarization
```
PS C:\>Invoke-CMSoftwareUpdateSummarization
```

This command runs the software update summarization immediately, instead of waiting for the next scheduled time.

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

[Get-CMSoftwareUpdateSummarizationSchedule](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdateSummarizationSchedule.md)

[Set-CMSoftwareUpdateSummarizationSchedule](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdateSummarizationSchedule.md)


