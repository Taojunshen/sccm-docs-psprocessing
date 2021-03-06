---
external help file: AdminUI.PS.Accounts.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834215
schema: 2.0.0
ms.assetid: 759B2F3E-8C83-44AB-9857-2EFF8FDF3338
updated_at: 1/7/2017 2:02 AM
ms.date: 1/7/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMAccount.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMAccount.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/8a6b9ef671600123aa3999d5e8820fa3d2bcf3e3/sccm-cmdlets/ConfigurationManager/vlatest/New-CMAccount.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMAccount

## SYNOPSIS
Creates a Configuration Manager user account.

## SYNTAX

```
New-CMAccount -Password <SecureString> -UserName <String> [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAccount** cmdlet creates a new user account in Microsoft System Center Configuration Manager.
A **CMAccount** is a user account that System Center Configuration Manager uses to connect to various system and network resources.
For more information about user accounts, see [Technical Reference for Accounts Used in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=248317) in the TechNet library.

## EXAMPLES

### Example 1: Create a user account by using name and password
```
PS C:\> $Secure = ConvertTo-SecureString -String "Pas$W0rd" -AsPlainText -Force
PS C:\> New-CMAccount -Name "TSQA\PFuller" -Password $Secure -SiteCode "CM2"
```

The first command creates a password as a secure string.

The second command creates an account by using the secure string.

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

### -Password
Specifies a secure string that contains the password for the user account.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a Configuration Manager site code.

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

[Get-CMAccount](xref:ConfigurationManager/vlatest/Get-CMAccount.md)

[Remove-CMAccount](xref:ConfigurationManager/vlatest/Remove-CMAccount.md)

[Set-CMAccount](xref:ConfigurationManager/vlatest/Set-CMAccount.md)
