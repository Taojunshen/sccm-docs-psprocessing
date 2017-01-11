---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833856
schema: 2.0.0
ms.assetid: 3F9D178E-7C8B-4C41-BC6C-3A2092A95B71
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSite.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSite.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSite.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMSite

## SYNOPSIS
Gets one or more Configuration Manager sites.

## SYNTAX

```
Get-CMSite [[-SiteCode] <String>] [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSite** cmdlet gets one or more Microsoft System Center Configuration Manager sites.
A System Center Configuration Manager site is a server that has clients assigned to it and that processes client-generated data.
You can get a Configuration Manager site by using either a site name or a site code.

## EXAMPLES

### Example 1: Get a site by using a site name
```
PS C:\> Get-CMSite -SiteName "CMSiteSystem"
```

This command gets a System Center Configuration Manager site by using the site name CMSiteSystem.

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

### -Name
Specifies the name of a Configuration Manager site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SiteName
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: False
Position: 0
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

[Set-CMSite](xref:ConfigurationManager/vlatest/Set-CMSite.md)


