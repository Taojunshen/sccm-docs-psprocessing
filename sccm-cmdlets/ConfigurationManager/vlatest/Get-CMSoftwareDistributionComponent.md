---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833887
schema: 2.0.0
ms.assetid: 46449F73-D5C2-440E-A775-5C2A01F9C1B3
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareDistributionComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareDistributionComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMSoftwareDistributionComponent

## SYNOPSIS
Gets an object that represents a software distribution component in Configuration Manager.

## SYNTAX

```
Get-CMSoftwareDistributionComponent [-SiteCode <String>] [-SiteSystemServerName <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareDistributionComponent** cmdlet gets an object that represents a software distribution component in Microsoft System Center Configuration Manager.
A software distribution component consists of individual components such as the client software distribution component.

## EXAMPLES

### Example 1: Get a software distribution component
```
PS C:\>Get-CMSoftwareDistributionComponent -Name "CM2"
```

This command gets the software distribution component.

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
Type: String[]
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

[Set-CMSoftwareDistributionComponent](xref:ConfigurationManager/vlatest/Set-CMSoftwareDistributionComponent.md)

