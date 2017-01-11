---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833871
schema: 2.0.0
ms.assetid: EBE1B874-1B5D-458D-9BBF-FDC66BA81FBA
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMHardwareRequirement.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMHardwareRequirement.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMHardwareRequirement.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMHardwareRequirement

## SYNOPSIS
Changes Configuration Manager hardware requirement settings for a product.

## SYNTAX

### SetByName (Default)
```
Set-CMHardwareRequirement -Product <String> [-MinCpu <Int32>] [-MinDiskFree <Int64>] [-MinDiskSize <Int64>]
 [-MinRam <Int64>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMHardwareRequirement -InputObject <IResultObject> [-MinCpu <Int32>] [-MinDiskFree <Int64>]
 [-MinDiskSize <Int64>] [-MinRam <Int64>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMHardwareRequirement** cmdlet changes settings for hardware requirements for software products.

Microsoft System Center Configuration Manager manages Asset Intelligence information, including hardware requirements, for different software products.
You can add, modify, or delete your own hardware requirements, but you cannot change built-in hardware requirements.

You can use this cmdlet to modify the minimum requirements associated with a software product or change the name that Configuration Manager uses for a product.
You can specify a product by name or obtain a product by using the **Get-CMHardwareRequirement** cmdlet.

## EXAMPLES

### Example 1: Change minimum RAM value
```
PS C:\> Set-CMHardwareRequirement -Product "Accounts Program" -MinRam 161072
```

This command sets the minimum RAM value for a specified product.

### Example 2: Change minimum disk size value for a hardware requirements object
```
PS C:\> $CMHR = Get-CMHardwareRequirement -Product "Accounts Program"
PS C:\> Set-CMHardwareRequirement -InputObject $CMHR -MinDiskSize 1600000
```

The first command gets the hardware requirements object for Accounts Program and stores it in the $CMHR variable.

The second command changes the minimum disk size for the object stored in $CMHR.

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
Specifies a hardware requirement object.
To obtain a hardware requirement object, use the [Get-CMHardwareRequirement](./Get-CMHardwareRequirement.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MinCpu
Specifies a minimum CPU speed, in megahertz (MHz), required for a software product.

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

### -MinDiskFree
Specifies a minimum amount of available disk memory, in kilobytes (KB), required for a software product.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinDiskSize
Specifies a minimum disk size, in kilobytes, required for a software product.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinRam
Specifies a minimum amount of random access memory (RAM), in kilobytes, required for a software product.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Product
Specifies the name of a software product name.

```yaml
Type: String
Parameter Sets: SetByName
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

[Get-CMHardwareRequirement](xref:ConfigurationManager/vlatest/Get-CMHardwareRequirement.md)

[New-CMHardwareRequirement](xref:ConfigurationManager/vlatest/New-CMHardwareRequirement.md)

[Remove-CMHardwareRequirement](xref:ConfigurationManager/vlatest/Remove-CMHardwareRequirement.md)
