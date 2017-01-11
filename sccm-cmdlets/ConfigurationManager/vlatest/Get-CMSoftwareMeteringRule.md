---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833892
schema: 2.0.0
ms.assetid: C12620B8-D0BF-464F-BF90-BB1658ABE0B4
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareMeteringRule.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareMeteringRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareMeteringRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMSoftwareMeteringRule

## SYNOPSIS
Gets Configuration Manager software metering rules.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareMeteringRule [-ProductName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareMeteringRule -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareMeteringRule** cmdlet gets one or more software metering rules in Microsoft System Center Configuration Manager.
You can use this cmdlet to get rules to pass to other cmdlets, such as the [Enable-CMSoftwareMeteringRule](./Enable-CMSoftwareMeteringRule.md) cmdlet or the [Remove-CMSoftwareMeteringRule](./Remove-CMSoftwareMeteringRule.md) cmdlet.

Software metering monitors and collects software usage data from System Center Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

You can specify rules by ID or by product name.

For more information about software metering in System Center Configuration Manager, see [Introduction to Software Metering in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268432) on TechNet.

## EXAMPLES

### Example 1: Get rules for a product
```
PS C:\> Get-CMSoftwareMeteringRule -ProductName "Accounting Package"
```

This command gets software metering rules for the product named Accounting Package.

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

### -ProductName
Specifies a name for a product that a rule meters.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Disable-CMSoftwareMeteringRule.md)

[Enable-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Enable-CMSoftwareMeteringRule.md)

[New-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/New-CMSoftwareMeteringRule.md)

[Remove-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Remove-CMSoftwareMeteringRule.md)

[Set-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Set-CMSoftwareMeteringRule.md)


