---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833745
schema: 2.0.0
ms.assetid: 69AC1D24-491C-4095-B924-5D78E948342B
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMManagementPointComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMManagementPointComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMManagementPointComponent

## SYNOPSIS
Gets a component for a Configuration Manager management point.

## SYNTAX

```
Get-CMManagementPointComponent [-SiteCode <String>] [-SiteSystemServerName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMManagementPointComponent** cmdlet gets a component of a management point for Microsoft System Center Configuration Manager.
A management point is a System Center Configuration Manager site that provides policy and service information to clients and receives configuration data from clients.

## EXAMPLES

### Example 1: Get a management point component
```
PS C:\>Get-CMManagementPointComponent -SiteCode "CM1" >>\1\Get-CMManagementPointComponent_data.txt
```

This command gets a component that is associated with the site that has the code CM1.
The command directs the output to the file Get-CMManagementPointComponent_data.txt.

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

[Set-CMManagementPointComponent](xref:ConfigurationManager/vlatest/Set-CMManagementPointComponent.md)

[Get-CMManagementPoint](xref:ConfigurationManager/vlatest/Get-CMManagementPoint.md)

[Remove-CMManagementPoint](xref:ConfigurationManager/vlatest/Remove-CMManagementPoint.md)


