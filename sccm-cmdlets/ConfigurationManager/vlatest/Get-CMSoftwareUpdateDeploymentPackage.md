---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833909
schema: 2.0.0
ms.assetid: 183D4DE8-9632-41D4-94D3-94CAED832637
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateDeploymentPackage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateDeploymentPackage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMSoftwareUpdateDeploymentPackage

## SYNOPSIS
Retrieves a deployment package.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateDeploymentPackage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareUpdateDeploymentPackage -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateDeploymentPackage** cmdlet retrieves a deployment package for a software update.
A **CMSoftwareUpdateDeploymentPackage** object contains one or more software updates.

## EXAMPLES

### Example 1: Get a deployment package by using a name
```
PS C:\>Get-CMSoftwareUpdateDeploymentPackage -Name "Asdset"
```

This command gets a deployment package named Asdset.

### Example 2: Get a deployment package by using an ID
```
PS C:\>Get-CMSoftwareUpdateDeploymentPackage -Id "ST10000C"
```

This command gets a deployment package that has the ID ST10000C.

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
Specifies an array of IDs for the deployment package.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the deployment package.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
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

[Remove-CMSoftwareUpdateDeploymentPackage](xref:ConfigurationManager/vlatest/Remove-CMSoftwareUpdateDeploymentPackage.md)

[Set-CMSoftwareUpdateDeploymentPackage](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdateDeploymentPackage.md)


