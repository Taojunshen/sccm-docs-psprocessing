---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834259
schema: 2.0.0
ms.assetid: 621E70A5-817B-46A2-ADEA-3D5F5012788F
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMComputerAssociation.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMComputerAssociation.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMComputerAssociation.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMComputerAssociation

## SYNOPSIS
Gets Configuration Manager computer associations.

## SYNTAX

### SearchByName (Default)
```
Get-CMComputerAssociation [-DestinationComputer <String>] [-SourceComputer <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMComputerAssociation -MigrationId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMComputerAssociation** cmdlet gets computer associations.
Microsoft System Center Configuration Manager uses a computer association to migrate user state and settings as part of operating system deployment.
You can specify a source computer, a destination computer, or both.
You can also use an ID to specify a computer association.

## EXAMPLES

### Example 1: Get all computer associations
```
PS C:\> Get-CMComputerAssociation
```

This command gets all the computer associations for System Center Configuration Manager.

### Example 2: Get computer associations for a destination comptuter
```
PS C:\> Get-CMComputerAssociation -DestinationComputer "West155"
```

This command gets all the computer associations for the destination computer named West155.

### Example 3: Get a computer association by using an ID
```
PS C:\> Get-CMComputerAssociation -MigrationId "MID1207"
```

This command gets the computer association that has the ID MID1207.

## PARAMETERS

### -DestinationComputer
Specifies the name of a destination computer.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: RestoreName
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

### -MigrationId
Specifies the ID of a computer association.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceComputer
Specifies the name of a source computer.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: SourceName
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

[New-CMComputerAssociation](xref:ConfigurationManager/vlatest/New-CMComputerAssociation.md)

[Remove-CMComputerAssociation](xref:ConfigurationManager/vlatest/Remove-CMComputerAssociation.md)

[Set-CMComputerAssociation](xref:ConfigurationManager/vlatest/Set-CMComputerAssociation.md)


