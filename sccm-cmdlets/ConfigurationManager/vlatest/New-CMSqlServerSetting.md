---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833773
schema: 2.0.0
ms.assetid: 3BEACC09-5500-4890-BF68-77652EF15768
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMSqlServerSetting.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/New-CMSqlServerSetting.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMSqlServerSetting

## SYNOPSIS
Creates a SQL Server settings object in Configuration Manager.

## SYNTAX

### NewSettingByExisting (Default)
```
New-CMSqlServerSetting [-UseExistingSqlServerInstance] [-InstanceName <String>] -SiteDatabaseName <String>
 [-SqlServerServiceBrokerPort <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewSettingByCopy
```
New-CMSqlServerSetting [-CopySqlServerExpressOnSecondarySite] [-SqlServerServicePort <Int32>]
 [-SqlServerServiceBrokerPort <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSqlServerSetting** cmdlet creates a Microsoft SQL Server settings object in Microsoft System Center Configuration Manager.
The object specifies settings for the name of the site database and the port number for the SQL Server service and SQL Server Service Broker.

## EXAMPLES

### Example 1: Create a SQL Server settings object
```
PS C:\>New-CMSqlServerSetting -CopySqlServerExpressOnSecondarySite -SqlServerServiceBrokerPort 4037
```

This command creates a SQL Server settings object that specifies that System Center Configuration Manager copies Microsoft SQL Server Express to a secondary site.
The command specifies that System Center Configuration Manager use port 4037 for the SQL Server Service Broker.

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

### -CopySqlServerExpressOnSecondarySite


```yaml
Type: SwitchParameter
Parameter Sets: NewSettingByCopy
Aliases: 

Required: True
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

### -InstanceName


```yaml
Type: String
Parameter Sets: NewSettingByExisting
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteDatabaseName


```yaml
Type: String
Parameter Sets: NewSettingByExisting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlServerServiceBrokerPort


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlServerServicePort


```yaml
Type: Int32
Parameter Sets: NewSettingByCopy
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseExistingSqlServerInstance


```yaml
Type: SwitchParameter
Parameter Sets: NewSettingByExisting
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


