---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833826
schema: 2.0.0
ms.assetid: 634952FD-0028-44EB-A3E8-D6907CDA26DD
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMDriverBootImage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMDriverBootImage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMDriverBootImage

## SYNOPSIS
Adds a driver to a boot image or removes a driver from a boot image.

## SYNTAX

### SetDriverBootImagesById_Id (Default)
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -DriverId <Int32>
 -BootImageId <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDriverBootImagesById_Object
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -DriverId <Int32>
 -BootImage <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesById_Name
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -DriverId <Int32>
 -BootImageName <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDriverBootImagesByName_Id
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -DriverName <String>
 -BootImageId <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDriverBootImagesByName_Name
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -DriverName <String>
 -BootImageName <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDriverBootImagesByName_Object
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -DriverName <String>
 -BootImage <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetDriverBootImagesByObject_Id
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -Driver <IResultObject>
 -BootImageId <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDriverBootImagesByObject_Name
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -Driver <IResultObject>
 -BootImageName <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetDriverBootImagesByObject_Object
```
Set-CMDriverBootImage -SetDriveBootImageAction <SetDriveBootImageActionType> -Driver <IResultObject>
 -BootImage <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDriverBootImage** cmdlet adds a driver to a boot image or removes a driver from a boot image.
You can add Windows device drivers that you have imported into the Microsoft System Center Configuration Manager driver catalog to one or more boot images.
You should add only mass storage device drivers and network adapter device drivers to boot images because other types of drivers are not needed and will increase the size of the boot image.

## EXAMPLES

### Example 1: Add a driver to a boot image
```
PS C:\>Set-CMDriverBootImage -SetDriveBootImageAction AddDriverToBootImage -DriverName "Adaptec Embedded SCSI HostRAID Controller" -BootImageName "Boot image (x64)"
```

This command adds the driver named Adaptec Embedded SCSI HostRAID Controller to the boot image named Boot image (x64).

### Example 2: Remove a driver from a boot image
```
PS C:\>Set-CMDriverBootImage -SetDriveBootImageAction RemoveDriverFromBootImage -DriverName "Adaptec SCSI HostRAID Management Processor Device" -BootImageName "Boot image (x64)"
```

This command removes the driver named Adaptec SCSI HostRAID Management Processor Device from the boot image named Boot image (x64).

## PARAMETERS

### -BootImage
Specifies a **CMBootImage** object.
To obtain a **CMBootImage** object, use the Get-CMBootImage cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetDriverBootImagesById_Object, SetDriverBootImagesByName_Object, SetDriverBootImagesByObject_Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId
Specifies the ID of a boot image.

```yaml
Type: String
Parameter Sets: SetDriverBootImagesById_Id, SetDriverBootImagesByName_Id, SetDriverBootImagesByObject_Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageName
Specifies the name of a boot image.

```yaml
Type: String
Parameter Sets: SetDriverBootImagesById_Name, SetDriverBootImagesByName_Name, SetDriverBootImagesByObject_Name
Aliases: 

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

### -Driver
Specifies a driver object.
To obtain a **CMDriver** object, use the Get-CMDriver cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetDriverBootImagesByObject_Id, SetDriverBootImagesByObject_Name, SetDriverBootImagesByObject_Object
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
Parameter Sets: SetDriverBootImagesById_Id, SetDriverBootImagesById_Object, SetDriverBootImagesById_Name
Aliases: Id, CIId, CI_ID

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
Parameter Sets: SetDriverBootImagesByName_Id, SetDriverBootImagesByName_Name, SetDriverBootImagesByName_Object
Aliases: 

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

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -SetDriveBootImageAction
Specifies the boot image action.
The acceptable values for this parameter are:

- AddDriverToBootImage
- RemoveDriverFromBootImage

```yaml
Type: SetDriveBootImageActionType
Parameter Sets: (All)
Aliases: 
Accepted values: AddDriverToBootImage, RemoveDriverFromBootImage

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

[Get-CMDriver](xref:ConfigurationManager/vlatest/Get-CMDriver.md)


