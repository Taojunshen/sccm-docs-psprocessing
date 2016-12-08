---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833602
schema: 2.0.0
ms.assetid: A2AA9552-58E9-4C19-BD23-EE6816C90CDB
updated_at: 12/7/2016 8:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMBoundaryToGroup.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/282d10ca7ed3ddf1432b06182fee46c9e52563a4/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMBoundaryToGroup.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Add-CMBoundaryToGroup

## SYNOPSIS
Assigns boundaries to a boundary group.

## SYNTAX

### AddBoundaryToGroupByObject_Object (Default)
```
Add-CMBoundaryToGroup -InputObject <IResultObject> -BoundaryGroupInputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddBoundaryToGroupById_Id
```
Add-CMBoundaryToGroup -BoundaryId <Int32> -BoundaryGroupId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddBoundaryToGroupById_Object
```
Add-CMBoundaryToGroup -BoundaryId <Int32> -BoundaryGroupInputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddBoundaryToGroupById_Name
```
Add-CMBoundaryToGroup -BoundaryId <Int32> -BoundaryGroupName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddBoundaryToGroupByName_Id
```
Add-CMBoundaryToGroup -BoundaryName <String> -BoundaryGroupId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddBoundaryToGroupByName_Name
```
Add-CMBoundaryToGroup -BoundaryName <String> -BoundaryGroupName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddBoundaryToGroupByName_Object
```
Add-CMBoundaryToGroup -BoundaryName <String> -BoundaryGroupInputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddBoundaryToGroupByObject_Id
```
Add-CMBoundaryToGroup -InputObject <IResultObject> -BoundaryGroupId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddBoundaryToGroupByObject_Name
```
Add-CMBoundaryToGroup -InputObject <IResultObject> -BoundaryGroupName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMBoundaryToGroup** cmdlet assigns boundaries to a boundary group.

In Microsoft System Center Configuration Manager, a boundary is an intranet location that contains one or more devices that you can manage.
A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, or an IP address range.

You can use boundary groups to manage network locations.
You must assign boundaries to boundary groups before you can use the boundary group.
Boundary groups enable client computers to find a primary site for client assignment, which is referred to as automatic site assignment, and a list of available site systems that have content.
For more information about boundaries, see [Planning for Boundaries and Boundary Groups in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266225) on TechNet.

## EXAMPLES

### Example 1: Assign a boundary group to a boundary
```
PS C:\>Add-CMBoundaryToGroup -BoundaryGroupID "16777219" -BoundaryName "CLBound03"
```

This command assigns the boundary named to CLBound03 to the boundary group that has the Id 16777219.

## PARAMETERS

### -BoundaryGroupId
Specifies the ID of a boundary group.

```yaml
Type: Int32
Parameter Sets: AddBoundaryToGroupById_Id, AddBoundaryToGroupByName_Id, AddBoundaryToGroupByObject_Id
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
Parameter Sets: AddBoundaryToGroupByObject_Object, AddBoundaryToGroupById_Object, AddBoundaryToGroupByName_Object
Aliases: BoundaryGroup
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryGroupName
Specifies the name of a boundary group.

```yaml
Type: String
Parameter Sets: AddBoundaryToGroupById_Name, AddBoundaryToGroupByName_Name, AddBoundaryToGroupByObject_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryId
Specifies the ID of a boundary.

```yaml
Type: Int32
Parameter Sets: AddBoundaryToGroupById_Id, AddBoundaryToGroupById_Object, AddBoundaryToGroupById_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryName
Specifies the name of a boundary.

```yaml
Type: String
Parameter Sets: AddBoundaryToGroupByName_Id, AddBoundaryToGroupByName_Name, AddBoundaryToGroupByName_Object
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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: AddBoundaryToGroupByObject_Object, AddBoundaryToGroupByObject_Id, AddBoundaryToGroupByObject_Name
Aliases: Boundary, BoundaryInputObject
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Planning for Boundaries and Boundary Groups in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266225)

[Get-CMBoundary](xref:ConfigurationManager/vlatest/Get-CMBoundary.md)

[Get-CMBoundaryGroup](xref:ConfigurationManager/vlatest/Get-CMBoundaryGroup.md)

[Remove-CMBoundaryFromGroup](xref:ConfigurationManager/vlatest/Remove-CMBoundaryFromGroup.md)


