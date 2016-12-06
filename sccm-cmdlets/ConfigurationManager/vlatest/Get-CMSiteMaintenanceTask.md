---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833870
schema: 2.0.0
ms.assetid: 3F2EAC38-7AA8-4DC7-BB4B-4F5C3D3A87BE
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSiteMaintenanceTask.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSiteMaintenanceTask.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMSiteMaintenanceTask

## SYNOPSIS
Gets maintenance tasks in Configuration Manager.

## SYNTAX

```
Get-CMSiteMaintenanceTask [-MaintenanceTaskName <String>] [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSiteMaintenanceTask** cmdlet gets maintenance tasks in Microsoft System Center Configuration Manager.
A maintenance task is a task in System Center Configuration Manager that performs maintenance on sites and databases.

## EXAMPLES

### Example 1: Get a maintenance task
```
PS C:\>Get-CMSiteMaintenanceTask -SiteCode "CM1" -MaintenanceTaskName "Backup"
```

This command gets the maintenance task named Backup for the Configuration Manager site that has the site code CM1.

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

### -MaintenanceTaskName
Specifies an array of names for maintenance tasks.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ItemName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSiteMaintenanceTask](xref:ConfigurationManager/vlatest/Set-CMSiteMaintenanceTask.md)


