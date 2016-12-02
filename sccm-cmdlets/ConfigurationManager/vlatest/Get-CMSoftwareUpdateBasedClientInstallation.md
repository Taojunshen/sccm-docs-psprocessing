---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833904
schema: 2.0.0
ms.assetid: 3E004486-ADA5-4109-BBB7-035A2FE790AA
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateBasedClientInstallation.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateBasedClientInstallation.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMSoftwareUpdateBasedClientInstallation

## SYNOPSIS
Gets a client installation on a Configuration Manager software update point.

## SYNTAX

```
Get-CMSoftwareUpdateBasedClientInstallation [-SiteCode <String>] [-SiteSystemServerName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateBasedClientInstallation** cmdlet gets a client installation hosted on a software update point for Microsoft System Center Configuration Manager.

System Center Configuration Manager publishes the System Center Configuration Manager client to a software update point.
This site system role can install the client on computers that do not already have it or upgrade existing clients.

To use software update point based installation, you must use the same Windows Server Update Services (WSUS) server for both client installation and software updates.
This server must be the active software update point in a primary site.

## EXAMPLES

### Example 1: Get a client installation
```
PS C:\>Get-CMSoftwareUpdateBasedClientInstallation -SiteCode "CM1"
```

This command gets the client installation for the site that has the site code CM1.

## PARAMETERS

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

### -SiteCode


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

### -SiteSystemServerName


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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSoftwareUpdateBasedClientInstallation](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdateBasedClientInstallation.md)

