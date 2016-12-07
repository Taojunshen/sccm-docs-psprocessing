---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834081
schema: 2.0.0
ms.assetid: C1210FA1-5B24-439D-858B-D97280BA8236
updated_at: 12/6/2016 11:13 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMDriverFromDriverPackage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/d1c6f0eeb340f832b2254d78bbd1bc9245dc24fc/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMDriverFromDriverPackage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMDriverFromDriverPackage

## SYNOPSIS
Removes a driver from a driver package.

## SYNTAX

### RemoveDriverFromDriverPackageById_Id (Default)
```
Remove-CMDriverFromDriverPackage [-Force] -DriverId <Int32> -DriverPackageId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDriverFromDriverPackageById_Object
```
Remove-CMDriverFromDriverPackage [-Force] -DriverId <Int32> -DriverPackage <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDriverFromDriverPackageById_Name
```
Remove-CMDriverFromDriverPackage [-Force] -DriverId <Int32> -DriverPackageName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Id
```
Remove-CMDriverFromDriverPackage [-Force] -DriverName <String> -DriverPackageId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Name
```
Remove-CMDriverFromDriverPackage [-Force] -DriverName <String> -DriverPackageName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByName_Object
```
Remove-CMDriverFromDriverPackage [-Force] -DriverName <String> -DriverPackage <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Name
```
Remove-CMDriverFromDriverPackage [-Force] -Driver <IResultObject> -DriverPackageName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Id
```
Remove-CMDriverFromDriverPackage [-Force] -Driver <IResultObject> -DriverPackageId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDriverFromDriverPackageByObject_Object
```
Remove-CMDriverFromDriverPackage [-Force] -Driver <IResultObject> -DriverPackage <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDriverFromDriverPackage** cmdlet removes a driver from a driver package in Microsoft System Center Configuration Manager.
When you remove a driver from a driver package, the device driver content is deleted from the source directory share for the driver package.

## EXAMPLES

### Example 1: Remove a driver from a driver package
```
PS C:\>Remove-CMDriverfromDriverPackage -DriverName "Adaptec Embedded SCSI HostRAID Controller" -DriverPackageName "DrvPkg01"
```

This command removes the driver named Adaptec Embedded SCSI HostRAID Controller from the boot image named DrvPkg01.

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

### -Driver
Specifies a driver object.
To obtain a **CMDriver** object, use the [Get-CMDriver](./Get-CMDriver.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveDriverFromDriverPackageByObject_Name, RemoveDriverFromDriverPackageByObject_Id, RemoveDriverFromDriverPackageByObject_Object
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DriverId
Specifies the ID of a driver.

```yaml
Type: Int32
Parameter Sets: RemoveDriverFromDriverPackageById_Id, RemoveDriverFromDriverPackageById_Object, RemoveDriverFromDriverPackageById_Name
Aliases: CIId, Id, CI_ID
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverName
Specifies the name of a driver.

```yaml
Type: String
Parameter Sets: RemoveDriverFromDriverPackageByName_Id, RemoveDriverFromDriverPackageByName_Name, RemoveDriverFromDriverPackageByName_Object
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackage
Specifies a **CMDriverPackage** object.
To obtain a **CMDriverPackage** object, use the [Get-CMDriverPackage](./Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveDriverFromDriverPackageById_Object, RemoveDriverFromDriverPackageByName_Object, RemoveDriverFromDriverPackageByObject_Object
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DriverPackageId
Specifies the ID of a driver package.

```yaml
Type: String
Parameter Sets: RemoveDriverFromDriverPackageById_Id, RemoveDriverFromDriverPackageByName_Id, RemoveDriverFromDriverPackageByObject_Id
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageName
Specifies the name of a driver package.

```yaml
Type: String
Parameter Sets: RemoveDriverFromDriverPackageById_Name, RemoveDriverFromDriverPackageByName_Name, RemoveDriverFromDriverPackageByObject_Name
Aliases: 
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

[Add-CMDriverToDriverPackage](xref:ConfigurationManager/vlatest/Add-CMDriverToDriverPackage.md)

[Get-CMDriver](xref:ConfigurationManager/vlatest/Get-CMDriver.md)


