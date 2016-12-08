---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833798
schema: 2.0.0
ms.assetid: 1C8CA4A9-A212-4C8C-95ED-E51675AE2F1A
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMOperatingSystemInstaller.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMOperatingSystemInstaller.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMOperatingSystemInstaller

## SYNOPSIS
Gets operating system installers.

## SYNTAX

### SearchByName (Default)
```
Get-CMOperatingSystemInstaller [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMOperatingSystemInstaller -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOperatingSystemInstaller** cmdlet gets one or more operating system installers.
An operating system installer is an installation package that contains all the files that Microsoft System Center Configuration Manager needs to install a Windows operating system on a reference computer.

## EXAMPLES

### Example 1: Get an operating system installer
```
PS C:\> Get-CMOperatingSystemInstaller -Name "OSInstPkg01"-SecuredScopeNames "SecScope02"
```

This command gets the operating system installer named OSInstPkg01 for the security scope named SecScope02.

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
Specifies an array of IDs of operating system installers.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of an operating system installer.

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

[New-CMOperatingSystemInstaller](xref:ConfigurationManager/vlatest/New-CMOperatingSystemInstaller.md)

[Remove-CMOperatingSystemInstaller](xref:ConfigurationManager/vlatest/Remove-CMOperatingSystemInstaller.md)

[Set-CMOperatingSystemInstaller](xref:ConfigurationManager/vlatest/Set-CMOperatingSystemInstaller.md)


