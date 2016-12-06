---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834067
schema: 2.0.0
ms.assetid: 1AB14130-5DCA-4803-B9ED-2E9105D24872
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMPackage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMPackage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Import-CMPackage

## SYNOPSIS
Imports a Configuration Manager package.

## SYNTAX

```
Import-CMPackage -ImportFilePath <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMPackage** cmdlet imports a Microsoft System Center Configuration Manager package.
You can use this cmdlet to import a package of collections, queries, or reports so that you can later deploy these items to a different location.

## EXAMPLES

### Example 1: Import a package
```
PS C:\>Import-CMPackage -ImportFilePath "\\Deploy01\ExportPackages"
```

This command imports a package from the path \\\\Deploy01\ExportPackages.

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
Specifies the Universal Naming Convention (UNC) path for the file package that contains the package that you import.
The cmdlet imports all packages that the file package contains.

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

[Export-CMPackage](xref:ConfigurationManager/vlatest/Export-CMPackage.md)

[Get-CMPackage](xref:ConfigurationManager/vlatest/Get-CMPackage.md)

[New-CMPackage](xref:ConfigurationManager/vlatest/New-CMPackage.md)

[Remove-CMPackage](xref:ConfigurationManager/vlatest/Remove-CMPackage.md)

[Set-CMPackage](xref:ConfigurationManager/vlatest/Set-CMPackage.md)


