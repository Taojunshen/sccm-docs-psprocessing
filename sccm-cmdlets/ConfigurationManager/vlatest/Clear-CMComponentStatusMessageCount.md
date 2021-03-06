---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833839
schema: 2.0.0
ms.assetid: ACD65BCF-63FD-4A8D-B382-9FBD3BEEF261
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Clear-CMComponentStatusMessageCount.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Clear-CMComponentStatusMessageCount.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Clear-CMComponentStatusMessageCount.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Clear-CMComponentStatusMessageCount

## SYNOPSIS
Changes the component status message count to zero.

## SYNTAX

```
Clear-CMComponentStatusMessageCount -ComponentName <String> [-ComputerName <String>] [-SiteCode <String>]
 -Severity <Severity> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Clear-CMComponentStatusMessageCount** cmdlet changes the component status message count to zero (0).

Microsoft System Center Configuration Manager indicates whether operations succeed or fail and include other information in component status messages.
Threads or processes send component status messages to Configuration Manager sites, identified by site codes.

You can define which message count to set to zero by the component that created the messages, severity of the messages, and the site code of the Configuration Manager server that receives the messages.
You can also specify the computer that hosts that component.

## EXAMPLES

### Example 1: Clear message count
```
PS C:\>Clear-CMComponentStatusMessageCount -ComponentName "SMS_HIERARCHY_MANAGER" -Severity All -SiteCode "CM1"
```

This command changes the message count to zero for the component SMS_HIERARCHY_MANAGER for all message severity types.
The command specifies the site that has the site code CM1.

### Example 2: Clear error message count
```
PS C:\>Clear-CMComponentStatusMessageCount -ComponentName "SMS_DISTRIBUTION_MANAGER" -Severity Error -SiteCode "CM1" -ComputerName "West34.Western.Contoso.com"
```

This command changes the message count to zero for the component SMS_DISTRIBUTION_MANAGER for error messages.
The command specifies the site that has the site code CM1, and includes the computer name West34.Western.Contoso.com.

## PARAMETERS

### -ComponentName
Specifies the name of a component that creates messages.

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

### -ComputerName
Specifies the name of a computer that hosts the component.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MachineName
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

### -Severity
Specifies the severity of a component status message.
The acceptable values for this parameter are:

- All
- Error
- Information
- Warning

```yaml
Type: Severity
Parameter Sets: (All)
Aliases: 
Accepted values: All, Error, Warning, Information
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.
Status messages originate in this site.

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

[Get-CMComponentStatusMessage](xref:ConfigurationManager/vlatest/Get-CMComponentStatusMessage.md)


