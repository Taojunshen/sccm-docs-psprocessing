---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833833
schema: 2.0.0
ms.assetid: 5B517A0E-E010-4E69-8658-9300234C3131
updated_at: 12/7/2016 8:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMReportingServicePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/282d10ca7ed3ddf1432b06182fee46c9e52563a4/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMReportingServicePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMReportingServicePoint

## SYNOPSIS
Gets a reporting service point.

## SYNTAX

### SearchByName
```
Get-CMReportingServicePoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMReportingServicePoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMReportingServicePoint** cmdlet gets a reporting service point.
A reporting service point is a site system role that is installed on a server that runs Microsoft SQL Server Reporting Services.

## EXAMPLES

### Example 1: Get a reporting service point
```
PS C:\>Get-CMReportingServicePoint -SiteSystemServerName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM" -SiteCode "CM1" >>\Cmrsp01\Get-CMReportingServicePoint_data.txt
```

This command gets a reporting service point from the Configuration Manager site that has the site code CM1 on the site system server named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM.
The command directs the output to the file \Cmrsp01\Get-CMReportingServicePoint_data.txt.

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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Microsoft System Center Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByName
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
Parameter Sets: SearchByName
Aliases: Name, ServerName
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

[Add-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Add-CMReportingServicePoint.md)

[Remove-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Remove-CMReportingServicePoint.md)

[Set-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Set-CMReportingServicePoint.md)


