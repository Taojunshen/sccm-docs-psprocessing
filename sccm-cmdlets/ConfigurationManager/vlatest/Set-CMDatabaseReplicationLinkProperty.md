---
external help file: AdminUI.PS.DatabaseReplication.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833779
schema: 2.0.0
ms.assetid: C3D5A011-7F5C-4151-BB10-112E9A0E78CA
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMDatabaseReplicationLinkProperty.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMDatabaseReplicationLinkProperty.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMDatabaseReplicationLinkProperty.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMDatabaseReplicationLinkProperty

## SYNOPSIS
Changes configuration settings for a database replication link.

## SYNTAX

### SetBySiteCodeMandatory (Default)
```
Set-CMDatabaseReplicationLinkProperty -ParentSiteCode <String> -ChildSiteCode <String>
 [-EnableDistributedViewForHardwareInventory <Boolean>] [-EnableDistributedViewForSoftwareInventory <Boolean>]
 [-EnableDistributedViewForStatusMessage <Boolean>] [-ReplicationDataTrafficSummarizationMins <Int32>]
 [-DegradedLinkStatusRetryCount <Int32>] [-FailedLinkStatusRetryCount <Int32>]
 [-GenerateReplicationDownAlert <Boolean>] [-ReplicationDownAlertMins <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetScheduleBySiteCodeMandatory
```
Set-CMDatabaseReplicationLinkProperty -ParentSiteCode <String> -ChildSiteCode <String>
 -DaysOfWeek <DaysOfWeek[]> -ReplicationStartHr <Int32> -ReplicationEndHr <Int32>
 -AvailabilityLevel <InvAvailabilityLevel> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDatabaseReplicationLinkProperty** cmdlet changes configuration settings for a database replication link between a Microsoft System Center Configuration Manager parent site and child site.

Database replication for Configuration Manager sites transfers data and merges changes made in a site database with information stored at other sites in the Configuration Manager hierarchy.
This enables all sites to share the same information.

## EXAMPLES

### Example 1: Change settings of a database replication link
```
PS C:\> Set-CMDatabaseReplicationLinkProperty -ParentSiteCode "CCC" -ChildSiteCode "CCB" -EnableDistributedViewForHardwareInventory 1 -EnableDistributedViewForSoftwareInventory 1 -EnableDistributedViewForStatusMessage 1 -ReplicationDataTrafficSummarizationIntervalMinutes 12 -DegradedLinkStatusRetryCount 40 -FailedLinkStatusRetryCount 60 -GenerateReplicationDownAlert 1 -ReplicationDownAlertThresholdMinutes 20
```

This command changes configuration settings for a database replication link between the Configuration Manager parent site that has the site code CCC and the child site that has the site code CCB.

### Example 2: Set the schedule for a database replication link
```
PS C:\> Set-CMDatabaseReplicationLinkProperty -ParentSiteCode "CCC" -ChildSiteCode "CCB" -DaysOfWeek Friday, Monday, Tuesday -TimePeriodStart 8 -TimePeriodEnd 0 -AvailabilityLevel HINVSINV
```

This command sets the schedule for the database replication link between the Configuration Manager parent site that has the site code CCC and the child site that has the site code CCB.
The command specifies that Configuration Manager replicates the database for Configuration Manager sites on Friday, Monday, and Tuesday.
The command specifies software and hardware inventory availability on the client computer.

## PARAMETERS

### -AvailabilityLevel
Specifies the availability level for software and hardware inventory on a client computer.
The acceptable values for this parameter are:

- Closed
- HINV
- SINV
- HINVSINV
- StatMSG
- HINVStatMSG
- SINVStatMSG
- HINVSINVStatMSG

```yaml
Type: InvAvailabilityLevel
Parameter Sets: SetScheduleBySiteCodeMandatory
Aliases: 
Accepted values: Closed, HINV, SINV, HINVSINV, StatMSG, HINVStatMSG, SINVStatMSG, HINVSINVStatMSG
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ChildSiteCode
Specifies a site code for a Configuration Manager site.
This parameter refers to the child site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Site2
Required: True
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

### -DaysOfWeek
Specifies an array of day names that determine the days of each week on which Configuration Manager replicates the database for Configuration Manager sites.
The acceptable values for this parameter are:

- Monday
- Tuesday
- Wednesday
- Thursday
- Friday
- Saturday
- Sunday

```yaml
Type: DaysOfWeek[]
Parameter Sets: SetScheduleBySiteCodeMandatory
Aliases: 
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DegradedLinkStatusRetryCount
Specifies a retry count when a replication group or object is delayed due to degraded link status.

```yaml
Type: Int32
Parameter Sets: SetBySiteCodeMandatory
Aliases: 
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

### -EnableDistributedViewForHardwareInventory
Indicates whether Configuration Manager configures the SQL Server distributed partitioned views for hardware inventory.

```yaml
Type: Boolean
Parameter Sets: SetBySiteCodeMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDistributedViewForSoftwareInventory
Indicates whether Configuration Manager configures the SQL Server distributed partitioned views for software inventory.

```yaml
Type: Boolean
Parameter Sets: SetBySiteCodeMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDistributedViewForStatusMessage
Indicates whether Configuration Manager configures the SQL Server distributed partitioned views for status messages.

```yaml
Type: Boolean
Parameter Sets: SetBySiteCodeMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FailedLinkStatusRetryCount
Specifies a retry count when a replication group or object is delayed by failed link status.

```yaml
Type: Int32
Parameter Sets: SetBySiteCodeMandatory
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

### -GenerateReplicationDownAlert
Indicates whether to generate a replication down alert.

```yaml
Type: Boolean
Parameter Sets: SetBySiteCodeMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentSiteCode
Specifies a site code for a Configuration Manager site.
This parameter refers to the parent site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Site1
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationDataTrafficSummarizationMins


```yaml
Type: Int32
Parameter Sets: SetBySiteCodeMandatory
Aliases: ReplicationDataTrafficSummarizationIntervalMinutes
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationDownAlertMins


```yaml
Type: Int32
Parameter Sets: SetBySiteCodeMandatory
Aliases: ReplicationDownAlertThresholdMinutes
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationEndHr


```yaml
Type: Int32
Parameter Sets: SetScheduleBySiteCodeMandatory
Aliases: TimePeriodEnd, ReplicationEndHour
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationStartHr


```yaml
Type: Int32
Parameter Sets: SetScheduleBySiteCodeMandatory
Aliases: TimePeriodStart, ReplicationStartHour
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

[Get-CMDatabaseReplicationLinkProperty](xref:ConfigurationManager/vlatest/Get-CMDatabaseReplicationLinkProperty.md)

[Get-CMDataBaseReplicationStatus](xref:ConfigurationManager/vlatest/Get-CMDataBaseReplicationStatus.md)


