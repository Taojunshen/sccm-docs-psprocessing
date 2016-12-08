---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834104
schema: 2.0.0
ms.assetid: 5BF0061A-3EB7-4D64-BA08-72AD7E25B4DC
updated_at: 12/7/2016 8:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMExchangeServer.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/282d10ca7ed3ddf1432b06182fee46c9e52563a4/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMExchangeServer.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMExchangeServer

## SYNOPSIS
Removes an Exchange Server object from Configuration Manager.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Remove-CMExchangeServer [-SiteCode <String>] -ExchangeServerUrl <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValue
```
Remove-CMExchangeServer [-Force] -InputObject <ExchangeConnector> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMExchangeServer** cmdlet removes a Microsoft Exchange Server object from Microsoft System Center Configuration Manager for one or more Configuration Manager sites.
This cmdlet does not uninstall the Exchange Server.

Configuration Manager works with Exchange Server to manage mobile devices that cannot run Configuration Manager clients.

## EXAMPLES

### Example 1: Remove an nextref_exchange
```
PS C:\>Remove-CMExchangeServer -Address "http://localhost/PowerShell" -SiteCode "PE1"
```

This command removes the Exchange Server with the specified address for the site code PE1.

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

### -ExchangeServerUrl


```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases: Address, ServerAddress
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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
Type: ExchangeConnector
Parameter Sets: ByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site associated with the Exchange Server.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
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

[Get-CMExchangeServer](xref:ConfigurationManager/vlatest/Get-CMExchangeServer.md)

[New-CMExchangeServer](xref:ConfigurationManager/vlatest/New-CMExchangeServer.md)

[Set-CMExchangeServer](xref:ConfigurationManager/vlatest/Set-CMExchangeServer.md)

[Sync-CMExchangeServer](xref:ConfigurationManager/vlatest/Sync-CMExchangeServer.md)


