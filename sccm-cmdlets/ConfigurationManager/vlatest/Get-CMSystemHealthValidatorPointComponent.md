---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833959
schema: 2.0.0
ms.assetid: 28507B76-6E7C-4438-97E4-42BCB4E0E221
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSystemHealthValidatorPointComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSystemHealthValidatorPointComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMSystemHealthValidatorPointComponent

## SYNOPSIS
Retrieves an object that represents a system health validator point in Configuration Manager.

## SYNTAX

```
Get-CMSystemHealthValidatorPointComponent [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSystemHealthValidatorPointComponent** cmdlet retrieves an object that represents a system health validator point.
A system health validator point is a site system role that evaluates system health information reported by Windows clients for security related compliance.

## EXAMPLES

### Example 1: Retrieve a system health validator point by site system server name
```
PS C:\>Get-CMSystemHealthValidatorPointComponent -SiteSystemServerName "Shvp-01.TSQA.Corp.Contoso.com"
```

This command retrieves a system health validator point component by using a site system server name.

### Example 2: Retrieve a system health validator point by site code
```
PS C:\>Get-CMSystemHealthValidatorPointComponent -SiteCode "CM4"
```

This command retrieves a system health validator point component by using a site code.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSystemHealthValidatorPointComponent](xref:ConfigurationManager/vlatest/Set-CMSystemHealthValidatorPointComponent.md)


