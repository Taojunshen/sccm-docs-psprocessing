---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833987
schema: 2.0.0
ms.assetid: 3075773B-6EDE-4F06-96B1-9B909098F9F6
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Enable-CMProgram.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Enable-CMProgram.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Enable-CMProgram

## SYNOPSIS
Enables programs in Configuration Manager packages.

## SYNTAX

### SearchByValue (Default)
```
Enable-CMProgram -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdAndNameMandatory
```
Enable-CMProgram -PackageId <String> -ProgramName <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameAndNameMandatory
```
Enable-CMProgram -PackageName <String> -ProgramName <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-CMProgram** cmdlet enables one or more programs in Microsoft System Center Configuration Manager packages.
You can enable a program that has been disabled in order to resume availability of that program to client computers.
You can also enable a program by enabling an advertisement that you used to disable it.

Programs are commands that are associated with a System Center Configuration Manager package.
Programs identify the actions that occur when the client receives the client package.
You can associate multiple programs with the same package.

## EXAMPLES

### Example 1: Enable a program
```
PS C:\>Enable-CMProgram -PackageId "CM400007" -ProgramName "ProgramD02"
```

This command enables the program named ProgramD02 in the package that has the ID CM400007.

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

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Program
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PackageId
Specifies an array of package IDs.

```yaml
Type: String
Parameter Sets: SearchByIdAndNameMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName
Specifies an array of package names.

```yaml
Type: String
Parameter Sets: SearchByNameAndNameMandatory
Aliases: 
Required: True
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

### -ProgramName
Specifies an array of program names.

```yaml
Type: String
Parameter Sets: SearchByIdAndNameMandatory, SearchByNameAndNameMandatory
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

[Disable-CMProgram](xref:ConfigurationManager/vlatest/Disable-CMProgram.md)

[Get-CMProgram](xref:ConfigurationManager/vlatest/Get-CMProgram.md)

[New-CMProgram](xref:ConfigurationManager/vlatest/New-CMProgram.md)

[Remove-CMProgram](xref:ConfigurationManager/vlatest/Remove-CMProgram.md)

[Set-CMProgram](xref:ConfigurationManager/vlatest/Set-CMProgram.md)

[Get-CMPackage](xref:ConfigurationManager/vlatest/Get-CMPackage.md)


