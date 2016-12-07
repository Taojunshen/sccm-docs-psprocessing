---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833668
schema: 2.0.0
ms.assetid: FFDDED71-D9A4-4974-A61E-F4325BCEADC4
updated_at: 12/7/2016 5:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDriverPackage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/f3e8fe7234dce2881d15465fb1eb6990d1f03567/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDriverPackage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMDriverPackage

## SYNOPSIS
Gets a driver package.

## SYNTAX

### SearchByName (Default)
```
Get-CMDriverPackage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDriverPackage -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDriverPackage** cmdlet gets a driver package.

## EXAMPLES

### Example 1: Get a driver package that is specified by its identifier
```
PS C:\>Get-CMDriverPackage -Id "CM100042"
```

This command gets a driver package that is specified by its identifier.

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

### -Id
Specifies an array of identifiers for a driver package.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: PackageId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a driver package.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Export-CMDriverPackage](xref:ConfigurationManager/vlatest/Export-CMDriverPackage.md)

[Import-CMDriverPackage](xref:ConfigurationManager/vlatest/Import-CMDriverPackage.md)

[New-CMDriverPackage](xref:ConfigurationManager/vlatest/New-CMDriverPackage.md)

[Remove-CMDriverPackage](xref:ConfigurationManager/vlatest/Remove-CMDriverPackage.md)

[Set-CMDriverPackage](xref:ConfigurationManager/vlatest/Set-CMDriverPackage.md)
