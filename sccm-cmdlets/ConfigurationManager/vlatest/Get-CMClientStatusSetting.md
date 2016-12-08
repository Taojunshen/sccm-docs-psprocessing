---
external help file: AdminUI.PS.ClientStatus.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834197
schema: 2.0.0
ms.assetid: C12D4C9E-15A3-44EB-9090-6E80B95045E3
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMClientStatusSetting.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMClientStatusSetting.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMClientStatusSetting

## SYNOPSIS
Gets client status settings.

## SYNTAX

```
Get-CMClientStatusSetting [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientStatusSetting** cmdlet gets client status settings for the local computer.
These settings determine the data collection intervals for individual client monitoring activities.

For more information about client settings, see [About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226) on TechNet.

## EXAMPLES

### Example 1: Get client status settings for the local computer
```
PS C:\> Get-CMClientStatusSetting
ADRetrieving Schedule  : 
CleanUpInterval        : 7
DDRInactiveInterval    : 3
HWInactiveInterval     : 4
NeedADLastLogonTime    : 
PolicyInactiveInterval : 3
SettingsID             : 1
StatusInactiveInterval : 6
SWInactiveInterval     : 5
```

This command gets client status settings for the local computer.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266226)

[Set-CMClientStatusSetting](xref:ConfigurationManager/vlatest/Set-CMClientStatusSetting.md)

[Update-CMClientStatus](xref:ConfigurationManager/vlatest/Update-CMClientStatus.md)


