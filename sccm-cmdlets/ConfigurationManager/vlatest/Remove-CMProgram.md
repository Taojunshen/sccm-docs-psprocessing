---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834163
schema: 2.0.0
ms.assetid: 5118DE8E-70F4-4352-83AA-81EFEA354785
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMProgram.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMProgram.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMProgram.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMProgram

## SYNOPSIS
Removes programs from a Configuration Manager package.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMProgram -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdAndNameMandatory
```
Remove-CMProgram -PackageId <String> -ProgramName <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMProgram** cmdlet removes one or more programs from a Microsoft System Center Configuration Manager package.
Programs are commands that are associated with a System Center Configuration Manager package.
Programs identify the actions that occur when the client receives the client package.
You can associate multiple programs with the same package.

When you remove a program from a package, System Center Configuration Manager updates the package information in the System Center Configuration Manager site database.
System Center Configuration Manager removes all of the advertisements for this program from the database and removes the advertisements from clients that have received them.
If System Center Configuration Manager has already run the advertised program on the client computer, System Center Configuration Manager does not remove the software.

## EXAMPLES

### Example 1: Remove a program by using a name and an ID
```
PS C:\> Remove-CMProgram -PackageId "ST10000F" -ProgramName "ProgramD02"
```

This command removes the program named ProgramD02 from the package that has the ID ST10000F.

### Example 2: Remove a program by using an object variable
```
PS C:\> $Prog = Get-CMProgram -Name "ProgramD02" -PackageId "ST10000F"
PS C:\> Remove-CMProgram -InputObject $Prog
```

The first command gets the program named ProgramD02 in the package that has the ID ST10000F.
The command stores the results in the $Prog variable.

The second command removes program in $Prog.

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

### -InputObject
Specifies a **CMProgram** object.
To obtain a **CMProgram** object, use the Get-CMProgram cmdlet.

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

### -PackageId
Specifies the package that contains the program by using an ID.

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

### -ProgramName
Specifies the program within the package by using a name.

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

[Enable-CMProgram](xref:ConfigurationManager/vlatest/Enable-CMProgram.md)

[Get-CMProgram](xref:ConfigurationManager/vlatest/Get-CMProgram.md)

[New-CMProgram](xref:ConfigurationManager/vlatest/New-CMProgram.md)

[Set-CMProgram](xref:ConfigurationManager/vlatest/Set-CMProgram.md)


