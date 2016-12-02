---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833920
schema: 2.0.0
ms.assetid: D7D57FDA-A9BC-40D4-B55B-4190280B2E5F
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMBaseline.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMBaseline.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMBaseline

## SYNOPSIS
Removes configuration baselines.

## SYNTAX

### SearchByIdMandatory (Default)
```
Remove-CMBaseline [-Id] <Int32> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMBaseline [-Name] <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMBaseline [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMBaseline** cmdlet removes one or more configuration baseline items in Microsoft System Center Configuration Manager.
You must remove all references to a configuration baseline before you can remove the configuration baseline.
After you remove a configuration baseline, System Center Configuration Manager removes the configuration baseline from the collection of devices to which you deployed it, and Configuration Manager no longer assesses their compliance with the configuration baseline.

## EXAMPLES

### Example 1: Remove a baseline configuration by using a name
```
PS C:\>Remove-CMBaseline -Name "BLConfigContoso02"
```

This command removes the configuration baseline named BLConfigContoso02.

### Example 2: Remove a baseline configuration by using an ID
```
PS C:\>Remove-CMBaseline -Id "16777366"
```

This command removes the configuration baseline that has the ID 16777366.

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

[Export-CMBaseline](xref:ConfigurationManager/vlatest/Export-CMBaseline.md)

[Get-CMBaseline](xref:ConfigurationManager/vlatest/Get-CMBaseline.md)

[Import-CMBaseline](xref:ConfigurationManager/vlatest/Import-CMBaseline.md)

[New-CMBaseline](xref:ConfigurationManager/vlatest/New-CMBaseline.md)

[Set-CMBaseline](xref:ConfigurationManager/vlatest/Set-CMBaseline.md)

[Get-CMBaselineXMLDefinition](xref:ConfigurationManager/vlatest/Get-CMBaselineXMLDefinition.md)

[Get-CMBaselineSummarizationSchedule](xref:ConfigurationManager/vlatest/Get-CMBaselineSummarizationSchedule.md)


