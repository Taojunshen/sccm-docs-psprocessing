---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833932
schema: 2.0.0
ms.assetid: 478AB135-42CF-4D2E-9D7B-B6A8C5A1ECCF
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMBoundaryFromGroup.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMBoundaryFromGroup.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMBoundaryFromGroup

## SYNOPSIS
Removes a Configuration Manager boundary from a boundary group.

## SYNTAX

### RemoveBoundaryFromGroupById_Id (Default)
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryId <Int32> -BoundaryGroupId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupById_Name
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryId <Int32> -BoundaryGroupName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupById_Object
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryId <Int32> -BoundaryGroupInputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByName_Name
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryName <String> -BoundaryGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByName_Id
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryName <String> -BoundaryGroupId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByName_Object
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryName <String> -BoundaryGroupInputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByObject_Id
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryInputObject <IResultObject> -BoundaryGroupId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByObject_Object
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryInputObject <IResultObject>
 -BoundaryGroupInputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### RemoveBoundaryFromGroupByObject_Name
```
Remove-CMBoundaryFromGroup [-Force] -BoundaryInputObject <IResultObject> -BoundaryGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMBoundaryFromGroup** cmdlet removes a Microsoft System Center Configuration Manager boundary from a boundary group.
A boundary is a network address range, subnet, or Active Directory site that identifies a group of computers that are close in the network.
A boundary group is a collection of boundaries.

## EXAMPLES

### Example 1: Remove a boundary from a group by using the boundary name
```
PS C:\>Remove-CMBoundaryFromGroup -BoundaryGroupID "16777219" -BoundaryName "CLBound03"
```

This example removes a boundary named CLBound03 from a boundary group that has the ID 16777219.

### Example 2: Remove multiple boundary groups by using an InputObject
```
PS C:\>$BoundaryObj = Get-CMBoundary -Name "Bound01", "Bound02", "Bound03"
PS C:\> Remove-CMBoundaryFromGroup -Boundary $BoundaryObj -BoundaryGroupName "BGroup02"
```

The first command uses the **Get-CMBoundary** cmdlet to get multiple boundaries that are specified by their names, and stores this data into the **$BoundaryObj** variable.

The second command identifies and removes the boundaries that are specified by using the input object **$BoundaryObj**.
Because the *Force* parameter is not specified, you must confirm the action before it is performed.

## PARAMETERS

### -BoundaryGroupId
Specifies an ID for the boundary group from which you remove a boundary.

```yaml
Type: Int32
Parameter Sets: RemoveBoundaryFromGroupById_Id, RemoveBoundaryFromGroupByName_Id, RemoveBoundaryFromGroupByObject_Id
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryGroupInputObject


```yaml
Type: IResultObject
Parameter Sets: RemoveBoundaryFromGroupById_Object, RemoveBoundaryFromGroupByName_Object, RemoveBoundaryFromGroupByObject_Object
Aliases: BoundaryGroup
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryGroupName
Specifies a name for the boundary group from which you remove a boundary.

```yaml
Type: String
Parameter Sets: RemoveBoundaryFromGroupById_Name, RemoveBoundaryFromGroupByName_Name, RemoveBoundaryFromGroupByObject_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryId
Specifies an ID for the boundary that this cmdlet removes.

```yaml
Type: Int32
Parameter Sets: RemoveBoundaryFromGroupById_Id, RemoveBoundaryFromGroupById_Name, RemoveBoundaryFromGroupById_Object
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryInputObject


```yaml
Type: IResultObject
Parameter Sets: RemoveBoundaryFromGroupByObject_Id, RemoveBoundaryFromGroupByObject_Object, RemoveBoundaryFromGroupByObject_Name
Aliases: Boundary
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryName
Specifies a name for the boundary that this cmdlet removes.

```yaml
Type: String
Parameter Sets: RemoveBoundaryFromGroupByName_Name, RemoveBoundaryFromGroupByName_Id, RemoveBoundaryFromGroupByName_Object
Aliases: 
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

[Add-CMBoundaryToGroup](xref:ConfigurationManager/vlatest/Add-CMBoundaryToGroup.md)

[Get-CMBoundary](xref:ConfigurationManager/vlatest/Get-CMBoundary.md)

[Get-CMBoundaryGroup](xref:ConfigurationManager/vlatest/Get-CMBoundaryGroup.md)

[New-CMBoundary](xref:ConfigurationManager/vlatest/New-CMBoundary.md)

[New-CMBoundaryGroup](xref:ConfigurationManager/vlatest/New-CMBoundaryGroup.md)

[Remove-CMBoundary](xref:ConfigurationManager/vlatest/Remove-CMBoundary.md)

[Remove-CMBoundaryGroup](xref:ConfigurationManager/vlatest/Remove-CMBoundaryGroup.md)

[Set-CMBoundaryGroup](xref:ConfigurationManager/vlatest/Set-CMBoundaryGroup.md)


