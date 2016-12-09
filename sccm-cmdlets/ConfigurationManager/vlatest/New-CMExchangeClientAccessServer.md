---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833654
schema: 2.0.0
ms.assetid: E66BF7A0-762F-470D-BCD0-E0A58EA3FB6F
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/New-CMExchangeClientAccessServer.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/New-CMExchangeClientAccessServer.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/New-CMExchangeClientAccessServer.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# New-CMExchangeClientAccessServer

## SYNOPSIS
Creates a Client Access server role for an Exchange Server.

## SYNTAX

```
New-CMExchangeClientAccessServer -ExchangeClientAccessServerName <String> -ActiveDirectorySiteName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeClientAccessServer** cmdlet creates a Client Access server role for a Microsoft Exchange Server.
The Client Access server role accepts connections to Exchange Server from different types of clients.
Software clients such as Microsoft Outlook use POP3 or IMAP4 connections to communicate with Exchange Server.
Hardware clients, such as mobile devices, use ActiveSync, POP3, or IMAP4 to communicate with Exchange Server.

## EXAMPLES

### Example 1: Create an Exchange Client Access server
```
PS C:\> $Ecs= New-CMExchangeClientAccessServer -ExchangeClientAccessServerName "ContosoWestCAS11" -ActiveDirectorySiteName "ContosoWestAD01"
```

This command creates a new Exchange Client Access server named ContosoWestCAS11 and associates it with the Active Directory site named ContosoWestAD01, then places the resulting Exchange Client Access server object in the variable $Ecs.

## PARAMETERS

### -ActiveDirectorySiteName
Specifies the name of the Active Directory site on which you are installing the Client Access server role.

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

### -ExchangeClientAccessServerName
Specifies the name of the Exchange Client Access server that you create.

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


