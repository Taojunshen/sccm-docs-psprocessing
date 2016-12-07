---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834126
schema: 2.0.0
ms.assetid: 64883A65-5691-40B6-B8DE-C2DE4EDEEB23
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMMaintenanceWindow.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMMaintenanceWindow.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMMaintenanceWindow

## SYNOPSIS
Removes a maintenance window.

## SYNTAX

### ByCollection (Default)
```
Remove-CMMaintenanceWindow [-Collection] <IResultObject> -MaintenanceWindowName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionId
```
Remove-CMMaintenanceWindow [-CollectionId] <String> -MaintenanceWindowName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionName
```
Remove-CMMaintenanceWindow [-CollectionName] <String> -MaintenanceWindowName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMMaintenanceWindow** cmdlet removes a maintenance window associated with a collection.
If you remove a maintenance window during that window, the maintenance updates finish installation.

## EXAMPLES

### Example 1: Remove a maintenance window
```
PS C:\>Remove-CMMaintenanceWindow -Name "Distribution Point Maintenance" -CollectionId "AAA0004D"
```

This command removes the maintenance window Distribution Point Maintenance.
The window is part of the collection AAA0004D.

## PARAMETERS

### -Collection


```yaml
Type: IResultObject
Parameter Sets: ByCollection
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId
Specifies the ID of the collection that the maintenance window applies to.

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

### -Force
Forces the command to run without asking for user confirmation.

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

### -MaintenanceWindowName


```yaml
Type: String
Parameter Sets: (All)
Aliases: Name
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

[New-CMMaintenanceWindow](xref:ConfigurationManager/vlatest/New-CMMaintenanceWindow.md)

[Set-CMMaintenanceWindow](xref:ConfigurationManager/vlatest/Set-CMMaintenanceWindow.md)


