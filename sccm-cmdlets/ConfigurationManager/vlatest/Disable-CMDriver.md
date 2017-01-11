---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833945
schema: 2.0.0
ms.assetid: DC4B2713-2B9D-45B0-A595-00407274F314
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Disable-CMDriver.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Disable-CMDriver.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Disable-CMDriver.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Disable-CMDriver

## SYNOPSIS
Disables a device driver.

## SYNTAX

### SearchByValueMandatory (Default)
```
Disable-CMDriver -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Disable-CMDriver -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Disable-CMDriver -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Disable-CMDriver** cmdlet disables a device driver in Microsoft System Center Configuration Manager.
To enable the driver, use the [Enable-CMDriver](./EnableCMDriver.md) cmdlet.

## EXAMPLES

### Example 1: Disable a device driver
```
PS C:\> $Driver = Get-CMDriver -Name "Driver01"
PS C:\> Disable-CMDriver -InputObject $Driver
```

The first command gets the driver object named Driver01 and stores the object in the $Driver variable.

The second command disables the driver stored in $Driver.

### Example 2: Disable a device driver by using the pipeline
```
PS C:\> Get-CMDriver -Name "Driver02" | Disable-CMDriver
```

This command gets the driver object named Driver02 and uses the pipeline operator to pass the object to **Disable-CMDriver**, which disables the driver object.

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
Specifies the ID of a driver.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a driver object.
To obtain a driver object, use the [Get-CMDriver](./Get-CMDriver.md) cmdlet.

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
Specifies the name of a driver.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName
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

[Enable-CMDriver](xref:ConfigurationManager/vlatest/Enable-CMDriver.md)

[Import-CMDriver](xref:ConfigurationManager/vlatest/Import-CMDriver.md)

[Get-CMDriver](xref:ConfigurationManager/vlatest/Get-CMDriver.md)

[Remove-CMDriver](xref:ConfigurationManager/vlatest/Remove-CMDriver.md)

[Set-CMDriver](xref:ConfigurationManager/vlatest/Set-CMDriver.md)

[Get-CMDriverPackage](xref:ConfigurationManager/vlatest/Get-CMDriverPackage.md)
