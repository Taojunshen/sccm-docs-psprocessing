---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833901
schema: 2.0.0
ms.assetid: 25E50823-D771-43CD-98E0-B5463B1DB374
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateAutoDeploymentRule.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateAutoDeploymentRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateAutoDeploymentRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Gets Configuration Manager deployment rules for automatic software updates.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateAutoDeploymentRule [[-Name] <String>] [-IsServicingPlan <Boolean>] [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareUpdateAutoDeploymentRule [-Id] <Int32[]> [-IsServicingPlan <Boolean>] [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateAutoDeploymentRule** cmdlet gets specified Microsoft System Center Configuration Manager deployment rules for automatic software updates.

System Center Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, System Center Configuration Manager adds updates that qualify for the rule to a software update group.
The System Center Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

You can specify rules by ID or by name.
You can use this cmdlet to get deployment rules for automatic software updates to use with other cmdlets, such as the Invoke-CMSoftwareUpdateAutoDeploymentRule cmdlet or the [Remove-CMSoftwareUpdateAutoDeploymentRule](./Remove-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.

## EXAMPLES

### Example 1: Get a deployment rule by name
```
PS C:\> Get-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
```

This command gets a deployment rule named Weekly Driver Updates.

### Example 2: Get a deployment rule by ID
```
PS C:\> Get-CMSoftwareUpdateAutoDeploymentRule -Id "16777217"
```

This command gets a deployment rule that has the ID 16777217.

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
Type: Int32[]
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsServicingPlan


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name of a rule for automatic deployment of software updates.

```yaml
Type: String
Parameter Sets: SearchByName
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

[Disable-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Enable-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Invoke-CMSoftwareUpdateAutoDeploymentRule.md)

[New-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/New-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Remove-CMSoftwareUpdateAutoDeploymentRule.md)

[Set-CMSoftwareUpdateAutoDeploymentRule](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdateAutoDeploymentRule.md)


