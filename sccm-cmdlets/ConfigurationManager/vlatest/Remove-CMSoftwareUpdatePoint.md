---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834229
schema: 2.0.0
ms.assetid: F459D8AF-0C31-4E95-8EF1-AF9FF31167BD
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMSoftwareUpdatePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMSoftwareUpdatePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMSoftwareUpdatePoint

## SYNOPSIS
Removes a software update point site system role from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMSoftwareUpdatePoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSoftwareUpdatePoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSoftwareUpdatePoint** cmdlet removes a software update point site system role from Microsoft System Center Configuration Manager.

A software update point is a site server role that hosts software updates.
System Center Configuration Manager clients connect to a software update point to get available updates.
The software update point interacts with Windows Server Update Services (WSUS) to configure update settings, request synchronization to the update source, and to synchronize software updates from the WSUS database.

You can specify a software update point to remove by site code and the name of the computer that hosts the site system role.
You can also use the Get-CMSoftwareUpdatePoint cmdlet to obtain a software update point.

## EXAMPLES

### Example 1: Remove a software update point
```
PS C:\> Remove-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "UpdateSystem.Western.Contoso.com"
```

The command removes a software update point.
The cmdlet requires both the site code and the name.
Because the command does not include the *Force* parameter, the cmdlet prompts you for confirmation.

### Example 2: Remove a software update point by using a variable
```
PS C:\> $CMSUP = Get-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "UpdateSystem.Western.Contoso.com"
PS C:\> Remove-CMSoftwareUpdatePoint -InputObject $CMSUP -Force
```

The first command gets a software update point and saves it to the $CMSUP variable.

The second command removes the software update point saved in the $CMSUP variable.
This command uses the *Force* parameter, so the cmdlet does not prompt you for confirmation.

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
Forces the command to run without asking for user confirmation.

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
Specifies a software update point object.
To obtain a software update point object, use the **Get-CMSoftwareUpdatePoint** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: SoftwareUpdatePoint
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a computer that hosts the software update point site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName
Required: True
Position: 0
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

[Add-CMSoftwareUpdatePoint](xref:ConfigurationManager/vlatest/Add-CMSoftwareUpdatePoint.md)

[Get-CMSoftwareUpdatePoint](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdatePoint.md)

[Set-CMSoftwareUpdatePoint](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdatePoint.md)


