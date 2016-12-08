---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833706
schema: 2.0.0
ms.assetid: 78A69AB1-BD8F-42A4-8A9B-B38810F81BD1
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMFileReplicationRoute.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMFileReplicationRoute.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMFileReplicationRoute

## SYNOPSIS
Gets a file replication route from Configuration Manager.

## SYNTAX

### SearchBySiteCode (Default)
```
Get-CMFileReplicationRoute [-SourceSiteCode <String>] [-DestinationSiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySiteName
```
Get-CMFileReplicationRoute [-SourceSiteName <String>] [-DestinationSiteName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMFileReplicationRoute** cmdlet gets a file replication route from Microsoft System Center Configuration Manager.
Configuration Manager uses file replication routes to transfer file-based data between sites in a hierarchy.
Each file replication route identifies a destination site to which file-based data can transfer.

File replication were known as addresses in versions of Configuration Manager before System Center Configuration Manager.
The functionality of file replication routes is the same as that of addresses in earlier versions.

## EXAMPLES

### Example 1: Get a file replication route by using site codes
```
PS C:\> Get-CMFileReplicationRoute -DestinationSiteCode "IM5" -SourceSiteCode "IM1"
```

This command creates a file replication route from the site that has the site code IM1 to the site that has the site code IM5.

## PARAMETERS

### -DestinationSiteCode
Specifies a destination site for data transfers by using a site code.

```yaml
Type: String
Parameter Sets: SearchBySiteCode
Aliases: DesSiteCode
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationSiteName
Specifies a destination site for data transfers by using a site name.

```yaml
Type: String
Parameter Sets: SearchBySiteName
Aliases: DesSiteName
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

### -SourceSiteCode
Specifies a source site for data transfers by using a site code.

```yaml
Type: String
Parameter Sets: SearchBySiteCode
Aliases: SiteCode
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceSiteName
Specifies a destination site for data transfers by using a site name.

```yaml
Type: String
Parameter Sets: SearchBySiteName
Aliases: SiteName
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

[New-CMFileReplicationRoute](xref:ConfigurationManager/vlatest/New-CMFileReplicationRoute.md)

[Remove-CMFileReplicationRoute](xref:ConfigurationManager/vlatest/Remove-CMFileReplicationRoute.md)

[Set-CMFileReplicationRoute](xref:ConfigurationManager/vlatest/Set-CMFileReplicationRoute.md)


