---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834303
schema: 2.0.0
ms.assetid: F5C5D86D-D784-4F14-A172-A57416465C12
updated_at: 12/7/2016 11:21 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/New-CMClientAuthCertificateProfileConfigurationItem.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4bb0549ab9452d0d1c9cdf57cfbc8185eefd798c/sccm-cmdlets/ConfigurationManager/vlatest/New-CMClientAuthCertificateProfileConfigurationItem.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# New-CMClientAuthCertificateProfileConfigurationItem

## SYNOPSIS
Creates a certificate profile.

## SYNTAX

```
New-CMClientAuthCertificateProfileConfigurationItem -DesiredConfigurationDigestPath <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMClientAuthCertificateProfileConfigurationItem** cmdlet creates a certificate profile.
Client computers use certificate profiles to authenticate when they use services such as a virtual private network (VPN) or a wireless network.

## EXAMPLES


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

### -DesiredConfigurationDigestPath
Specifies a path to the configuration data stored as a digest.

```yaml
Type: String
Parameter Sets: (All)
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

[Set-CMClientAuthCertificateProfileConfigurationItem](xref:ConfigurationManager/vlatest/Set-CMClientAuthCertificateProfileConfigurationItem.md)


