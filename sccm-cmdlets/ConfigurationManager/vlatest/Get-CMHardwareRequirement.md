---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833714
schema: 2.0.0
ms.assetid: 64498870-8A44-440C-B6A6-D0D25C3805FE
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMHardwareRequirement.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMHardwareRequirement.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMHardwareRequirement.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMHardwareRequirement

## SYNOPSIS
Gets Configuration Manager hardware requirements for products.

## SYNTAX

```
Get-CMHardwareRequirement [-Product <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMHardwareRequirement** cmdlet gets hardware requirements objects for software products.

Microsoft System Center Configuration Manager manages Asset Intelligence information, including hardware requirements, for different software products.
You can add, modify, or delete your own hardware requirements, but you cannot change built-in hardware requirement objects.

You can use this cmdlet to get all the hardware requirement objects for a System Center Configuration Manager server or one or more hardware requirement objects for a specified product names.
You can use hardware requirements with other cmdlets, such as the **Remove-CMHardwareRequirement** cmdlet or the **Set-CMHardwareRequirement** cmdlet.

## EXAMPLES

### Example 1: Get a hardware requirement
```
PS C:\> Get-CMHardwareRequirement -Product "Accounts Program"
IsLocal     : False
MinCPU      : 233
MinDiskFree : 1572864
MinDiskSize : 10485760
MinRAM      : 131072
Product     : Accounts Program
State       : 0
```

This command gets the hardware requirement object for a product named Accounts Program.

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

### -Product
Specifies the name of a software product.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMHardwareRequirement](xref:ConfigurationManager/vlatest/New-CMHardwareRequirement.md)

[Remove-CMHardwareRequirement](xref:ConfigurationManager/vlatest/Remove-CMHardwareRequirement.md)

[Set-CMHardwareRequirement](xref:ConfigurationManager/vlatest/Set-CMHardwareRequirement.md)


