---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833690
schema: 2.0.0
ms.assetid: 51F673B9-5558-4865-8AF8-B0B67296F729
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMBoundaryGroup.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMBoundaryGroup.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMBoundaryGroup

## SYNOPSIS
Modifies the properties of a boundary group.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMBoundaryGroup -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-DefaultSiteCode <String>] [-AddSiteSystemServer <Hashtable>] [-RemoveSiteSystemServer <IResultObject[]>]
 [-RemoveSiteSystemServerName <String[]>] [-ClearSiteSystemServer] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMBoundaryGroup -Id <String> [-NewName <String>] [-Description <String>] [-DefaultSiteCode <String>]
 [-AddSiteSystemServer <Hashtable>] [-RemoveSiteSystemServer <IResultObject[]>]
 [-RemoveSiteSystemServerName <String[]>] [-ClearSiteSystemServer] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMBoundaryGroup -Name <String> [-NewName <String>] [-Description <String>] [-DefaultSiteCode <String>]
 [-AddSiteSystemServer <Hashtable>] [-RemoveSiteSystemServer <IResultObject[]>]
 [-RemoveSiteSystemServerName <String[]>] [-ClearSiteSystemServer] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMBoundaryGroup** cmdlet modifies the properties of a boundary group.
A boundary group is a collection of boundaries.
For more information about boundaries, see [Planning for Boundaries and Boundary Groups in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266225) on TechNet and the New-CMBoundary cmdlet.

## EXAMPLES

### Example 1: Rename a boundary group
```
PS C:\>Set-CMBoundaryGroup -Name "BGroup01" -NewName "BGroup00"
```

This command renames a boundary group.

### Example 2: Add a security scope to a boundary group
```
PS C:\>Set-CMBoundaryGroup -SecurityScopeAction AddMembership -SecurityScopeName "OSDeploymentScope" -Name "BGroup02"
```

This command adds the security scope OSDeploymentScope to the boundary group BGroup02.

## PARAMETERS

### -AddSiteSystemServer


```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: AddSiteSystemServers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearSiteSystemServer


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearSiteSystemServers

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

### -DefaultSiteCode
Specifies the default site code of a boundary group.

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

### -Description
Specifies a description for a boundary group.

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

### -Id


```yaml
Type: String
Parameter Sets: SetById
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name


```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for a boundary group.

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

### -PassThru


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

### -RemoveSiteSystemServer


```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveSiteSystemServers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSiteSystemServerName


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveSiteSystemServerNames

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

[Planning for Boundaries and Boundary Groups in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266225)

[Get-CMBoundaryGroup](xref:ConfigurationManager/vlatest/Get-CMBoundaryGroup.md)

[New-CMBoundaryGroup](xref:ConfigurationManager/vlatest/New-CMBoundaryGroup.md)

[Remove-CMBoundaryGroup](xref:ConfigurationManager/vlatest/Remove-CMBoundaryGroup.md)

[Set-CMSecurityScope](xref:ConfigurationManager/vlatest/Set-CMSecurityScope.md)

[New-CMBoundary](xref:ConfigurationManager/vlatest/New-CMBoundary.md)


