---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833661
schema: 2.0.0
ms.assetid: DEDB28D8-E0D3-43B5-9EC7-B0F81B36652D
updated_at: 12/7/2016 11:21 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMDistributionPointToGroup.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMDistributionPointToGroup.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4bb0549ab9452d0d1c9cdf57cfbc8185eefd798c/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMDistributionPointToGroup.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Add-CMDistributionPointToGroup

## SYNOPSIS
Adds a distribution point to a distribution point group.

## SYNTAX

### AddDistributionPointToGroupByObject_Object (Default)
```
Add-CMDistributionPointToGroup -DistributionPoint <IResultObject> -DistributionPointGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupById_Object
```
Add-CMDistributionPointToGroup -DistributionPointId <String> -DistributionPointGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupById_Name
```
Add-CMDistributionPointToGroup -DistributionPointId <String> -DistributionPointGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupById_Id
```
Add-CMDistributionPointToGroup -DistributionPointId <String> -DistributionPointGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByName_Name
```
Add-CMDistributionPointToGroup -DistributionPointName <String> -DistributionPointGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByName_Id
```
Add-CMDistributionPointToGroup -DistributionPointName <String> -DistributionPointGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByName_Object
```
Add-CMDistributionPointToGroup -DistributionPointName <String> -DistributionPointGroup <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByObject_Name
```
Add-CMDistributionPointToGroup -DistributionPoint <IResultObject> -DistributionPointGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDistributionPointToGroupByObject_Id
```
Add-CMDistributionPointToGroup -DistributionPoint <IResultObject> -DistributionPointGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDistributionPointToGroup** cmdlet adds a distribution point to a distribution point group.
Distribution point groups provide a logical grouping of distribution points for content distribution.

You can add one or more distribution points from any site in the Microsoft System Center Configuration Manager hierarchy to the distribution point group.
You can also add the distribution point to more than one distribution point group so that you can manage and monitor content from a central location for distribution points that span multiple sites.

## EXAMPLES

### Example 1: Add a distribution point to a group
```
PS C:\>Add-CMDistributionPointToGroup -DistributionPointGroupName "DPG01" -Id "{FA921CF2-89C9-407D-A21D-FE6947F2C00A}"
```

This command adds the distribution point that has the Id FA921CF2-89C9-407D-A21D-FE6947F2C00A to the distribution point group named DPG01.

## PARAMETERS

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

### -DistributionPoint
Specifies a distribution point object.
To obtain a **CMDistributionPoint** object, use the [Get-CMDistributionPoint](./Get-CMDistributionPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddDistributionPointToGroupByObject_Object, AddDistributionPointToGroupByObject_Name, AddDistributionPointToGroupByObject_Id
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroup
Specifies a distribution point group object.
To obtain a **CMDistributionPointGroup** object, use the [Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddDistributionPointToGroupByObject_Object, AddDistributionPointToGroupById_Object, AddDistributionPointToGroupByName_Object
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroupId
Specifies the ID of a distribution point group.

```yaml
Type: String
Parameter Sets: AddDistributionPointToGroupById_Id, AddDistributionPointToGroupByName_Id, AddDistributionPointToGroupByObject_Id
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
Specifies the name of a distribution point group.

```yaml
Type: String
Parameter Sets: AddDistributionPointToGroupById_Name, AddDistributionPointToGroupByName_Name, AddDistributionPointToGroupByObject_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointId
Specifies the ID of a distribution point.

```yaml
Type: String
Parameter Sets: AddDistributionPointToGroupById_Object, AddDistributionPointToGroupById_Name, AddDistributionPointToGroupById_Id
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointName
Specifies the name of a distribution point.

```yaml
Type: String
Parameter Sets: AddDistributionPointToGroupByName_Name, AddDistributionPointToGroupByName_Id, AddDistributionPointToGroupByName_Object
Aliases: 
Required: True
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

[Remove-CMDistributionPointFromGroup](xref:ConfigurationManager/vlatest/Remove-CMDistributionPointFromGroup.md)

[Get-CMDistributionPointGroup](xref:ConfigurationManager/vlatest/Get-CMDistributionPointGroup.md)

[Get-CMDistributionPoint](xref:ConfigurationManager/vlatest/Get-CMDistributionPoint.md)


