---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834005
schema: 2.0.0
ms.assetid: 94996A97-9D9F-428F-B198-DFB589398780
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMUserDeviceAffinityRequest.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMUserDeviceAffinityRequest.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMUserDeviceAffinityRequest

## SYNOPSIS
Gets a request for user device affinity in Configuration Manager.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMUserDeviceAffinityRequest -CollectionName <String> [-UserName <String>] [-UserId <String>]
 [-DeviceName <String>] [-DeviceId <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMUserDeviceAffinityRequest -CollectionId <String> [-UserName <String>] [-UserId <String>]
 [-DeviceName <String>] [-DeviceId <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserDeviceAffinityRequest** cmdlet gets a request for user device affinity.

In Microsoft System Center Configuration Manager, user device affinity defines a relationship between a user and a device.
Instead of deploying an application to a group of devices, you deploy an application to a user and Configuration Manager installs the application on all devices associated with the user.

## EXAMPLES

### Example 1: Get a request for user device affinity
```
PS C:\> Get-CMUserDeviceAffinityRequest -CollectionName "All Systems"
```

This command gets a request for user device affinity for the collection named All Systems.

## PARAMETERS

### -CollectionId
Specifies a collection ID that represents the user device affinity in Configuration Manager.

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

### -CollectionName
Specifies a name of a collection that represents the user device affinity in Configuration Manager.

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
Specifies a device ID in Configuration Manager.

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

### -DeviceName
Specifies a device name in Configuration Manager.

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

### -UserId
Specifies a Configuration Manager ID for a user resource.

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

### -UserName
Specifies a user name for a resource in Configuration Manager.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Approve-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Deny-CMUserDeviceAffinityRequest.md)


