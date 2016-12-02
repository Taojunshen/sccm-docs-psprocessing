---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834213
schema: 2.0.0
ms.assetid: 140F1D39-4D3B-4F73-BB67-676B5080A972
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMSoftwareMeteringRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMSoftwareMeteringRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMSoftwareMeteringRule

## SYNOPSIS
Removes Configuration Manager software metering rules.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMSoftwareMeteringRule -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMSoftwareMeteringRule -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSoftwareMeteringRule -ProductName <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSoftwareMeteringRule** cmdlet removes one or more software metering rules from Microsoft System Center Configuration Manager.

Software metering monitors and collects software usage data from System Center Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

You can specify rules to disable by ID or by product name, or use the Get-CMSoftwareMeteringRule cmdlet.
You can use the Disable-CMSoftwareMeteringRule to temporarily suspend a rule.

For more information about software metering in System Center Configuration Manager, see [Introduction to Software Metering in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268432) on TechNet.

## EXAMPLES

### Example 1: Remove rules for a product
```
PS C:\>Remove-CMSoftwareMeteringRule -ProductName "Accounting Package"
Remove
Are you sure you wish to remove SoftwareMeteringRule: RuleID=16777220? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

Remove
Are you sure you wish to remove SoftwareMeteringRule: RuleID=16777221? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

This command removes any software metering rules for a product named Accounting Package.
In this example, there are two rules for that product.
The command does not include the *Force* parameter, so the cmdlet prompts for confirmation for both rules.

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

### -Id
Specifies an array of IDs for software metering rules.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: RuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software metering rule object.
To obtain a software metering rule object, use the Get-CMSoftwareMeteringRule cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProductName
Specifies a name for a product that a rule meters.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

[Disable-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Disable-CMSoftwareMeteringRule.md)

[Enable-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Enable-CMSoftwareMeteringRule.md)

[Get-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Get-CMSoftwareMeteringRule.md)

[New-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/New-CMSoftwareMeteringRule.md)

[Set-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Set-CMSoftwareMeteringRule.md)


