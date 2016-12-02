---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834035
schema: 2.0.0
ms.assetid: 484FFAF5-FE27-4B04-93D0-A7F2337ADF86
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMBaseline.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMBaseline.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Import-CMBaseline

## SYNOPSIS
Imports Configuration Manager baselines.

## SYNTAX

```
Import-CMBaseline -FileName <String[]> [-DuplicateWhileImporting] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMBaseline** cmdlet imports Microsoft System Center Configuration Manager baselines from files.
A baseline is a collection of configuration items that Configuration Manager uses to evaluate whether a computer complies with software requirements.
After you import a baseline, you can deploy it to a collection so that devices in that collection download the configuration baseline and assess compliance with it.

You can import a configuration baseline from a .cab file that conforms to the Service Modeling Language (SML) schema.
For example, you might import data previously exported from Configuration Manager or best practices included in a Monitoring Pack for Configuration Manager.

When you import a baseline configuration, you have the option of creating a local copy.
You can modify that baseline in the future.

## EXAMPLES

### Example 1: Import a baseline
```
PS C:\>Import-CMBaseline -FileName "\\ContosoServer01\Public\CM\BaselineW2K8.cab"
```

This command imports a baseline from a file named BaselineW2K8.cab.

### Example 2: Import multiple baselines
```
PS C:\>Import-CMBaseline -FileName "\\ContosoServer01\Public\CM\BaselineW2K8.cab","\\ContosoServer01\Public\CM\BaselineWin7.cab" -DuplicateWhileImporting
```

This command imports baselines from .cab files named BaselineW2K8.cab and BaselineWin7.cab.
This command uses the *DuplicateWhileImporting* parameter, so the command creates an editable version of the configuration baselines.

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

### -DuplicateWhileImporting
Indicates that the cmdlet duplicates a baseline while it imports the baseline.
If you duplicate a baseline, you can modify that baseline in the future.

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

### -FileName
Specifies an array of .cab file names.
Each file contains Configuration Manager configuration items.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
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

[New-CMBaseline](xref:ConfigurationManager/vlatest/New-CMBaseline.md)

[Remove-CMBaseline](xref:ConfigurationManager/vlatest/Remove-CMBaseline.md)

[Set-CMBaseline](xref:ConfigurationManager/vlatest/Set-CMBaseline.md)


