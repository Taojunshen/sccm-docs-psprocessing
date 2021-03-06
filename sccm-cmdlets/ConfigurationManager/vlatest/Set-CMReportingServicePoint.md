---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834010
schema: 2.0.0
ms.assetid: 06BFF15B-79D8-46D1-99F3-CE319F2BF432
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMReportingServicePoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMReportingServicePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMReportingServicePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMReportingServicePoint

## SYNOPSIS
Modifies a System Center Configuration Manager reporting service point.

## SYNTAX

### SetByValue (Default)
```
Set-CMReportingServicePoint [-DatabaseServerName <String>] [-DatabaseName <String>] [-UserName <String>]
 -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMReportingServicePoint [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-DatabaseServerName <String>] [-DatabaseName <String>] [-UserName <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMReportingServicePoint** cmdlet modifies a Microsoft System Center Configuration Manager reporting service point.
A reporting service point is a site system role that is installed on a server that is running Microsoft SQL Server Reporting Services.

## EXAMPLES

### Example 1: Set a reporting service point
```
PS C:\> Set-CMReportingServicePoint -SiteSystemServerName "Contoso-Test.Contoso.Com" -SiteCode "CM4" -UserName "Contoso\DavidChew"
```

The command sets a reporting service point by using the *SiteSystemServerName* parameter.

### Example 2: Set a reporting service point by using a site system server name
```
PS C:\> Set-CMReportingServicePoint -SiteSystemServerName "Contoso-Test.Contoso.Com" -SiteCode "CM4" -DatabaseServerName "Contoso-TestDB.Contoso.Com" -DatabaseName "CM_CM2"
```

The command sets a reporting service point by using the *SiteSystemServerName* parameter.

### Example 3: Set a reporting service point by using an input object
```
PS C:\> $RS = Get-CMReportingServicePoint -SiteSystemServerName "Contoso-Test.Contoso.Com" -SiteCode "CM4" 
PS C:\> Set-CMReportingServicePoint -InputObject $RS -DatabaseServerName "Contoso-TestDB.Contoso.Com" -DatabaseName "CM_CM4"
```

The first command uses the **Get-CMReportingServicePoint** cmdlet to get a reporting service point, by using the *SiteSystemServerName* parameter.

The second command uses the **Set-CMReportingServicePoint** cmdlet to set the reporting point by using the input object.

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
Specifies the name of the Configuration Manager database server that you want to use as the data source for the reports from Microsoft SQL Server Reporting Services.
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
Specifies an input object.
To obtain an input object, use the [Get-CMReportingServicePoint](./Get-CMReportingServicePoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: ReportingServicePoint
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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
Specifies a site code of a Configuration Manager site that hosts this system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server hosting the site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies a user name that Configuration Manager uses to connect with Microsoft SQL Server Reporting Services and that gives this user access to the site database.

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

[Add-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Add-CMReportingServicePoint.md)

[Get-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Get-CMReportingServicePoint.md)

[Remove-CMReportingServicePoint](xref:ConfigurationManager/vlatest/Remove-CMReportingServicePoint.md)
