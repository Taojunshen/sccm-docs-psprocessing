---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834169
schema: 2.0.0
ms.assetid: B5D0F1F5-75B0-42FF-8C3E-9FEB9551C18D
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMSoftwareUpdateAutoDeploymentRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMSoftwareUpdateAutoDeploymentRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Invoke-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Runs a Configuration Manager deployment rule for automatic software updates.

## SYNTAX

### SearchByIdMandatory (Default)
```
Invoke-CMSoftwareUpdateAutoDeploymentRule -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMSoftwareUpdateAutoDeploymentRule -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMSoftwareUpdateAutoDeploymentRule -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMSoftwareUpdateAutoDeploymentRule** cmdlet runs a Microsoft System Center Configuration Manager deployment rule for automatic software updates immediately instead of according to its schedule.

System Center Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, System Center Configuration Manager adds updates that qualify for the rule to a software update group.
The System Center Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

You can specify rules to run by ID or by name, or specify a rule object by using the Get-CMSoftwareUpdateAutoDeploymentRule cmdlet.
You cannot run a disabled rule.
You can use the Enable-CMSoftwareUpdateAutoDeploymentRule cmdlet to enable a rule and then run it.

## EXAMPLES

### Example 1: Invoke a deployment rule
```
PS C:\>Invoke-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Security Updates"
```

This command runs a rule called Weekly Security Updates.

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
Specifies an array of IDs for rules for automatic deployment of software updates.
This value is the **AutoDeploymentID** property of the deployment rule object.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software update automatic deployment rule object.
To obtain a deployment rule object, use the **Get-CMSoftwareUpdateAutoDeploymentRule** cmdlet.

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
Specifies a name of a rule for automatic deployment of software updates.

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

[Disable-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Enable-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Get-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Remove-CMSoftwareUpdateAutoDeploymentRule.md)


