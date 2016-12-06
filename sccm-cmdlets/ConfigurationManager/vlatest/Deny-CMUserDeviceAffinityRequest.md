---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833931
schema: 2.0.0
ms.assetid: CF9105FA-8872-47E9-8FEB-1736A3FEBBEF
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Deny-CMUserDeviceAffinityRequest.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Deny-CMUserDeviceAffinityRequest.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Deny-CMUserDeviceAffinityRequest

## SYNOPSIS
Denies a request for user device affinity in Configuration Manager.

## SYNTAX

### SearchByNameMandatory (Default)
```
Deny-CMUserDeviceAffinityRequest -CollectionName <String> [-UserName <String>] [-UserId <String>]
 [-DeviceName <String>] [-DeviceId <String>] [-UserDeviceAffinityRequestId <String>]
 [-UserDeviceAffinityRequest <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Deny-CMUserDeviceAffinityRequest -CollectionId <String> [-UserName <String>] [-UserId <String>]
 [-DeviceName <String>] [-DeviceId <String>] [-UserDeviceAffinityRequestId <String>]
 [-UserDeviceAffinityRequest <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Deny-CMUserDeviceAffinityRequest** cmdlet denies a request for user device affinity.

In Microsoft System Center Configuration Manager, user device affinity defines a relationship between a user and a device.

## EXAMPLES

### Example 1: Deny a request for user device affinity
```
PS C:\>Deny-CMUserDeviceAffinityRequest -CollectionName "All Systems" -UserName "Western\EvanNarvaez$"
```

This command denies a request for user device affinity for the collection named All Systems.

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

### -UserDeviceAffinityRequest
Specifies a **CMUserDeviceAffinityRequest** object.
To obtain a **CMUserDeviceAffinityRequest** object, use the Get-CMUserDeviceAffinityRequest cmdlet.

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

### -UserDeviceAffinityRequestId
Specifies a unique ID for a request for user device affinity.

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

[Approve-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Approve-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Get-CMUserDeviceAffinityRequest.md)


