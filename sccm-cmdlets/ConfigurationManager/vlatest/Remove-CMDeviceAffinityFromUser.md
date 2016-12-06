---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834041
schema: 2.0.0
ms.assetid: D7E17940-5C9F-4DDE-A364-11E554AAC586
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMDeviceAffinityFromUser.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMDeviceAffinityFromUser.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMDeviceAffinityFromUser

## SYNOPSIS
Removes device affinity from a Configuration Manager user.

## SYNTAX

### RemoveDeviceAffinityByUserName (Default)
```
Remove-CMDeviceAffinityFromUser -UserName <String[]> [-DeviceId <String>] [-DeviceName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDeviceAffinityByUserId
```
Remove-CMDeviceAffinityFromUser -UserId <String> [-DeviceId <String>] [-DeviceName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDeviceAffinityFromUser** cmdlet removes device affinity from a user of Microsoft System Center Configuration Manager.

Device affinity in Configuration Manager associates a user with one or more devices.
Instead of deploying applications to all the devices of a user, you deploy the application to the user and Configuration Manager automatically installs the application on all devices that are associated with that user.
Device affinity removes the need for Configuration Manager to determine the names of all the devices of a user before you deploy applications for that user.

For more information about user device affinity, see [How to Manage User Device Affinity in Configuration Manager](http://go.microsoft.com/fwlink/?linkid=247182) on TechNet.

## EXAMPLES

### Example 1: Remove device affinity from a user by user ID
```
PS C:\>Remove-CMDeviceAffinityFromUser -UserName "Patti Fuller" -DeviceName "WestDivUpdates05"
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

### -Force


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
Parameter Sets: RemoveDeviceAffinityByUserId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies an array of user names.

```yaml
Type: String[]
Parameter Sets: RemoveDeviceAffinityByUserName
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

[Add-CMDeviceAffinityToUser](xref:ConfigurationManager/vlatest/Add-CMDeviceAffinityToUser.md)

[Approve-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Approve-CMUserDeviceAffinityRequest.md)

[Deny-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Deny-CMUserDeviceAffinityRequest.md)

[Get-CMUserDeviceAffinity](xref:ConfigurationManager/vlatest/Get-CMUserDeviceAffinity.md)

[Get-CMUserDeviceAffinityRequest](xref:ConfigurationManager/vlatest/Get-CMUserDeviceAffinityRequest.md)

[Import-CMUserDeviceAffinity](xref:ConfigurationManager/vlatest/Import-CMUserDeviceAffinity.md)


