---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834202
schema: 2.0.0
ms.assetid: 78F11C36-9204-405A-AB8C-4F4F305349EA
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMClientStatusUpdateSchedule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMClientStatusUpdateSchedule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMClientStatusUpdateSchedule

## SYNOPSIS
Gets a schedule interval of the client status update task.

## SYNTAX

```
Get-CMClientStatusUpdateSchedule [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientStatusUpdateSchedule** cmdlet gets a schedule interval of the client status update task.

## EXAMPLES

### Example 1: Gets a client status update schedule
```
PS C:\>Get-CMClientStatusUpdateSchedule
Interval Unit 
-------- ----
       1 Days
```

This command gets a client status update schedule.

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

[Set-CMClientStatusUpdateSchedule](xref:ConfigurationManager/vlatest/Set-CMClientStatusUpdateSchedule.md)

[Get-CMClientStatusSetting](xref:ConfigurationManager/vlatest/Get-CMClientStatusSetting.md)

[Set-CMClientStatusSetting](xref:ConfigurationManager/vlatest/Set-CMClientStatusSetting.md)


