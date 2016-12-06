---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833697
schema: 2.0.0
ms.assetid: 0F23554E-0127-4B10-A3B2-3F9AF0D639C5
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMMaintenanceWindow.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/New-CMMaintenanceWindow.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMMaintenanceWindow

## SYNOPSIS
Creates a maintenance window for a collection.

## SYNTAX

### ByCollection (Default)
```
New-CMMaintenanceWindow [-InputObject] <IResultObject> [-IsEnabled <Boolean>] -Schedule <IResultObject>
 -Name <String> [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToTaskSequenceOnly] [-ApplyToSoftwareUpdateOnly]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionId
```
New-CMMaintenanceWindow [-CollectionId] <String> [-IsEnabled <Boolean>] -Schedule <IResultObject>
 -Name <String> [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToTaskSequenceOnly] [-ApplyToSoftwareUpdateOnly]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionName
```
New-CMMaintenanceWindow [-CollectionName] <String> [-IsEnabled <Boolean>] -Schedule <IResultObject>
 -Name <String> [-ApplyTo <MaintenanceWindowApplyTo>] [-ApplyToTaskSequenceOnly] [-ApplyToSoftwareUpdateOnly]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMMaintenanceWindow** cmdlet creates a maintenance window for a collection.
Maintenance windows are periods of time reserved for write operations such as applying software updates, installing software, or configuring computer settings.

## EXAMPLES

### Example 1: Create a maintenance window
```
PS C:\>$MWSchedule = New-CMSchedule -DayOfWeek Friday -DurationCount 0 -DurationInterval Hours -RecurCount 1 -Start "10/12/2013 21:00:00"
PS C:\> New-CMMaintenanceWindow -CollectionID "AAA0005D" -Name "MonthlySchedule" -Schedule $MWSchedule
```

The first command uses the **New-CMSchedule** cmdlet to create a schedule object, and then stores it in the $MWSchedule variable.

The second command creates a maintenance window named MonthlySchedule for the specified collection.
The maintenance window uses the schedule stored in the $MWSchedule variable.

## PARAMETERS

### -ApplyTo


```yaml
Type: MaintenanceWindowApplyTo
Parameter Sets: (All)
Aliases: 
Accepted values: Any, SoftwareUpdatesOnly, TaskSequencesOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToSoftwareUpdateOnly


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

### -ApplyToTaskSequenceOnly


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

### -CollectionId


```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName


```yaml
Type: String
Parameter Sets: ByCollectionName
Aliases: 

Required: True
Position: 0
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


```yaml
Type: IResultObject
Parameter Sets: ByCollection
Aliases: Collection

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsEnabled


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

### -Name


```yaml
Type: String
Parameter Sets: (All)
Aliases: MaintenanceWindowName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule


```yaml
Type: IResultObject
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

[Get-CMMaintenanceWindow](xref:ConfigurationManager/vlatest/Get-CMMaintenanceWindow.md)

[New-CMSchedule](xref:ConfigurationManager/vlatest/New-CMSchedule.md)

[Remove-CMMaintenanceWindow](xref:ConfigurationManager/vlatest/Remove-CMMaintenanceWindow.md)

[Set-CMMaintenanceWindow](xref:ConfigurationManager/vlatest/Set-CMMaintenanceWindow.md)


