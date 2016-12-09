---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834285
schema: 2.0.0
ms.assetid: F3E1E495-47DC-4EA2-BC27-6BCB1F7A9B7B
updated_at: 12/7/2016 11:21 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCaptureMedia.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCaptureMedia.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4bb0549ab9452d0d1c9cdf57cfbc8185eefd798c/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCaptureMedia.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# New-CMCaptureMedia

## SYNOPSIS
Creates capture media.

## SYNTAX

```
New-CMCaptureMedia [-AllowUacPrompt] -BootImage <IResultObject> -DistributionPoint <IResultObject[]> [-Force]
 [-FormatMedia] -MediaType <MediaInputType> -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCaptureMedia** cmdlets creates media used to capture an operating system deployment image from a reference computer.

NOTE: This cmdlet requires elevated permissions to run.

## EXAMPLES

### Example 1: Create capture media
```
PS C:\> $BootImage = Get-CMBootImage -Name "Boot image (x64)"
PS C:\> $DistributionPoint = Get-CMDistributionpoint -SiteCode CM1
PS C:\> New-CMCaptureMedia -MediaType CdDvd -Path "\\server\share\CaptureMedia.iso" -BootImage $BootImage -DistributionPoint $DistributionPoint
```

The first command gets the boot image object named Boot image (x64) and stores the object in the $BootImage variable.

The second command gets the distribution point object for the site code named CM1 and stores the object in the $DistributionPoint variable.

The last command creates capture media using the BootImage stored in $BootImage, and the distribution point stored in $DistributionPoint.

## PARAMETERS

### -AllowUacPrompt
Indicates that User Account Control (UAC) prompts are allowed.

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

### -BootImage
Specifies a boot image object.
To obtain a boot image object, use the [Get-CMBootImage](./Get-CMBootImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: BootImagePackage
Required: True
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

### -DistributionPoint
Specifies an array of distribution point objects.
To obtain a distribution point object, use the [Get-CMDistributionPoint](./Get-CMDistributionPoint.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DistributionPoints
Required: True
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

### -FormatMedia
Indicates that the cmdlet formats the removable USB drive (FAT32), and makes it bootable.

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

### -MediaType
Specifies the media mode.
Valid values are: 

- Usb
- CdDvd
- Hd

```yaml
Type: MediaInputType
Parameter Sets: (All)
Aliases: 
Accepted values: Usb, CdDvd
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the name and path where the output files are written.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MediaPath, OutputPath, DriveName
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

[Get-CMBootImage](xref:ConfigurationManager/vlatest/Get-CMBootImage.md)

[Get-CMDistributionPoint](xref:ConfigurationManager/vlatest/Get-CMDistributionPoint.md)


