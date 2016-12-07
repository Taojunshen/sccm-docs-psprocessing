---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833815
schema: 2.0.0
ms.assetid: ABD06920-8C34-4C90-8E38-929E2897A780
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/New-CMVhd.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/New-CMVhd.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# New-CMVhd

## SYNOPSIS
Creates a VHD image.

## SYNTAX

```
New-CMVhd -Name <String> -VhdFilePath <String> [-Version <String>] [-Description <String>]
 -TaskSequencePackageId <String> -DistributionPointServerName <String[]> [-VhdSizeGB <Int32>]
 [-Timeout <TimeSpan>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMVhd** cmdlet creates a virtual hard disk (VHD) image by using the operating system deployment feature.

## EXAMPLES

### Example 1: Create a VHD image
```
PS C:\>New-CMVhd -Name "Windows 10 Enterprise " -Path "\\vhd-server\hyper-v\ Windows10.vhd" -VHDSize 50 -TaskSequencePackageId "P0071267" -DistributionPointServerNames "distribution-server.contoso.com" -Version "X64"
```

This command creates a virtual hard disk (VHD) image named Windows 10 Enterprise, and then copies the VHD image file to the distribution point that is named distribution-server.contoso.com.

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
Specifies a description for the VHD.

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

### -DistributionPointServerName


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DistributionPointServerNames
Required: True
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
Specifies the name of a VHD image.

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

### -TaskSequencePackageId
Specifies an ID for a task sequence package.

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

### -Timeout


```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies a version for the VHD.
Use any string.

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

### -VhdFilePath


```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath, Path
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdSizeGB


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: VhdSize
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

[Get-CMVhd](xref:ConfigurationManager/vlatest/Get-CMVhd.md)

[Remove-CMVhd](xref:ConfigurationManager/vlatest/Remove-CMVhd.md)

[Set-CMVhd](xref:ConfigurationManager/vlatest/Set-CMVhd.md)


