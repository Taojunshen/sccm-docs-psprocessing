---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834205
schema: 2.0.0
ms.assetid: A636E1DD-49D4-4A9D-94BE-167F3D9A4D5D
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCloudDistributionPoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCloudDistributionPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCloudDistributionPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMCloudDistributionPoint

## SYNOPSIS
Gets cloud-based distribution points.

## SYNTAX

### SearchByGroupName (Default)
```
Get-CMCloudDistributionPoint -DistributionPointGroupName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMCloudDistributionPoint -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMCloudDistributionPoint [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByGroupId
```
Get-CMCloudDistributionPoint -DistributionPointGroupId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByGroup
```
Get-CMCloudDistributionPoint -DistributionPointGroup <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCloudDistributionPoint** cmdlet gets one or more cloud-based distribution points in Microsoft System Center Configuration Manager.

In Configuration Manager, you can use a cloud service in Azure to host a distribution point for storing files to download to clients.
You can send packages and apps to and host packages and apps in cloud distribution points.
For more information about cloud distribution points, see [Planning for Content Management in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266223) on TechNet.

You can use the **Get-CMCloudDistributionPoint** cmdlet to get distribution points to use with other cmdlets.
For example, you might want to get a distribution point and then use the [Stop-CMCloudDistributionPoint](./Stop-CMCloudDistributionPoint.md) cmdlet to suspend it.

## EXAMPLES

### Example 1: Get all cloud distribution points
```
PS C:\> Get-CMCloudDistributionPoint
```

This command gets all the cloud distribution points.

### Example 2: Get a cloud distribution point by name
```
PS C:\> Get-CMCloudDistributionPoint -Name "West01"
```

This command gets a distribution point named West01.

### Example 3: Get a cloud distribution point by ID
```
PS C:\> Get-CMCloudDistributionPoint -Id "16777230"
```

This command gets a distribution point with the specified ID.

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

### -DistributionPointGroup
Specifies a **CMDistributionPointGroup** object.
To get a **CMDistributionPointGroup** object, use the [Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByGroup
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroupId
Specifies the ID of a distribution point group.

```yaml
Type: String
Parameter Sets: SearchByGroupId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
Specifies the name of a distribution point group.

```yaml
Type: String
Parameter Sets: SearchByGroupName
Aliases: 
Required: True
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
Specifies an array of identifiers for cloud distribution points.
You can use a comma separated list.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: AzureServiceId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a cloud distribution point.

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

[New-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/New-CMCloudDistributionPoint.md)

[Remove-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Remove-CMCloudDistributionPoint.md)

[Set-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Set-CMCloudDistributionPoint.md)

[Start-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Start-CMCloudDistributionPoint.md)

[Stop-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Stop-CMCloudDistributionPoint.md)
