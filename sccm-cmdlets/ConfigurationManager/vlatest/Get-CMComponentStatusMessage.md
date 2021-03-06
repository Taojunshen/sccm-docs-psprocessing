---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834250
schema: 2.0.0
ms.assetid: 3AABF576-B504-4756-A8B8-412E842306C3
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMComponentStatusMessage.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMComponentStatusMessage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMComponentStatusMessage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMComponentStatusMessage

## SYNOPSIS
Gets component status messages in Configuration Manager.

## SYNTAX

```
Get-CMComponentStatusMessage [-ComponentName <String>] [-ComputerName <String>] [-SiteCode <String>]
 [-Severity <Severity>] -StartTime <DateTime> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMComponentStatusMessage** cmdlet gets component status messages for a specified period.

Microsoft System Center Configuration Manager indicates whether operations succeed or fail and include other information in component status messages.
Threads or processes send component status messages to Configuration Manager sites, which are identified by site codes.

You can define which messages to get by the severity of the message, the component that created the message, the computer that hosts that component, or the Configuration Manager server that receives the message.
You must specify a viewing period, as a **TimeSpan** object.

## EXAMPLES

### Example 1: Get critical messages for a site
```
PS C:\> Get-CMComponentStatusMessage -ViewingPeriod "2/1/2013 12:00 AM" -Severity Warning -SiteCode "CM1"
```

This command gets component status messages for the specified viewing period for the Configuration Manager site that has the site code CM1.
The command gets only warning messages.

## PARAMETERS

### -ComponentName
Specifies the name of a thread or process.
A thread or process sends a component status message.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Component
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Specifies the name of a computer.
A computer hosts a component that sends a status message.

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
Specifies the severity of status messages. 
The acceptable values for this parameter are:

- ALL
- Error
- Information
- Warning

```yaml
Type: Severity
Parameter Sets: (All)
Aliases: 
Accepted values: All, Error, Warning, Information
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies an array of a site codes for Configuration Manager sites.

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

### -StartTime


```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: ViewingPeriod
Required: True
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

[Get-CMComponentStatusSetting](xref:ConfigurationManager/vlatest/Get-CMComponentStatusSetting.md)


