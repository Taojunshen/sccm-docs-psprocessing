---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833663
schema: 2.0.0
ms.assetid: 6141C593-89DD-4BEB-80B2-DD9B391EB045
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMAssignedSite.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMAssignedSite.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMAssignedSite

## SYNOPSIS
Assigns a client computer to a primary site.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMAssignedSite -InputObject <IResultObject> [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMAssignedSite -DeviceName <String> [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMAssignedSite -DeviceId <String> [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAssignedSite** cmdlet assigns a client computer to a primary site.
When you install a client agent, the installation determines the primary site for the client.
This cmdlet assigns a client to a different primary site.

## EXAMPLES

### Example 1: Reassign a client to a site
```
PS C:\>Set-CMAssignedSite -DeviceId "2097152000" -SiteCode "CM7"
```

This command reassigns the client that has the device ID 2097152000 to the site that has the site code CM7.

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
Specifies an array of device IDs.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
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
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name

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

### -InputObject
Specifies a **CMDevice** object.
To obtain a **CMDevice** object, use the Get-CMDevice cmdlet.

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

### -SiteCode
Specifies the site code of the new primary site to assign the client to.

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

[Get-CMDevice](xref:ConfigurationManager/vlatest/Get-CMDevice.md)

