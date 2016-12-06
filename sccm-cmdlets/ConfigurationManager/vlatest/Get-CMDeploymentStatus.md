---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833580
schema: 2.0.0
ms.assetid: AE6E47B5-5E78-4C8C-9A65-E7F25712BD92
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDeploymentStatus.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDeploymentStatus.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMDeploymentStatus

## SYNOPSIS
Gets the status of classic software distribution deployments.

## SYNTAX

### SearchByName (Default)
```
Get-CMDeploymentStatus [-Name <String>] [-StatusType <PackageDeploymentStatusType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMDeploymentStatus -DeploymentId <String> [-StatusType <PackageDeploymentStatusType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByPackageId
```
Get-CMDeploymentStatus -PackageId <String> [-StatusType <PackageDeploymentStatusType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMDeploymentStatus [-StatusType <PackageDeploymentStatusType>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeploymentStatus** cmdlet gets the status of one or more classic software distribution deployments.
A classic software distribution is a legacy software distribution program on a client.

## EXAMPLES

### Example 1: Get the status of a deployment
```
PS C:\>Get-CMDeploymentStatus -Name "Depack01"
```

This command gets the status of a deployment that is distributed to Configuration Manager clients by using the deployment package named Depack01.

## PARAMETERS

### -DeploymentId


```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: Id

Required: True
Position: Named
Default value: None
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


```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of deployment packages.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: PackageName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageId


```yaml
Type: String
Parameter Sets: SearchByPackageId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatusType


```yaml
Type: PackageDeploymentStatusType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Success, InProgress, RequirementsNotMet, Unknown, Error

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

[Get-CMDeploymentType](xref:ConfigurationManager/vlatest/Get-CMDeploymentType.md)

[Get-CMDeploymentPackage](xref:ConfigurationManager/vlatest/Get-CMDeploymentPackage.md)

[Invoke-CMDeploymentSummarization](xref:ConfigurationManager/vlatest/Invoke-CMDeploymentSummarization.md)

[Remove-CMDeployment](xref:ConfigurationManager/vlatest/Remove-CMDeployment.md)


