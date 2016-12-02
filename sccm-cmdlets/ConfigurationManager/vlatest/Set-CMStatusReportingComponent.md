---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834114
schema: 2.0.0
ms.assetid: CCA28711-4E40-4FAC-8444-E007F9A1049A
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMStatusReportingComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMStatusReportingComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMStatusReportingComponent

## SYNOPSIS
Sets an object representing a status reporting component.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMStatusReportingComponent -InputObject <IResultObject> [-ServerReportChecked <Boolean>]
 [-ServerReportType <StatusReportOrLogType>] [-ServerReportFailureChecked <Boolean>]
 [-ServerLogChecked <Boolean>] [-ServerLogType <StatusReportOrLogType>] [-ServerLogFailureChecked <Boolean>]
 [-ClientReportChecked <Boolean>] [-ClientReportType <StatusReportOrLogType>]
 [-ClientReportFailureChecked <Boolean>] [-ClientLogChecked <Boolean>] [-ClientLogType <StatusReportOrLogType>]
 [-ClientLogFailureChecked <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchBySiteCodeMandatory
```
Set-CMStatusReportingComponent [-SiteCode <String>] [-ServerReportChecked <Boolean>]
 [-ServerReportType <StatusReportOrLogType>] [-ServerReportFailureChecked <Boolean>]
 [-ServerLogChecked <Boolean>] [-ServerLogType <StatusReportOrLogType>] [-ServerLogFailureChecked <Boolean>]
 [-ClientReportChecked <Boolean>] [-ClientReportType <StatusReportOrLogType>]
 [-ClientReportFailureChecked <Boolean>] [-ClientLogChecked <Boolean>] [-ClientLogType <StatusReportOrLogType>]
 [-ClientLogFailureChecked <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMStatusReportingComponent -Name <String> [-ServerReportChecked <Boolean>]
 [-ServerReportType <StatusReportOrLogType>] [-ServerReportFailureChecked <Boolean>]
 [-ServerLogChecked <Boolean>] [-ServerLogType <StatusReportOrLogType>] [-ServerLogFailureChecked <Boolean>]
 [-ClientReportChecked <Boolean>] [-ClientReportType <StatusReportOrLogType>]
 [-ClientReportFailureChecked <Boolean>] [-ClientLogChecked <Boolean>] [-ClientLogType <StatusReportOrLogType>]
 [-ClientLogFailureChecked <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMStatusReportingComponent** cmdlet sets an object that represents a status reporting component.
A status reporting component object specifies information about the client configuration and server configuration components.

You can configure the reporting component to check log files and monitor the severity of entries in the log files.

## EXAMPLES

### Example 1: Set status reporting component
```
PS C:\>Set-CMStatusReportingComponent -SiteCode "CM1" -ClientReportType AllMilestones -ServerReportType AllMilestones
```

This command sets a client report type and a server report type.

## PARAMETERS

### -ClientLogChecked
Indicates whether a client log is checked.

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

### -ClientLogFailureChecked
Indicates whether a client log failure is checked.

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

### -ClientLogType
Specifies a type of client log.
The acceptable values for this parameter are:

- AllMilestones
- AllMilestonesAndAllDetails
- AllMilestonesAndAllDetails
- ErrorMilestones

```yaml
Type: StatusReportOrLogType
Parameter Sets: (All)
Aliases: 
Accepted values: AllMilestonesAndAllDetails, AllMilestones, ErrorAndWarningMilestones, ErrorMilestones

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientReportChecked
Indicates whether a client report is checked.

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

### -ClientReportFailureChecked
Indicates whether a client failure is checked.

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

### -ClientReportType
Specifies a type of report.
The acceptable values for this parameter are:

- AllMilestones
- AllMilestonesAndAllDetails
- ErrorAndWarningMilestones
- ErrorMilestones

```yaml
Type: StatusReportOrLogType
Parameter Sets: (All)
Aliases: 
Accepted values: AllMilestonesAndAllDetails, AllMilestones, ErrorAndWarningMilestones, ErrorMilestones

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

### -InputObject
Specifies an object output from another cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for a status reporting component in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerLogChecked
Indicates whether a server log is checked.

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

### -ServerLogFailureChecked
Indicates whether a server log failure is checked.

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

### -ServerLogType
Specifies a server log type.
The acceptable values for this parameter are:

- AllMilestones
- AllMilestonesAndAllDetails
- ErrorAndWarningMilestones
- ErrorMilestones

```yaml
Type: StatusReportOrLogType
Parameter Sets: (All)
Aliases: 
Accepted values: AllMilestonesAndAllDetails, AllMilestones, ErrorAndWarningMilestones, ErrorMilestones

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerReportChecked
Indicates whether a server report is checked.

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

### -ServerReportFailureChecked
Indicates whether a server report failure is checked.

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

### -ServerReportType
Specifies a report type.
The acceptable values for this parameter are:

- AllMilestones
- AllMilestonesAndAllDetails
- ErrorAndWarningMilestones
- ErrorMilestones

```yaml
Type: StatusReportOrLogType
Parameter Sets: (All)
Aliases: 
Accepted values: AllMilestonesAndAllDetails, AllMilestones, ErrorAndWarningMilestones, ErrorMilestones

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
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

[Get-CMStatusReportingComponent](xref:ConfigurationManager/vlatest/Get-CMStatusReportingComponent.md)


