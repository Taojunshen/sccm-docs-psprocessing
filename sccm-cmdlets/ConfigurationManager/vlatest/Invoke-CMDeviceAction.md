---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834125
schema: 2.0.0
ms.assetid: B2F9AD76-2083-44CA-A964-D58F7E7A9A07
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMDeviceAction.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMDeviceAction.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Invoke-CMDeviceAction

## SYNOPSIS
Initiates a remote action on a mobile device.

## SYNTAX

### ByValue (Default)
```
Invoke-CMDeviceAction [-InputObject] <IResultObject> [-Action] <DeviceActionType> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Invoke-CMDeviceAction [-Name] <String> [-Action] <DeviceActionType> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Invoke-CMDeviceAction [-Id] <Int32> [-Action] <DeviceActionType> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMDeviceAction** cmdlet initiates a remote action, such as locking or resetting a PIN for, a mobile device.
This cmdlet only works on mobile devices.

## EXAMPLES

### Example 1: Lock a mobile device
```
PS C:\> Get-CMDevice -Name "WindowsPhone0401" | Invoke-CMDeviceAction -Action Lock
```

This command gets the device object named WindowsPhone0401 and uses the pipeline operator to pass the object to **Invoke-CMDeviceAction**, which locks the device.

### Example 2: Reset the PIN for a mobile device
```
PS C:\> Invoke-CMDeviceAction -Name "WindowsPhone0402" -Action PinReset -PassThru
```

This command resets the PIN for the device named WindowsPhone0402.

## PARAMETERS

### -Action
Specifies the action you want to initiate on the device.
Valid values are: 

- Lock
- PinReset
- BypassActivationLock
- RequestNewActivationLockCode
- Unknown

```yaml
Type: DeviceActionType
Parameter Sets: (All)
Aliases: 
Accepted values: Lock, PinReset, BypassActivationLock, RequestNewActivationLockCode

Required: True
Position: 1
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
Specifies an ID for a device.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a device object.
To obtain a device object, use the Get-CMDevice cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Device

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a device.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
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

[Get-CMDevice](xref:ConfigurationManager/vlatest/Get-CMDevice.md)


