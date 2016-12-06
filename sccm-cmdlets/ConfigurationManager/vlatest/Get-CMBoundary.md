---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834150
schema: 2.0.0
ms.assetid: B3E5550C-8A64-46FA-8D31-1E89FE83BC71
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMBoundary.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMBoundary.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMBoundary

## SYNOPSIS
Gets a boundary.

## SYNTAX

### SearchByName (Default)
```
Get-CMBoundary [-BoundaryName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBoundary -BoundaryId <UInt32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByBoundaryGroupIdMandatory
```
Get-CMBoundary -BoundaryGroupId <UInt32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByBoundaryGroupNameMandatory
```
Get-CMBoundary -BoundaryGroupName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByBoundaryGroup
```
Get-CMBoundary -BoundaryGroupInputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBoundary** cmdlet gets a boundary.

In Microsoft System Center Configuration Manager, a boundary is an intranet location that contains one or more devices that you can manage.
A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, or an IP address range.

## EXAMPLES

### Example 1: Get a boundary that is specified by its identifier.
```
PS C:\>Get-Boundary -Id "67777217"
BoundaryFlags:      0
BoundaryID:         67777217
BoundaryType:       1
CreatedBy:          Contoso\PFuller
CreatedOn           6/10/2012 2:58:56 PM
DefaultSiteCode: 
DisplayName: 
GroupCount:         0
ModifiedBy:         Contoso\PFuller
ModifiedOn:         9/13/2012  10:04 AM
SiteSystems: 
Value:              Default1
```

This command gets a boundary that is specified by the identifier 67777217.

### Example 2: Get a boundary that is specified by the name of an associated boundary group
```
PS C:\>Get-Boundary -BoundaryGroupName "BGroup07"
BoundaryFlags:      0
BoundaryID:         63997411
BoundaryType:       2
CreatedBy:          Contoso\PFuller
CreatedOn           4/13/2012 06:58:56 AM
DefaultSiteCode: 
DisplayName: 
GroupCount:         1
ModifiedBy:         Contoso\PFuller
ModifiedOn:         8/02/2012  11:16 AM
SiteSystems: 
Value:              Default1
```

This command gets a boundary that is specified by the associated boundary group BGroup07.

## PARAMETERS

### -BoundaryGroupId
Specifies an identifier (ID) for a boundary group.
You can get a boundary group ID by using the **Get-CMBoundaryGroup** cmdlet.

```yaml
Type: UInt32
Parameter Sets: SearchByBoundaryGroupIdMandatory
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
Parameter Sets: SearchByBoundaryGroup
Aliases: BoundaryGroup
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryGroupName
Specifies a name for a boundary group.
You can get a boundary group name by using the **Get-CMBoundaryGroup** cmdlet.

```yaml
Type: String
Parameter Sets: SearchByBoundaryGroupNameMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryId


```yaml
Type: UInt32
Parameter Sets: SearchByIdMandatory
Aliases: Id
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BoundaryName


```yaml
Type: String
Parameter Sets: SearchByName
Aliases: DisplayName, Name
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Remove-CMBoundary](xref:ConfigurationManager/vlatest/Remove-CMBoundary.md)

[New-CMBoundary](xref:ConfigurationManager/vlatest/New-CMBoundary.md)

[Set-CMBoundary](xref:ConfigurationManager/vlatest/Set-CMBoundary.md)

[Get-CMBoundaryGroup](xref:ConfigurationManager/vlatest/Get-CMBoundaryGroup.md)


