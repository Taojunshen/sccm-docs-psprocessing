---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833916
schema: 2.0.0
ms.assetid: B1D024FB-2D23-40B5-A7F4-C8F4E4EE3273
updated_at: 1/27/2017 6:21 PM
ms.date: 1/27/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAutoDeploymentRuleDeployment.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAutoDeploymentRuleDeployment.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0d568aaa1e8e67f5e8fbff3a4676788779689ecb/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAutoDeploymentRuleDeployment.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMAutoDeploymentRuleDeployment

## SYNOPSIS
Removes a deployment from an auto deployment rule.

## SYNTAX

```
Remove-CMAutoDeploymentRuleDeployment [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAutoDeploymentRuleDeployment** cmdlet removes a deployment from an auto deployment rule.

## EXAMPLES

### Example 1: Remove a deployment
```
PS C:\> $Deployments = Get-CMAutoDeploymentRuleDeployment -Name "TestRule01"
PS C:\> Remove-CMAutoDeploymentRuleDeployment -InputObject $Deployments[0]
```

The first command gets the deployment objects associated with the automatic deployment rule named TestRule01 and stores the objects in the $Deployments variable.

The second command removes the first deployment object stored in $Deployments.

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

### -InputObject
Specifies an automatic deployment rule deployment object.
To obtain a deployment object, use the [Get-CMAutoDeploymentRuleDeployment](./Get-CMAutoDeploymentRuleDeployment.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: AutoDeploymentRuleDeployment

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-CMAutoDeploymentRuleDeployment](xref:ConfigurationManager/vlatest/Get-CMAutoDeploymentRuleDeployment.md)

[New-CMAutoDeploymentRuleDeployment](xref:ConfigurationManager/vlatest/New-CMAutoDeploymentRuleDeployment.md)

[Set-CMAutoDeploymentRuleDeployment](xref:ConfigurationManager/vlatest/Set-CMAutoDeploymentRuleDeployment.md)
