---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: F43D2D81-0586-4B25-83CA-041B24C9D1DA
online version: https://go.microsoft.com/fwlink/?linkid=833611
schema: 2.0.0
updated_at: 3/15/2017 12:29 AM
ms.date: 3/15/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDevice.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDevice.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/d9f2d13e074e123ab321d322788b43453a59147b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDevice.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMDevice

## SYNOPSIS
Gets a device.

## SYNTAX

### ByName (Default)
```
Get-CMDevice [-Name <String>] [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameMandatory
```
Get-CMDevice -CollectionName <String> [-Name <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDevice -CollectionId <String> [-Name <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] -ThreatId <String> [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] -ThreatName <String> [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] -InputObject <IResultObject> [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMDevice -Collection <IResultObject> [-Name <String>] [-Fast] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMDevice -ResourceId <Int32> [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDevice** cmdlet gets a Microsoft System Center Configuration Manager device.

## EXAMPLES

### Example 1: Get a device by collection ID
```
PS C:\> Get-CMDevice -CollectionID "SMSDM003"
```

This command gets all the device objects in the device collection with the ID of SMSDM003.

### Example 2: Get a device by name
```
PS C:\> Get-CMDevice -CollectionName "All systems" -Name "Win10-86-33"
```

This command gets the device named Win10-86-33 in the device collection named All systems.

## PARAMETERS

### -Collection
Specifies a device collection object. To obtain a device collection object, use the [Get-CMDeviceCollection](./Get-CMDeviceCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
Specifies an ID for a device collection.

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

```yaml
Type: String
Parameter Sets: SearchByIdMandatoryForViewInfectedClients, SearchByNameMandatoryForViewInfectedClients, SearchByValueMandatoryForViewInfectedClients
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a device collection.

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

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance. If lazy properties are not used, this parameter should be specified.

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

### -InputObject
Specifies an object that represents a threat.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatoryForViewInfectedClients
Aliases: Threat

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a device.

```yaml
Type: String
Parameter Sets: ByName, SearchByNameMandatory, SearchByIdMandatory, SearchByValueMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifies the resource ID of a device.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: Id, DeviceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreatId
Specifies an ID of a threat.

```yaml
Type: String
Parameter Sets: SearchByIdMandatoryForViewInfectedClients
Aliases: ThreatNameId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreatName
Specifies a name of a threat.

```yaml
Type: String
Parameter Sets: SearchByNameMandatoryForViewInfectedClients
Aliases:

Required: True
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

[Approve-CMDevice](xref:ConfigurationManager/vlatest/Approve-CMDevice.md)

[Block-CMDevice](xref:ConfigurationManager/vlatest/Block-CMDevice.md)

[Get-CMDeviceCollection](xref:ConfigurationManager/vlatest/Get-CMDeviceCollection.md)

[Remove-CMDevice](xref:ConfigurationManager/vlatest/Remove-CMDevice.md)

[Unblock-CMDevice](xref:ConfigurationManager/vlatest/Unblock-CMDevice.md)
