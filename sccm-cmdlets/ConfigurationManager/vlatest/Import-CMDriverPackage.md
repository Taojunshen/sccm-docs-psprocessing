---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834062
schema: 2.0.0
ms.assetid: 2E251111-93BB-4D25-AD73-C7C1C316E253
updated_at: 12/7/2016 9:59 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMDriverPackage.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMDriverPackage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/f515f556ebbba15d2592786d6aad82ee381435ec/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMDriverPackage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Import-CMDriverPackage

## SYNOPSIS
Imports a driver package.

## SYNTAX

```
Import-CMDriverPackage -ImportFilePath <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMDriverPackage** cmdlet imports a driver packages to Microsoft System Center Configuration Manager.
You can use the [Export-CMDriverPackage](./Export-CMDriverPackage.md) cmdlet to export a driver package to a .zip file.

## EXAMPLES

### Example 1: Import a driver package
```
PS C:\>Import-CMDriverPackage -ImportFilePath "\\Contoso02\main\driverpackages\DriverPackage.zip"
```

This command imports a driver package from the import file named DriverPackage.zip.

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

### -ImportFilePath
Specifies the Universal Naming Convention (UNC) path of the import file.

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

[Export-CMDriverPackage](xref:ConfigurationManager/vlatest/Export-CMDriverPackage.md)

[Get-CMDriverPackage](xref:ConfigurationManager/vlatest/Get-CMDriverPackage.md)

[New-CMDriverPackage](xref:ConfigurationManager/vlatest/New-CMDriverPackage.md)

[Remove-CMDriverPackage](xref:ConfigurationManager/vlatest/Remove-CMDriverPackage.md)

[Set-CMDriverPackage](xref:ConfigurationManager/vlatest/Set-CMDriverPackage.md)


