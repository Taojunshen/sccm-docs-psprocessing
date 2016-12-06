---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833949
schema: 2.0.0
ms.assetid: B4E99D6B-B50F-496B-AFA7-AD795ADA8C8A
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Disable-CMProgram.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Disable-CMProgram.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Disable-CMProgram

## SYNOPSIS
Disables programs in Configuration Manager packages.

## SYNTAX

### SearchByValue (Default)
```
Disable-CMProgram -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdAndNameMandatory
```
Disable-CMProgram -PackageId <String> -ProgramName <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameAndNameMandatory
```
Disable-CMProgram -PackageName <String> -ProgramName <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-CMProgram** cmdlet disables one or more programs in Microsoft System Center Configuration Manager packages.
Programs are commands that are associated with a System Center Configuration Manager package.
Programs identify the actions that occur when the client receives the client package.
You can associate multiple programs with the same package.

You can disable a program to prevent System Center Configuration Manager from running it on client computers where it is currently advertised.
When you disable a program, System Center Configuration Manager still sends the program to distribution points and still advertises the Program on client computers, but Configuration Manager does not display or run the program on the client.
This behavior is the same that occurs when you disable an advertisement with which the program has been associated.

## EXAMPLES

### Example 1: Disable a program
```
PS C:\>Disable-CMProgram -PackageId "CM400007" -ProgramName "ProgramD02"
```

This command disables the program named ProgramD02 in the package that has the ID CM400007.

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

[Enable-CMProgram](xref:ConfigurationManager/vlatest/Enable-CMProgram.md)

[Get-CMProgram](xref:ConfigurationManager/vlatest/Get-CMProgram.md)

[New-CMProgram](xref:ConfigurationManager/vlatest/New-CMProgram.md)

[Remove-CMProgram](xref:ConfigurationManager/vlatest/Remove-CMProgram.md)

[Set-CMProgram](xref:ConfigurationManager/vlatest/Set-CMProgram.md)

[Get-CMPackage](xref:ConfigurationManager/vlatest/Get-CMPackage.md)


