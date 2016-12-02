---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833793
schema: 2.0.0
ms.assetid: 3057C77C-7B9C-4413-AC06-DF8A17AD448C
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMOperatingSystemImageUpdateSchedule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMOperatingSystemImageUpdateSchedule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMOperatingSystemImageUpdateSchedule

## SYNOPSIS
Retrieves an operating system image update schedule object in Configuration Manager.

## SYNTAX

### SearchByName (Default)
```
Get-CMOperatingSystemImageUpdateSchedule [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMOperatingSystemImageUpdateSchedule -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMOperatingSystemImageUpdateSchedule -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOperatingSystemImageUpdateSchedule** cmdlet retrieves an object that represents an operating system image update schedule in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Retrieve the operating system image update schedule
```
PS C:\>Get-CMOperatingSystemImageUpdateSchedule -Id "1207"
```

This command retrieves the operating system image update schedule identified by the ID 1207.

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
Specifies an array of IDs of operating system image update schedules in Configuration Manager.

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

### -InputObject
Specifies an operating system image update schedule object in Configuration Manager.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name


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

[Clear-CMOperatingSystemImageUpdateSchedule](xref:ConfigurationManager/vlatest/Clear-CMOperatingSystemImageUpdateSchedule.md)

