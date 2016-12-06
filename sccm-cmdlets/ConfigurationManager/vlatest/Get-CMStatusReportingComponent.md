---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833944
schema: 2.0.0
ms.assetid: D8EA1510-9DA9-4DE1-BCBB-D5AA2D737E58
updated_at: 12/5/2016 10:55 PM
ms.date: 12/5/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMStatusReportingComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/f95cf139be40af870257194c70c82183d89f7a0c/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMStatusReportingComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMStatusReportingComponent

## SYNOPSIS
Gets an object representing a status reporting component.

## SYNTAX

```
Get-CMStatusReportingComponent [-SiteSystemServerName <String>] [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMStatusReportingComponent** cmdlet gets an object that represents the status reporting component.
This object provides information about the client configuration and server configuration components.

## EXAMPLES

### Example 1: Get status reporting components
```
PS C:\>Get-CMStatusReportingComponent -SiteCode "CM1"
```

This command gets the status reporting components that Set-CMStatusReportingComponent configures for the site.

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
Specifies a site code of a Configuration Manager site.

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
Specifies an array of site system server names.

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

[Set-CMStatusReportingComponent](xref:ConfigurationManager/vlatest/Set-CMStatusReportingComponent.md)


