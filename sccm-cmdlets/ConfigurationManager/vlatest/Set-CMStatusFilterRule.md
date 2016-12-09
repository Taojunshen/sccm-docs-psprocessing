---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834108
schema: 2.0.0
ms.assetid: 3911D73C-E269-4160-8667-732DAFD7AB48
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMStatusFilterRule.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMStatusFilterRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMStatusFilterRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMStatusFilterRule

## SYNOPSIS
Modifies settings for a Configuration Manager filter rule for status messages.

## SYNTAX

```
Set-CMStatusFilterRule [-SiteCode <String>] -Name <String> [-Priority <PriorityChangeType>] [-Source <String>]
 [-StatusFilterRuleSiteCode <String>] [-SiteSystemServerName <String>] [-ComponentName <String>]
 [-MessageType <MessageType>] [-SeverityType <SeverityType>] [-MessageId <Int32>] [-PropertyId <String>]
 [-PropertyValue <String>] [-WriteToDatabase <Boolean>] [-AllowDeleteAfterDays <Int32>]
 [-ReportToEventLog <Boolean>] [-ReplicateToParentSite <Boolean>] [-ReplicationPriority <ReplicationPriority>]
 [-RunProgram <Boolean>] [-ProgramPath <String>] [-ForwardToStatusSummarizer <Boolean>]
 [-ProcessLowerPriorityRule <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMStatusFilterRule** cmdlet modifies settings for a Microsoft System Center Configuration Manager filter rule for status messages.
System Center Configuration Manager checks a status message against rules in order of priority.
A rule can specify that rules with lower priority do not apply to a message after that rule applied.

Status filter rules specify how System Center Configuration Manager responds to status messages.
Each filter rule contains criteria and actions for status messages.
You configure status filter rules for each site, not across all sites.

To change the priority of a rule, use the rule name to specify the rule.

## EXAMPLES

### Example 1: Increase the priority of a rule
```
PS C:\> Set-CMStatusFilterRule -Name "Status change to critical" -SiteCode "CM1" -Priority Increase
```

This command increases the priority of a filter rule that has the specified name in a site that has the site code CM1.

## PARAMETERS

### -AllowDeleteAfterDays


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: AllowUserDeleteMessagesAfterThresholdDays
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComponentName
Specifies the Configuration Manager component that corresponds to the status messages.

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

### -ForwardToStatusSummarizer
Indicates whether to forward to the status summarizer.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MessageId
Specifies a message ID in Configuration Manager.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MessageType
Specifies a status message type in Configuration Manager.

Valid values are:

- Audit
- Detail
- Milestone
- None

```yaml
Type: MessageType
Parameter Sets: (All)
Aliases:
Accepted values: None, Milestone, Detail, Audit
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names for status filter rules.

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

### -Priority
Specifies a change in priority.
Configuration Manager checks status messages against rules in order of rule priority.
Valid values are: Decrease and Increase.

```yaml
Type: PriorityChangeType
Parameter Sets: (All)
Aliases:
Accepted values: Increase, Decrease
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessLowerPriorityRule
Indicates whether to process a lower priority rule, which prevents further rule processing.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgramPath
Specifies a path to a program that runs when a status message matches the status filter rule.

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

### -PropertyId
Specifies a property ID in Configuration Manager.

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

### -PropertyValue
Specifies a value for the corresponding *PropertyId* parameter.

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

### -ReplicateToParentSite
Indicates whether to pass a message to the parent site.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationPriority
Specifies a replication priority for sending status messages to the parent site.

Valid values are:

- High
- Low
- Medium

```yaml
Type: ReplicationPriority
Parameter Sets: (All)
Aliases:
Accepted values: High, Medium, Low
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportToEventLog
Indicates whether to report an event in the Windows event log.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunProgram
Indicates whether to run a program when a status message matches a filter rule.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SeverityType
Specifies the severity of a status message.

Valid values are:

- Error
- Informational
- None
- Warning

```yaml
Type: SeverityType
Parameter Sets: (All)
Aliases:
Accepted values: None, Informational, Warning, Error
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

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

### -SiteSystemServerName
Specifies the name of a site system server in Configuration Manager.

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

### -Source
Specifies the status message source to match.
The possible sources are the following:

- Client
- SMS Provider
- Site Server

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

### -StatusFilterRuleSiteCode
Specifies a site code for the site from which the status message originated.

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

### -WriteToDatabase
Indicates whether to write a message to the database.
Specify a value of $True for this parameter to enable the *AllowUserDeleteMessagesAfterThresholdDays* parameter.

```yaml
Type: Boolean
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

[Disable-CMStatusFilterRule](xref:ConfigurationManager/vlatest/Disable-CMStatusFilterRule.md)

[Enable-CMStatusFilterRule](xref:ConfigurationManager/vlatest/Enable-CMStatusFilterRule.md)

[Get-CMStatusFilterRule](xref:ConfigurationManager/vlatest/Get-CMStatusFilterRule.md)

[New-CMStatusFilterRule](xref:ConfigurationManager/vlatest/New-CMStatusFilterRule.md)

[Remove-CMStatusFilterRule](xref:ConfigurationManager/vlatest/Remove-CMStatusFilterRule.md)
