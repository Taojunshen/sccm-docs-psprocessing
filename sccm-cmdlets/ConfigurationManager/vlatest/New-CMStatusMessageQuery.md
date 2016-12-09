---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833785
schema: 2.0.0
ms.assetid: BA4334C4-8D63-4455-AE99-E62E49362502
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/New-CMStatusMessageQuery.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/New-CMStatusMessageQuery.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/New-CMStatusMessageQuery.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# New-CMStatusMessageQuery

## SYNOPSIS
Creates a status message query.

## SYNTAX

```
New-CMStatusMessageQuery -Name <String> [-Comment <String>] [-Expression <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMStatusMessageQuery** cmdlet creates a status message query in Microsoft System Center Configuration Manager.
Status message queries in System Center Configuration Manager return status messages from the site database.
All major System Center Configuration Manager components generate status messages.

## EXAMPLES

### Example 1: Create a status message query
```
PS C:\> New-CMStatusMessageQuery -Name "Client Component Configuration Changes and Fatal Errors" -Expression "select stat.*, ins.*, att1.*, stat.Time from SMS_StatusMessage as stat left join SMS_StatMsgInsStrings as ins on stat.RecordID = ins.RecordID left join SMS_StatMsgAttributes as att1 on stat.RecordID = att1.RecordID where stat.ModuleName = 'SMS Client' and stat.MessageID = 669 and stat.SiteCode = ##PRM:SMS_StatusMessage.SiteCode## and stat.Time >= ##PRM:SMS_StatusMessage.Time## order by stat.Time desc"
```

This command creates a status message query named Client Component Configuration Changes and Fatal Errors.
The *Expression* parameter specifies the WMI Query Language (WQL) text for the query.

## PARAMETERS

### -Comment


```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Expression
Specifies WMI Query Language (WQL) text for the query.

```yaml
Type: String
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

### -Name
Specifies a name for the status message query.

```yaml
Type: String
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

[Get-CMStatusMessageQuery](xref:ConfigurationManager/vlatest/Get-CMStatusMessageQuery.md)

[Set-CMStatusMessageQuery](xref:ConfigurationManager/vlatest/Set-CMStatusMessageQuery.md)

[Remove-CMStatusMessageQuery](xref:ConfigurationManager/vlatest/Remove-CMStatusMessageQuery.md)


