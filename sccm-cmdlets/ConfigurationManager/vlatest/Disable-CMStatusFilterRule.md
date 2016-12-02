---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833961
schema: 2.0.0
ms.assetid: AF1704A4-0EC9-4228-AEF3-BC4D7434B4CD
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Disable-CMStatusFilterRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Disable-CMStatusFilterRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Disable-CMStatusFilterRule

## SYNOPSIS
Disables a Configuration Manager filter rule for status messages.

## SYNTAX

### SearchByValue (Default)
```
Disable-CMStatusFilterRule -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Disable-CMStatusFilterRule [-SiteCode <String>] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-CMStatusFilterRule** cmdlet disables a specified Microsoft System Center Configuration Manager filter rule for status messages.

Status filter rules specify how System Center Configuration Manager responds to status messages.
Each filter rule contains criteria and actions for status messages.
You configure status filter rules for each site, not across all sites.

Use the rule name and site code to specify a rule to disable.
You can use the Enable-CMStatusFilterRule cmdlet to enable a rule.
To remove a rule permanently, use the Remove-CMStatusFilterRule cmdlet.

## EXAMPLES

### Example 1: Disable a status filter rule
```
PS C:\>Disable-CMStatusFilterRule -Name "Status change to critical" -SiteCode "CM1"
```

This command disables a status filter rule that has the specified name in a site that has the site code CM1.

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
Specifies a status filter rule object to disable.
To obtain a status filter rule object, use the Get-CMStatusFilterRule cmdlet.

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

### -Name


```yaml
Type: String
Parameter Sets: SearchByName
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
Parameter Sets: SearchByName
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

[Enable-CMStatusFilterRule](xref:ConfigurationManager/vlatest/Enable-CMStatusFilterRule.md)

[Get-CMStatusFilterRule](xref:ConfigurationManager/vlatest/Get-CMStatusFilterRule.md)

[New-CMStatusFilterRule](xref:ConfigurationManager/vlatest/New-CMStatusFilterRule.md)

[Remove-CMStatusFilterRule](xref:ConfigurationManager/vlatest/Remove-CMStatusFilterRule.md)

[Set-CMStatusFilterRule](xref:ConfigurationManager/vlatest/Set-CMStatusFilterRule.md)

