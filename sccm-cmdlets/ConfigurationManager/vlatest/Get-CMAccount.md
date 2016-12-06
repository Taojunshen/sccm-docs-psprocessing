---
external help file: AdminUI.PS.Accounts.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834057
schema: 2.0.0
ms.assetid: 37B4DA45-91D4-47B0-AD08-F7D68D98FF8D
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAccount.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAccount.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMAccount

## SYNOPSIS
Gets a named user account.

## SYNTAX

```
Get-CMAccount [[-UserName] <String>] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAccount** cmdlet gets a Microsoft System Center Configuration Manager user account.
The user name must be in the domain\user format.
For more information about System Center Configuration Manager user accounts, see [Technical Reference for Accounts Used in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=248317) in the TechNet library.

## EXAMPLES

### Example 1: Get a user account by using its name
```
PS C:\>Get-CMAccount -Name "CONTOSO\ENarvaez"
```

This command gets a user account.

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

### -UserName


```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

[New-CMAccount](xref:ConfigurationManager/vlatest/New-CMAccount.md)

[Remove-CMAccount](xref:ConfigurationManager/vlatest/Remove-CMAccount.md)

[Set-CMAccount](xref:ConfigurationManager/vlatest/Set-CMAccount.md)


