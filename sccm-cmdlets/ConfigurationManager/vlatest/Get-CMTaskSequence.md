---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833962
schema: 2.0.0
ms.assetid: 3D651458-AAB7-4D25-933A-935F8DE730D9
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMTaskSequence.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMTaskSequence.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMTaskSequence.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMTaskSequence

## SYNOPSIS
Gets Configuration Manager task sequences.

## SYNTAX

### SearchByName (Default)
```
Get-CMTaskSequence [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMTaskSequence -TaskSequencePackageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMTaskSequence** cmdlet gets Microsoft System Center Configuration Manager task sequences.
A task sequence includes configuration and operating system deployment settings for a System Center Configuration Manager client computer.

You can specify a name or ID to get a specific sequence.
You can also specify a security scope, by itself or with a name or ID, to get sequences with that security scope.

## EXAMPLES

### Example 1: Get a task sequence by name
```
PS C:\> Get-CMTaskSequence -Name "taskSequence"
```

This command gets the task sequence named taskSequence.

## PARAMETERS

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

### -Name
Specifies a name for a task sequence.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequencePackageId
Specifies the ID of a task sequence package.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId, Id
Required: True
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

[Disable-CMTaskSequence](xref:ConfigurationManager/vlatest/Disable-CMTaskSequence.md)

[Enable-CMTaskSequence](xref:ConfigurationManager/vlatest/Enable-CMTaskSequence.md)

[Export-CMTaskSequence](xref:ConfigurationManager/vlatest/Export-CMTaskSequence.md)

[Import-CMTaskSequence](xref:ConfigurationManager/vlatest/Import-CMTaskSequence.md)

[New-CMTaskSequence](xref:ConfigurationManager/vlatest/New-CMTaskSequence.md)

[Remove-CMTaskSequence](xref:ConfigurationManager/vlatest/Remove-CMTaskSequence.md)

[Set-CMTaskSequence](xref:ConfigurationManager/vlatest/Set-CMTaskSequence.md)


