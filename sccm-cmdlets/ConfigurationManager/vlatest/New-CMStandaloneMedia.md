---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833778
schema: 2.0.0
ms.assetid: 7715E46A-AE0E-47C1-86B5-AC56F7BAD28C
updated_at: 12/7/2016 11:21 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMStandaloneMedia.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMStandaloneMedia.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4bb0549ab9452d0d1c9cdf57cfbc8185eefd798c/sccm-cmdlets/ConfigurationManager/vlatest/New-CMStandaloneMedia.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMStandaloneMedia

## SYNOPSIS
Creates stand-alone media.

## SYNTAX

```
New-CMStandaloneMedia [-IncludeApplicationDependency] [-MediaSize <MediaSize>] -TaskSequence <IResultObject>
 [-AllowUacPrompt] [-AllowUnattended] [-CertificatePath <String>] -DistributionPoint <IResultObject[]> [-Force]
 [-FormatMedia] [-MediaPassword <SecureString>] -MediaType <MediaInputType> -Path <String>
 [-PrestartCommand <String>] [-PrestartPackage <IResultObject>] [-Variable <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMStandaloneMedia** cmdlet creates media used to deploy operating systems without network access.

NOTE: This cmdlet requires elevated permissions to run.

## EXAMPLES

### Example 1: Create stand-alone media using variables
```
PS C:\> $TaskSequence = Get-CMTaskSequence -Name "TaskSequence01"
PS C:\> $DistributionPoint = Get-CMDistributionpoint -SiteCode CM1
PS C:\> New-CMStandaloneMedia -MediaType CdDvd -Path \\server\share\standaloneMedia.iso -TaskSequence $TaskSequence -DistributionPoint $DistributionPoint
```

The first command gets the task sequence object named TaskSequence01 and stores the object in the $TaskSequence variable.

The second command gets the distribution point object for the site code named CM1 and stores the object in the $DistributionPoint variable.

The last command creates stand-alone media using the task sequence stored in $TaskSequence and the distribution point stored in $DistributionPoint.

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

### -AllowUnattended
Indicates that unattended operating system deployments are allowed.
An unattended operating system deployment does not prompt for network configuration or optional task sequences.

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

### -CertificatePath
Specifies a path from which to import a PKI certificate.

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

### -IncludeApplicationDependency
Indicates that the cmdlet detects associated application dependencies and adds them to this media.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: IncludeApplicationDependencies
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaPassword
Specifies, as a secure string, a password to protect task sequence media.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaSize
Specifies the size of the media.
Valid values are: 

- None
- Size4GB
- Size8GB
- Size650MB
- SizeUnlimited

```yaml
Type: MediaSize
Parameter Sets: (All)
Aliases: 
Accepted values: None, Size650MB, Size4GB, Size8GB, SizeUnlimited
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaType
Specifies the media type.
Valid values are: 

- CdDvd
- Usb
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

### -PrestartCommand
Specifies a prestart command that will run before the task sequence runs.
A prestart command is a script or an executable that can interact with the user in Windows PE before the task sequence runs to install the operating system.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PreExecCommandLine
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestartPackage
Specifies a package object that contains files for the prestart command.
To obtain a package object, use the [Get-CMPackage](./Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequence
Specifies a task sequence object.
To obtain a task sequence object, use the [Get-CMTaskSequence](./Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable
Specifies a task sequence variable.
A task sequence variable is a name/value pair that is used during the task sequence deployment.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: TaskSequenceVariables, Variables
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

[Get-CMDistributionPoint](xref:ConfigurationManager/vlatest/Get-CMDistributionPoint.md)

[Get-CMPackage](xref:ConfigurationManager/vlatest/Get-CMPackage.md)

[Get-CMTaskSequence](xref:ConfigurationManager/vlatest/Get-CMTaskSequence.md)


