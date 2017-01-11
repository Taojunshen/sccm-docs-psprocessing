---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833735
schema: 2.0.0
ms.assetid: E05F73D3-A82F-43B2-AD2A-BC6555936C41
updated_at: 12/7/2016 8:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMReportingServicePoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMReportingServicePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/282d10ca7ed3ddf1432b06182fee46c9e52563a4/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMReportingServicePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Add-CMReportingServicePoint

## SYNOPSIS
Adds a reporting service point to Configuration Manager.

## SYNTAX

### ReportingServicePointByValue (Default)
```
Add-CMReportingServicePoint [-ReportServerInstance <String>] [-DatabaseServerName <String>]
 [-DatabaseName <String>] -UserName <String> -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ReportingServicePoint
```
Add-CMReportingServicePoint [-FolderName <String>] [-ReportServerInstance <String>]
 [-SiteSystemServerName] <String> [-SiteCode <String>] [-DatabaseServerName <String>] [-DatabaseName <String>]
 -UserName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMReportingServicePoint** cmdlet adds a reporting service point to Configuration Manager.
A reporting service point is a site system role that is installed on a server that run Microsoft SQL Server Reporting Services.

## EXAMPLES

### Example 1: Add a reporting service point
```
PS C:\>Add-CMReportingServicePoint -SiteCode "CM1" -SiteSystemServerName "CMReportingServicePoint.TSQA.Contoso.com"
```

This command adds a reporting service point on the computer named CMReportingServicePoint.TSQA.Contoso.com for the Configuration Manager site that has the site code CM1.

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

### -DatabaseName
Specifies the name of the Configuration Manager database that you want to use as the data source for reports from Microsoft SQL Server Reporting Services.

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

### -DatabaseServerName
Specifies the name of the Configuration Manager database server that you want to use as the data source for reports from Microsoft SQL Server Reporting Services.
To specify a database instance, use the format \<Server Name\>\\\<Instance Name\>.

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

### -FolderName
Specifies the name of the report folder on the report server.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: ReportingServicePointByValue
Aliases: SiteServer
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReportServerInstance
Specifies the name of an instance of Microsoft SQL Server Reporting Services.

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

### -SiteCode
Specifies a site code of a Configuration Manager site that hosts this site system role.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: ReportingServicePoint
Aliases: Name, ServerName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies a user name for an account that Configuration Manager uses to connect with Microsoft SQL Server Reporting Services and that gives this user access to the site database.

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

[Get-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Get-CMReportingServicePoint.md)

[Remove-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Remove-CMReportingServicePoint.md)

[Set-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Set-CMReportingServicePoint.md)


