---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834025
schema: 2.0.0
ms.assetid: FB721B53-FA7D-4F58-984A-D8A94A218161
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMDriverPackage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMDriverPackage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Export-CMDriverPackage

## SYNOPSIS
Exports driver packages.

## SYNTAX

### SearchPackageByNameMandatory (Default)
```
Export-CMDriverPackage -Name <String> -ExportFilePath <String> [-WithDependence <Boolean>]
 [-WithContent <Boolean>] [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Export-CMDriverPackage -InputObject <IResultObject> -ExportFilePath <String> [-WithDependence <Boolean>]
 [-WithContent <Boolean>] [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Export-CMDriverPackage -Id <String> -ExportFilePath <String> [-WithDependence <Boolean>]
 [-WithContent <Boolean>] [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMDriverPackage** cmdlet exports one or more driver packages to a .zip file.

## EXAMPLES

### Example 1: Export a driver package
```
PS C:\>Export-CMDriverPackage -Name "DrvPkg01" -ExportFilePath "\\Contoso02\DriverPackages\DriverPackage01.zip"
```

This command exports the driver package named DrvPkg01 to the export file DriverPackage01.zip.

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

### -ExportFilePath
Specifies the full path for the export file.

```yaml
Type: String
Parameter Sets: (All)
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

### -Id
Specifies an array of IDs of driver packages.

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
Specifies a driver package object.
To obtain a **CMDriverPackage** object, use the Get-CMDriverPackage cmdlet.

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
Specifies the name of a driver package.

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
Specifies whether to export the content files for the driver packages and drivers.

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
Specifies whether to export all drivers associated with the driver package.

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

[Get-CMDriverPackage](xref:ConfigurationManager/vlatest/Get-CMDriverPackage.md)

[Import-CMDriverPackage](xref:ConfigurationManager/vlatest/Import-CMDriverPackage.md)

[New-CMDriverPackage](xref:ConfigurationManager/vlatest/New-CMDriverPackage.md)

[Remove-CMDriverPackage](xref:ConfigurationManager/vlatest/Remove-CMDriverPackage.md)

[Set-CMDriverPackage](xref:ConfigurationManager/vlatest/Set-CMDriverPackage.md)


