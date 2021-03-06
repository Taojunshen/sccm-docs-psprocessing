---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833757
schema: 2.0.0
ms.assetid: 1175C860-DAC9-40FA-BFA0-F035CA8126E9
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMComputerAssociation.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMComputerAssociation.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMComputerAssociation.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMComputerAssociation

## SYNOPSIS
Changes settings for a computer association in Configuration Manager.

## SYNTAX

```
Set-CMComputerAssociation -DestinationComputer <String> -SourceComputer <String>
 [-MigrationBehavior <MigrationBehavior>] [-AddMigrationUserName <String[]>]
 [-RemoveMigrationUserName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMComputerAssociation** cmdlet changes settings for a computer association used for migration.
Microsoft System Center Configuration Manager can migrate user state and settings from an existing computer to a different computer as part of operating system deployment.
In the course of migration, System Center Configuration Manager saves accounts created on the source computer and creates those user accounts on the destination computer.

A computer association contains the user names to be migrated and how to deal with other user names from the source computer.
You can use this cmdlet to modify an association.
You can add user names to the association, or remove user names.
You can also change whether System Center Configuration Manager includes other user names from the source computer.

## EXAMPLES

### Example 1: Modify a computer association
```
PS C:\> Set-CMComputerAssociation -DestinationComputer "TSQA155" -SourceComputer "TSQA073" -AddMigrationUserName "ContosoTSQA\EvanNarvaez" -MigrationBehavior CaptureAllUserAccountsAndRestoreSpecifiedAccounts -RemoveMigrationUserName "ContosoTSQA\ElisaDaugherty"
```

This command changes the association between the computer named TSQA073 and TSQA155.
The command adds the user ContosoTSQA\EvanNarvaez and removes the user ContosoTSQA\ElisaDaugherty.
The command specifies the migration behavior as CaptureAllUserAccountsAndRestoreSpecifiedAccounts, so the association causes the migration to save all accounts created on the source computer, but only to create the accounts specified by the computer association on the destination computer.

## PARAMETERS

### -AddMigrationUserName
Specifies an array of user names for accounts created on the source computer.
The cmdlet adds these user names to the current specified user names of the computer association.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
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

### -DestinationComputer
Specifies the name of a destination computer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RestoreName
Required: True
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

### -MigrationBehavior
Specifies how Configuration Manager treats user accounts created on the source computer.
When you create a computer association, specify user accounts created on the source computer by using the *MigrationUserName* parameter of the [New-CMComputerAssociation](./New-CMComputerAssociation.md) cmdlet.
The computer association can specify that the migration process creates some or all of those accounts on the destination computer.

The acceptable values for this parameter are:

- CaptureAllUserAccountsAndRestoreSpecifiedAccounts.
Saves all accounts created on the source computer, but creates only the specified accounts on the destination computer. 
- CaptureAndRestoreAllUserAccounts.
Saves all accounts created on the source computer, and creates them on the destination computer.
- CaptureAndRestoreSpecifiedUserAccounts.
Saves only the specified accounts from the source computer, and creates those accounts on the destination computer.

```yaml
Type: MigrationBehavior
Parameter Sets: (All)
Aliases: 
Accepted values: CaptureAndRestoreAllUserAccounts, CaptureAllUserAccountsAndRestoreSpecifiedAccounts, CaptureAndRestoreSpecifiedUserAccounts
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveMigrationUserName
Specifies an array of user names for accounts created on the source computer.
The cmdlet removes these user names from current specified user names of the computer association.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceComputer
Specifies the name of the source computer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceName
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

[Get-CMComputerAssociation](xref:ConfigurationManager/vlatest/Get-CMComputerAssociation.md)

[New-CMComputerAssociation](xref:ConfigurationManager/vlatest/New-CMComputerAssociation.md)

[Remove-CMComputerAssociation](xref:ConfigurationManager/vlatest/Remove-CMComputerAssociation.md)
