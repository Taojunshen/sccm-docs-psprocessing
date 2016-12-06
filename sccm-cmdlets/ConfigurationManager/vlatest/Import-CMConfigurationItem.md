---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834055
schema: 2.0.0
ms.assetid: 79D7AE04-6894-4349-AD82-C50735D1F4EF
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMConfigurationItem.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMConfigurationItem.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Import-CMConfigurationItem

## SYNOPSIS
Imports Configuration Manager configuration items.

## SYNTAX

```
Import-CMConfigurationItem -FileName <String[]> [-DuplicateWhileImporting] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMConfigurationItem** cmdlet imports Microsoft System Center Configuration Manager configuration items from one or more cabinet files.
The files that you import must conform to the Service Modeling Language (SML) schema and can contain information about configuration data from one of the following sources: 

- Best practices from a System Center Configuration Manager Configuration Pack.
- Configuration data that you have externally authored and packaged into a cabinet (.cab) file.
- Configuration data exported from System Center Configuration Manager.

Configuration items contain one or more settings, along with compliance rules.
Items usually define a unit of configuration you want to monitor.

## EXAMPLES

### Example 1: Import configuration items
```
PS C:\>Import-CMConfigurationItem -FileName "\\atc-dist-01\Public\CM\AdminUITeam\CIData\7389_OSCI.cab","\\atc-dist-01\Public\CM\AdminUITeam\CIData\7452OS_1.cab"
```

This command imports configuration items from the files 7389_OSCI.cab and 7452OS_1.cab.

### Example 2: Import configuration items and create duplicate configuration items
```
PS C:\>Import-CMConfigurationItem -FileName "\\Contoso01\Public\CM\7389_OSCI.cab","\\ Contoso01\Public\CM\7452OS_1.cab" -DuplicateWhileImporting
```

This command imports configuration items from the files 7389_OSCI.cab and 7452OS_1.cab.
The *DuplicateWhileImporting* parameter indicates that imports configuration items that exist in System Center Configuration Manager as duplicate configuration items.

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
Indicates that Configuration Manager imports configuration items that exist in Configuration Manager as duplicate configuration items.

Use this parameter to create a configuration item when you want an exact copy of a configuration item that you import to use as your starting point, but you want to modify it to create an independent configuration item from the original.

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
Specifies an array of names of cabinet (cab) files.

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

Use this parameter to create a configuration item when you want an exact copy of a configuration item that you import to use as your starting point, but you want to modify it to create an independent configuration item from the original.

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

Use this parameter to create a configuration item when you want an exact copy of a configuration item that you import to use as your starting point, but you want to modify it to create an independent configuration item from the original.

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

[Get-CMConfigurationItem](xref:ConfigurationManager/vlatest/Get-CMConfigurationItem.md)

[Set-CMConfigurationItem](xref:ConfigurationManager/vlatest/Set-CMConfigurationItem.md)

[New-CMConfigurationItem](xref:ConfigurationManager/vlatest/New-CMConfigurationItem.md)

[Remove-CMConfigurationItem](xref:ConfigurationManager/vlatest/Remove-CMConfigurationItem.md)

[Export-CMConfigurationItem](xref:ConfigurationManager/vlatest/Export-CMConfigurationItem.md)


