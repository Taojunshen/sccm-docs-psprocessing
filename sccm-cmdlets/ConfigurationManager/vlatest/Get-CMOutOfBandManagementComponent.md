---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833802
schema: 2.0.0
ms.assetid: DBE058A7-0428-449A-9EA0-65151A1702A7
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMOutOfBandManagementComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMOutOfBandManagementComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMOutOfBandManagementComponent

## SYNOPSIS
Gets an out of band management component.

## SYNTAX

```
Get-CMOutOfBandManagementComponent [-SiteSystemServerName <String>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOutOfBandManagementComponent** cmdlet gets the site system computer that has the out of band management role.
The out of band management role manages computers that have the Intel vPro chip set and a version of Intel Active Management Technology (Intel AMT) that System Center Configuration Manager supports.
Out of band management lets you connect to a computer AMT management controller when the computer is turned off, in hibernation, or otherwise unresponsive through the operating system.

## EXAMPLES

### Example 1: Get an out of band management component by using a site code
```
PS C:\>Get-CMOutOfBandManagementComponent -SiteCode "CM4"
```

This command gets the out of band management component from the client site that has code CM4.

### Example 2: Get an out of band management component by using a site server name
```
PS C:\>Get-CMOutOfBandManagementComponent -SiteSystemServerName "condev-test04.tsqa.corp.contoso.com"
```

This command gets the out of band management component from the site server named condev-test04.tsqa.corp.contoso.com in the client site.

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

[Set-CMOutOfBandManagementComponent](xref:ConfigurationManager/vlatest/Set-CMOutOfBandManagementComponent.md)

