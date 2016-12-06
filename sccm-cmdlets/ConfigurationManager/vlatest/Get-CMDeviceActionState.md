---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833615
schema: 2.0.0
ms.assetid: 7B562CA1-B1D1-49AF-A7C2-1E47BF36BBB7
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDeviceActionState.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDeviceActionState.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMDeviceActionState

## SYNOPSIS
Gets the state of a device action.

## SYNTAX

### ByName (Default)
```
Get-CMDeviceActionState [[-Action] <DeviceActionType>] [[-Name] <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMDeviceActionState [[-Action] <DeviceActionType>] [-Id] <Int32> [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMDeviceActionState [[-Action] <DeviceActionType>] [-InputObject] <IResultObject> [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceActionState** cmdlet gets the state of an action initiated on a mobile device by using the Invoke-CMDeviceAction cmdlet.

## EXAMPLES

### Example 1: Get the state of a device action using the pipeline
```
PS C:\> Get-CMDevice -Name "WindowsPhone0402" | Get-CMDeviceActionState -Action PinReset
```

This command gets the device object named WindowsPhone0402 and uses the pipeline operator to pass the object to **Get-CMDeviceActionState**, which gets the state of the PIN reset action on the device.

### Example 2: Get the state of a lock action
```
PS C:\> Get-CMDeviceActionState -Name "WindowsPhone0401" -Action Lock
```

This command gets the state of the lock action on the device named WindowsPhone0401.

## PARAMETERS

### -Action
Specifies the action for which you want status.
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

Required: False
Position: 1
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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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
Specifies the ID of a device.

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

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject#SMS_DeviceAction

## NOTES

## RELATED LINKS

[Get-CMDevice](xref:ConfigurationManager/vlatest/Get-CMDevice.md)

[Invoke-CMDeviceAction](xref:ConfigurationManager/vlatest/Invoke-CMDeviceAction.md)


