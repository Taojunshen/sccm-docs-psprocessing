---
external help file: AdminUI.PS.Sum-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834020
schema: 2.0.0
ms.assetid: A33A1535-F234-4E1A-896D-2832DDA6B2A3
updated_at: 1/27/2017 5:25 PM
ms.date: 1/27/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMWindowsServicingPlan.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMWindowsServicingPlan.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/342b83622089894f77967bf4f9c2b47fa45b9b8a/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMWindowsServicingPlan.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMWindowsServicingPlan

## SYNOPSIS
Gets a Windows 10 servicing plan.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMWindowsServicingPlan [[-Name] <String>] [-Fast] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMWindowsServicingPlan [-Id] <Int32> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMWindowsServicingPlan** cmdlet gets a Windows 10 servicing plan.

## EXAMPLES

### Example 1: Get all servicing plans
```
PS C:\> Get-CMWindowsServicingPlan -Fast
```

This command gets all Windows 10 servicing plans.
The command does not return lazy properties.

### Example 2: Get a servicing plan by name
```
PS C:\> Get-CMWindowsServicingPlan -Name "SvcPlan01"
```

This command returns the Windows 10 servicing plan named SvcPlan01.

## PARAMETERS

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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
Specifies the AutoDeploymentID of a servicing plan.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a servicing plan.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: False
Position: 0
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

[New-CMWindowsServicingPlan](xref:ConfigurationManager/vlatest/New-CMWindowsServicingPlan.md)


