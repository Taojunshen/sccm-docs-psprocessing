---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833658
schema: 2.0.0
ms.assetid: 6A49F9E5-ECD8-438F-9A2D-D0D2615941B3
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMExchangeServer.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/New-CMExchangeServer.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMExchangeServer

## SYNOPSIS
Configures a new Exchange Server connector.

## SYNTAX

### NewOnPrem (Default)
```
New-CMExchangeServer [-SiteCode <String>] -ServerAddress <String> [-IsHosted <Boolean>] [-OnPrem]
 [-ExchangeClientAccessServer <Dictionary`2[]>] [-UserName <String>] -FullSyncSchedule <IResultObject>
 -DeltaSyncMins <Int32> [-MaximumInactiveDay <Int32>] [-ActiveDirectoryContainer <String[]>]
 [-GeneralSetting <ExchangeConnectorGeneralSetting>] [-PasswordSetting <ExchangeConnectorPasswordSetting>]
 [-EmailManagementSetting <ExchangeConnectorEmailManagementSetting>]
 [-SecuritySetting <ExchangeConnectorSecuritySetting>]
 [-ApplicationSetting <ExchangeConnectorApplicationSetting>] [-AllowExternalDeviceManagement <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewHosted
```
New-CMExchangeServer [-SiteCode <String>] -ServerAddress <String> [-IsHosted <Boolean>] [-Hosted]
 -UserName <String> -FullSyncSchedule <IResultObject> -DeltaSyncMins <Int32> [-MaximumInactiveDay <Int32>]
 [-ActiveDirectoryContainer <String[]>] [-GeneralSetting <ExchangeConnectorGeneralSetting>]
 [-PasswordSetting <ExchangeConnectorPasswordSetting>]
 [-EmailManagementSetting <ExchangeConnectorEmailManagementSetting>]
 [-SecuritySetting <ExchangeConnectorSecuritySetting>]
 [-ApplicationSetting <ExchangeConnectorApplicationSetting>] [-AllowExternalDeviceManagement <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServer** cmdlet configures a new Microsoft Exchange Server connector in Microsoft System Center Configuration Manager.
An Exchange Server connector synchronizes and manages the device enrolled by the Exchange Server.
For more information, see [Configuration Manager 2012 Exchange Connector Implementation in Microsoft IT](http://go.microsoft.com/fwlink/?LinkId=286314) on TechNet.

## EXAMPLES

### Example 1: Create an Exchange Server
```
PS C:\>$schedule = New-CMSchedule -Start "03/01/2016 11:59 PM" -RecurInterval Days -RecurCount 1
New-CMExchangeServer -ServerAddress "http://exchange.contoso.com" -DeltaSyncInterval 120 -FullSyncSchedule $schedule -IsHosted -SiteCode "ContosoSite"
```

These commands create an Exchange Server with the server address http://exchange,contoso.com.
To do this, the first command in the example uses the **New-CMSchedule** cmdlet to create a schedule for doing Exchange synchronizations.
This schedule object is stored in a variable $schedule.

The second command then uses **New-CMExchangeServer** to create the new server as part of the site ContosoSite.

## PARAMETERS

### -ActiveDirectoryContainer


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

### -AllowExternalDeviceManagement


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationSetting


```yaml
Type: ExchangeConnectorApplicationSetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -DeltaSyncMins


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DeltaSyncInterval

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

### -EmailManagementSetting


```yaml
Type: ExchangeConnectorEmailManagementSetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExchangeClientAccessServer


```yaml
Type: Dictionary`2[]
Parameter Sets: NewOnPrem
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

### -FullSyncSchedule


```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -GeneralSetting


```yaml
Type: ExchangeConnectorGeneralSetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hosted


```yaml
Type: SwitchParameter
Parameter Sets: NewHosted
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsHosted


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumInactiveDay


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

### -OnPrem


```yaml
Type: SwitchParameter
Parameter Sets: NewOnPrem
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PasswordSetting


```yaml
Type: ExchangeConnectorPasswordSetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecuritySetting


```yaml
Type: ExchangeConnectorSecuritySetting
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerAddress


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

### -UserName


```yaml
Type: String
Parameter Sets: NewOnPrem
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NewHosted
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

[Get-CMExchangeServer](xref:ConfigurationManager/vlatest/Get-CMExchangeServer.md)

[Remove-CMExchangeServer](xref:ConfigurationManager/vlatest/Remove-CMExchangeServer.md)

[Set-CMExchangeServer](xref:ConfigurationManager/vlatest/Set-CMExchangeServer.md)

[Sync-CMExchangeServer](xref:ConfigurationManager/vlatest/Sync-CMExchangeServer.md)

