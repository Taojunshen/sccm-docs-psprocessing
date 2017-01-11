---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834208
schema: 2.0.0
ms.assetid: 336CD5FE-3132-4211-A98D-0D5DDFA6F203
updated_at: 1/10/2017 12:09 AM
ms.date: 1/10/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCmdletUpdateCheck.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCmdletUpdateCheck.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/fc724eb955efcd7270886ed969a5ed6250f9ffc5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCmdletUpdateCheck.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMCmdletUpdateCheck

## SYNOPSIS
Gets a cmdlet update check configuration object.

## SYNTAX

### User (Default)
```
Get-CMCmdletUpdateCheck [-CurrentUser] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### System
```
Get-CMCmdletUpdateCheck [-System] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCmdletUpdateCheck** cmdlet gets an update check configuration object and indicates if user policy is being overridden by system policy.

**Note:** This cmdlet is deprecated starting with version 1610, and may be removed in a future release.

## EXAMPLES

### Example 1: Get the update check configuration
```
PS C:\> Get-CMCmdletUpdateCheck -CurrentUser
```

This command gets the update check configuration for the current user.

## PARAMETERS

### -CurrentUser
Indicates that the update check configuration for the current user is returned.
This parameter lets you know if the system policy is overriding user policy.

```yaml
Type: SwitchParameter
Parameter Sets: User
Aliases: User
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

### -System
Indicates that the update check for the system is returned.
This parameter lets you know what is being overridden by system policy.

```yaml
Type: SwitchParameter
Parameter Sets: System
Aliases:
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

### Microsoft.ConfigurationManagement.Cmdlets.Common.Update.CMCmdletUpdateConfiguration

## NOTES

## RELATED LINKS

[Send-CMCmdletUpdateCheck](xref:ConfigurationManager/vlatest/Send-CMCmdletUpdateCheck.md)

[Set-CMCmdletUpdateCheck](xref:ConfigurationManager/vlatest/Set-CMCmdletUpdateCheck.md)
