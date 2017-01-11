---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834003
schema: 2.0.0
ms.assetid: 9CD7B8EA-2F75-4AB0-B5FA-5CFD8855C1E9
updated_at: 12/7/2016 11:21 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Enable-CMTaskSequence.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Enable-CMTaskSequence.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4bb0549ab9452d0d1c9cdf57cfbc8185eefd798c/sccm-cmdlets/ConfigurationManager/vlatest/Enable-CMTaskSequence.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Enable-CMTaskSequence

## SYNOPSIS
This cmdlet is deprecated.
Use the [Set-CMTaskSequence](./Set-CMTaskSequence.md) cmdlet to enable a task sequence.

## SYNTAX

### SearchByValueMandatory (Default)
```
Enable-CMTaskSequence -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Enable-CMTaskSequence -TaskSequencePackageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Enable-CMTaskSequence -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
This cmdlet is deprecated.
Use the [Set-CMTaskSequence](./Set-CMTaskSequence.md) cmdlet to enable a task sequence.

## EXAMPLES


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
Specifies a task sequence object.
To obtain a task sequence object, use the [Get-CMTaskSequence](./Get-CMTaskSequence.md) cmdlet.

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

### -Name
Specifies a name for a task sequence.

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

### -TaskSequencePackageId
Specifies the package ID of a task sequence.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId, Id
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

[Disable-CMTaskSequence](xref:ConfigurationManager/vlatest/Disable-CMTaskSequence.md)

[Export-CMTaskSequence](xref:ConfigurationManager/vlatest/Export-CMTaskSequence.md)

[Get-CMTaskSequence](xref:ConfigurationManager/vlatest/Get-CMTaskSequence.md)

[Import-CMTaskSequence](xref:ConfigurationManager/vlatest/Import-CMTaskSequence.md)

[New-CMTaskSequence](xref:ConfigurationManager/vlatest/New-CMTaskSequence.md)

[Remove-CMTaskSequence](xref:ConfigurationManager/vlatest/Remove-CMTaskSequence.md)

[Set-CMTaskSequence](xref:ConfigurationManager/vlatest/Set-CMTaskSequence.md)


