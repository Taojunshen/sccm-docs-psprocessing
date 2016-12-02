---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834274
schema: 2.0.0
ms.assetid: 94BE72CA-AAE0-47C1-8C05-1BAF02B798A0
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMBootImage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/New-CMBootImage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMBootImage

## SYNOPSIS
Adds a new operating system boot image.

## SYNTAX

```
New-CMBootImage -Path <String> -Index <Int32> -Name <String> [-Version <String>] [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMBootImage** cmdlet adds a new Windows Preinstallation Environment (Windows PE) operating system boot image to Microsoft System Center Configuration Manager.
Operating system images are .wim format files.
These files contain a compressed set of reference files and folders that are required to successfully install and configure a boot image on a computer.
By default, System Center Configuration Manager includes both x86 and x64 operating system images.

You must run **New-CMBootImage** on the computer that is running the Systems Management Server (SMS) provider.
The computer account of the computer that is running the SMS provider must have Read and Write access to the package source of the boot image.
For more information about the SMS provider, see [Planning for the SMS Provider in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=263566) on TechNet.

## EXAMPLES

### Example 1: Create a new boot image object
```
PS C:\>New-CMBootImage -Path "\\Server99.Contoso.com\SMS_CCC\osd\boot\i386\boot.wim" -Index 1 -Name "WinPE Boot Image" -Version 11 -Description "WinPE Boot Image x86 Approved 9/1/2012"
```

This command creates a new boot image object and provides it with a source path for its WIM file, an index value, a name, an operating system version, and a description.

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

### -Description
Specifies a description of the boot image.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

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

### -Index
Specifies an index.
An index is the number of an image in a .wim file.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ImageIndex

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a new boot image.

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

### -Path
Specifies the location of the original WIM file for the boot image.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ImagePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies the version of the boot image.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

[Planning for the SMS Provider in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=263566)

[Get-CMBootImage](xref:ConfigurationManager/vlatest/Get-CMBootImage.md)

[Remove-CMBootImage](xref:ConfigurationManager/vlatest/Remove-CMBootImage.md)

[Set-CMBootImage](xref:ConfigurationManager/vlatest/Set-CMBootImage.md)

