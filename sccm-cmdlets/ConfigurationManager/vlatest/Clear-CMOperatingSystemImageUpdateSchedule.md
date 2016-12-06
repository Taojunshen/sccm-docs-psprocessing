---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833846
schema: 2.0.0
ms.assetid: 522EDC95-F732-4237-B269-59AE6D0CC370
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Clear-CMOperatingSystemImageUpdateSchedule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Clear-CMOperatingSystemImageUpdateSchedule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Clear-CMOperatingSystemImageUpdateSchedule

## SYNOPSIS
Removes a schedule for updating an operating system image.

## SYNTAX

### SearchByValueMandatory (Default)
```
Clear-CMOperatingSystemImageUpdateSchedule -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Clear-CMOperatingSystemImageUpdateSchedule -Id <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Clear-CMOperatingSystemImageUpdateSchedule -Name <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Clear-CMOperatingSystemImageUpdateSchedule** cmdlet removes a schedule for updating an operating system image from a Microsoft System Center Configuration Manager site.

Operating system images are .wim format files, which represent a compressed collection of reference files and folders that System Center Configuration Manager requires to successfully install and configure an operating system on a computer.
You can use System Center Configuration Manager to define a schedule for updating these images by using Component Based Servicing (CBS), then delete unwanted schedules by using this cmdlet.

## EXAMPLES

### Example 1: Remove a schedule for updating an operating system image by using a name
```
PS C:\>Clear-CMOperatingSystemUpdateSchedule -OperatingSystemImageName "Win8UpdateSchedule"
```

This command removes a schedule named Win8UpdateSchedule that updates an operating system image.

### Example 2: Remove a schedule for updating an operating system image by using an object
```
PS C:\>$Win8UpdateSchedule = Get-CMOperatingSystemUpdateSchedule -Id 1207
PS C:\> Clear-CMOperatingSystemImageUpdateSchedule -OperatingSystemImageName "Win8UpdateSchedule"
```

The first command gets the image update schedule by using the ID 1207.
The command stores this schedule in the $UpdateSchedObject variable.

The second command removes the image update schedule by using $UpdateSchedObject.

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

### -Id


```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: OperatingSystemImageId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: OperatingSystemImage, ServicingSchedule
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name


```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: OperatingSystemImageName
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

[Get-CMOperatingSystemImageUpdateSchedule](xref:ConfigurationManager/vlatest/Get-CMOperatingSystemImageUpdateSchedule.md)


