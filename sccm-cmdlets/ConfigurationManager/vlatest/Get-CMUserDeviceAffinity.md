---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834001
schema: 2.0.0
ms.assetid: 465E33E8-26CF-4981-A815-0ADD2BFA15F9
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMUserDeviceAffinity.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMUserDeviceAffinity.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMUserDeviceAffinity

## SYNOPSIS
Gets user device affinities.

## SYNTAX

### SearchByUserNameMandatory (Default)
```
Get-CMUserDeviceAffinity -UserName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Get-CMUserDeviceAffinity -DeviceName <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Get-CMUserDeviceAffinity -DeviceId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByUserIdMandatory
```
Get-CMUserDeviceAffinity -UserId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserDeviceAffinity** cmdlet gets one or more user device affinities.
User device affinity in Microsoft System Center Configuration Manager is a method of associating a user with one or more specified devices.

## EXAMPLES

### Example 1: Get a user device affinity by using a user name
```
PS C:\>Get-CMUserDeviceAffinity -UserName "CENTRAL\001D$"
```

This command gets the user device affinity for the user named CENTRAL\001D$.

### Example 2: Get a user device affinity by using a user ID
```
PS C:\>Get-CMUserDeviceAffinity -UserID "2063597981"
```

This command gets the user device affinity for the user that has the ID named 2063597981.

### Example 3: Get a user device affinity by using a device name
```
PS C:\>Get-CMUserDeviceAffinity -DeviceName "CMCEN-DIST02"
```

This command gets the user device affinity for the device named CMCEN-DIST02.

### Example 4: Get a user device affinity by using a device ID
```
PS C:\>Get-CMUserDeviceAffinity -DeviceID "2097152000"
```

This command gets the user device affinity for the device that has the ID 2097152000.

## PARAMETERS

### -DeviceId
Specifies an array of device IDs.

```yaml
Type: String[]
Parameter Sets: SearchByDeviceIdMandatory
Aliases: ResourceId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of device names.

```yaml
Type: String[]
Parameter Sets: SearchByDeviceNameMandatory
Aliases: ResourceName
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
Specifies an array of IDs of the primary users of the devices.

```yaml
Type: String[]
Parameter Sets: SearchByUserIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies an array of names of the primary users of the devices.

```yaml
Type: String[]
Parameter Sets: SearchByUserNameMandatory
Aliases: UniqueUserName
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

[Approve-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Deny-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Get-CMUserDeviceAffinityRequest.md)

[Import-CMUserDeviceAffinity](xref:ConfigurationManager/vlatest/Import-CMUserDeviceAffinity.md)


