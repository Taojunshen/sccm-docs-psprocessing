---
external help file: AdminUI.PS.Accounts.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833605
schema: 2.0.0
ms.assetid: 5DA6777B-C1CC-4FC0-A85C-6185F7AB69BE
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMAccount.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMAccount.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMAccount

## SYNOPSIS
Sets a Configuration Manager user account.

## SYNTAX

### SetAccountByName (Default)
```
Set-CMAccount [-Password <SecureString>] -UserName <String> [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetAccountByObject
```
Set-CMAccount [-Password <SecureString>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAccount** cmdlet sets a user account in Microsoft System Center Configuration Manager.
A **CMAccount** is a user account that Configuration Manager uses to connect to various system and network resources.
For more information about user accounts, see [Technical Reference for Accounts Used in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=248317) in the TechNet library.

## EXAMPLES

### Example 1: Set an account by using name and password
```
PS C:\>$Secure = Read-Host -AsSecureString
PS C:\> $ConfirmSecure = Read-Host -AsSecureString
PS C:\> Set-CMAccount -Name " TSQA\PFuller" -Password $Secure -ConfirmPassword $ConfirmSecure -SiteCode "CM2"
```

The first command creates a variable as a secure string.

The second command creates another variable as a secure string.

The third command sets the password for the account.

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

### -InputObject
Specifies a user account object.
You can get a user account object by using the Get-CMAccount cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetAccountByObject
Aliases: Account

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Password
Specifies a secure string that contains the password for the user account.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a Configuration Manager site code.

```yaml
Type: String
Parameter Sets: SetAccountByName
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
Parameter Sets: SetAccountByName
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

[New-CMAccount](xref:ConfigurationManager/vlatest/New-CMAccount.md)

[Remove-CMAccount](xref:ConfigurationManager/vlatest/Remove-CMAccount.md)


