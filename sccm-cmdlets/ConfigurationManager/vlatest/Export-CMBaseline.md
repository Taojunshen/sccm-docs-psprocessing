---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834013
schema: 2.0.0
ms.assetid: E01D931B-EEB2-4A1E-A206-CCE907238209
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMBaseline.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMBaseline.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Export-CMBaseline

## SYNOPSIS
Exports configuration baselines.

## SYNTAX

### SearchByNameMandatory (Default)
```
Export-CMBaseline [-Name] <String> -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Export-CMBaseline [-Id] <Int32> -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Export-CMBaseline [-InputObject] <IResultObject> -Path <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMBaseline** cmdlet exports configuration baselines in a cabinet (.cab) file format from a Microsoft System Center Configuration Manager site.
You can then import it to the same or a different System Center Configuration Manager site.
Configuration data is converted to desired configuration managementâ€Ž (DCM) Digest.

## EXAMPLES

### Example 1: Export a baseline
```
PS C:\>Export-CMBaseline -Name "BLConfig01" -Path "\\Contoso01\CM\Toolbox\BaselineW2K8.cab"
```

This command exports the configuration baseline named BLConfig01 to the file named BaselineW2K8.cab.

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

### -Id
Specifies an array of IDs of configuration baselines.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMBaseline** object.
To obtain a **CMBaseline** object, use the Get-CMBaseline cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration baselines.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the full path of the cabinet (.cab) file.

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

[Disable-CMBaseline](xref:ConfigurationManager/vlatest/Disable-CMBaseline.md)

[Enable-CMBaseline](xref:ConfigurationManager/vlatest/Enable-CMBaseline.md)

[Get-CMBaseline](xref:ConfigurationManager/vlatest/Get-CMBaseline.md)

[Import-CMBaseline](xref:ConfigurationManager/vlatest/Import-CMBaseline.md)

[New-CMBaseline](xref:ConfigurationManager/vlatest/New-CMBaseline.md)

[Remove-CMBaseline](xref:ConfigurationManager/vlatest/Remove-CMBaseline.md)

[Set-CMBaseline](xref:ConfigurationManager/vlatest/Set-CMBaseline.md)

[Get-CMBaselineXMLDefinition](xref:ConfigurationManager/vlatest/Get-CMBaselineXMLDefinition.md)

[Get-CMBaselineSummarizationSchedule](xref:ConfigurationManager/vlatest/Get-CMBaselineSummarizationSchedule.md)


