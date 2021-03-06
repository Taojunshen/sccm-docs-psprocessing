---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834029
schema: 2.0.0
ms.assetid: CBAF58CB-B602-4A3D-ACAD-61078090F657
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMPackage.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMPackage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMPackage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Export-CMPackage

## SYNOPSIS
Exports a Configuration Manager package.

## SYNTAX

### SearchByValue (Default)
```
Export-CMPackage -InputObject <IResultObject> -FileName <String> [-WithDependence <Boolean>]
 [-WithContent <Boolean>] [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Export-CMPackage -Id <String> -FileName <String> [-WithDependence <Boolean>] [-WithContent <Boolean>]
 [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchPackageByNameMandatory
```
Export-CMPackage -Name <String> -FileName <String> [-WithDependence <Boolean>] [-WithContent <Boolean>]
 [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMPackage** cmdlet exports a Microsoft System Center Configuration Manager package.
You can use this cmdlet in System Center Configuration Manager to create a package of collections, queries, or reports and then export that package so that you can later deploy these items to a different location.

## EXAMPLES

### Example 1: Export a package by using an ID
```
PS C:\>Export-CMPackage -Id "ST120001" -ExportFilePath "\\Deploy01\ExportPackages"
```

This command exports a package that has the ID ST120001 to the output path \\\\Deploy01\ExportPackages.

### Example 2: Export a package by using a variable
```
PS C:\> $DeplObj = Get-CMPackage -Id "ST120001"
PS C:\> Export-CMPackage - "ST120001" -ExportFilePath"\\Deploy01\ExportPackages" -InputObject $DeplObj
```

The first command gets the package that has the ID ST120001, and then stores it in the variable $DeplObj.

The second command exports the package to the path \\\\Deploy01\ExportPackages by using the $DeplObj variable.

## PARAMETERS

### -Comment


```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments
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

### -FileName


```yaml
Type: String
Parameter Sets: (All)
Aliases: ExportFilePath
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

### -Id
Specifies an array of IDs for packages.

```yaml
Type: String
Parameter Sets: SearchPackageByIdMandatory
Aliases: PackageId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the package that you export by using a Configuration Manager package object.
To obtain a package object, use the [Get-CMPackage](./Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a package.

```yaml
Type: String
Parameter Sets: SearchPackageByNameMandatory
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

### -WithContent
Indicates whether to include content in the package.

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

### -WithDependence
Indicates whether to include dependencies in the package.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Import-CMPackage](xref:ConfigurationManager/vlatest/Import-CMPackage.md)

[Get-CMPackage](xref:ConfigurationManager/vlatest/Get-CMPackage.md)

[New-CMPackage](xref:ConfigurationManager/vlatest/New-CMPackage.md)

[Remove-CMPackage](xref:ConfigurationManager/vlatest/Remove-CMPackage.md)

[Set-CMPackage](xref:ConfigurationManager/vlatest/Set-CMPackage.md)


