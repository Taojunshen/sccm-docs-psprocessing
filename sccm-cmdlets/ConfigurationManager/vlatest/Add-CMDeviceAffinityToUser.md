---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833638
schema: 2.0.0
ms.assetid: 8E7A3551-4BB0-43EB-AD44-FB4FF6A8F3A4
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMDeviceAffinityToUser.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMDeviceAffinityToUser.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMDeviceAffinityToUser.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Add-CMDeviceAffinityToUser

## SYNOPSIS
Adds device affinity to a Configuration Manager user.

## SYNTAX

### AddDeviceAffinityByUserName (Default)
```
Add-CMDeviceAffinityToUser -UserName <String[]> [-DeviceId <String>] [-DeviceName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddDeviceAffinityByUserId
```
Add-CMDeviceAffinityToUser -UserId <String> [-DeviceId <String>] [-DeviceName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDeviceAffinityToUser** cmdlet adds device affinity to a user of Microsoft System Center Configuration Manager.

Device affinity in Configuration Manager associates a user with one or more devices.
Instead of deploying applications to all the user's devices, you deploy the application to the user and Configuration Manager automatically installs the application on all devices that are associated with that user.
Device affinity removes the need for Configuration Manager to determine the names of the devices of a user before you deploy applications for that user.

For more information about user device affinity, see [How to Manage User Device Affinity in Configuration Manager](http://go.microsoft.com/fwlink/?linkid=247182) on TechNet.

## EXAMPLES

### Example 1: Add device affinity to a user by user ID
```
PS C:\>Add-CMDeviceAffinityToUser -UserName "Patti Fuller" -DeviceName "WestDivUpdates05"
```

This command adds affinity to the device named WestDivUpdates05 for the user named Patti Fuller.

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

### -DeviceId
Specifies a device by using an ID.

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
Specifies a device by using a name.

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
Specifies a user by using an ID.

```yaml
Type: String
Parameter Sets: AddDeviceAffinityByUserId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies an array of user names to associate with the device.

```yaml
Type: String[]
Parameter Sets: AddDeviceAffinityByUserName
Aliases: UniqueUserName
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

[Approve-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Deny-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinity](xref:ConfigurationManager/vlatest/Get-CMUserDeviceAffinity.md)

[Get-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Get-CMUserDeviceAffinityRequest.md)

[Import-CMUserDeviceAffinity](xref:ConfigurationManager/vlatest/Import-CMUserDeviceAffinity.md)

[Remove-CMDeviceAffinityFromUser](xref:ConfigurationManager/vlatest/Remove-CMDeviceAffinityFromUser.md)


