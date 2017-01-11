---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833587
schema: 2.0.0
ms.assetid: 762F1090-8DA6-46BC-A4E7-876E1A7A5511
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Save-CMEndpointProtectionDefinition.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Save-CMEndpointProtectionDefinition.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Save-CMEndpointProtectionDefinition.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Save-CMEndpointProtectionDefinition

## SYNOPSIS
Saves an Endpoint Protection definition.

## SYNTAX

### SearchByValueMandatory (Default)
```
Save-CMEndpointProtectionDefinition [-DeviceName <String>] [-DeviceId <String>] [-Device <IResultObject>]
 -DeviceCollection <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Save-CMEndpointProtectionDefinition [-DeviceName <String>] [-DeviceId <String>] [-Device <IResultObject>]
 -DeviceCollectionName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Save-CMEndpointProtectionDefinition [-DeviceName <String>] [-DeviceId <String>] [-Device <IResultObject>]
 -DeviceCollectionId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Save-CMEndpointProtectionDefinition** cmdlet saves a System Center 2016 Endpoint Protection definition in Microsoft System Center Configuration Manager.
Endpoint Protection definitions contain anti-malware policies and settings for Windows Firewall that you can apply to specific groups of computers.

For more information about Endpoint Protection, see [Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?linkid=268427) on TechNet.

## EXAMPLES

### Example 1: Save an Endpoint Protection epshort definition by using a device collection nameepshortEndpoint Protection
```
PS C:\> Save-CMEndpointProtectionDefinition -DeviceCollectionName "NA-Client-Devices"
```

This command saves the Endpoint Protection definition to the devices in the device collection named NA-Client-Devices.

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

### -Device
Specifies a device object in Configuration Manager.
To obtain a device object, use the [Get-CMDevice](./Get-CMDevice.md) cmdlet.
This object identifies the device to which you save the Endpoint Protection definition.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceCollection
Specifies a device collection object in Configuration Manager.
To obtain a device collection object, use the [Get-CMDeviceCollection](./Get-CMDeviceCollection.md) cmdlet.
This object identifies the device collection to which you save the Endpoint Protection definition.

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

### -DeviceCollectionId
Specifies an ID for a Configuration Manager device collection to which you add the Endpoint Protection definition.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceCollectionName
Specifies a name for a Configuration Manager device collection to which you add the Endpoint Protection definition.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceId
Specifies the ID of a Configuration Manager device to which you add the Endpoint Protection definition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceID
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies the name of a Configuration Manager device to which you save the Endpoint Protection definition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name
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

[Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?linkid=268427)

[Add-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Add-CMEndpointProtectionPoint.md)

[Get-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Get-CMEndpointProtectionPoint.md)

[Remove-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Remove-CMEndpointProtectionPoint.md)

[Get-CMDevice](xref:ConfigurationManager/vlatest/Get-CMDevice.md)

[Get-CMDeviceCollection](xref:ConfigurationManager/vlatest/Get-CMDeviceCollection.md)


