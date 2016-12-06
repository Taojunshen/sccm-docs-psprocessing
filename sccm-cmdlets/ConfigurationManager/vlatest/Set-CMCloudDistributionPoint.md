---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833730
schema: 2.0.0
ms.assetid: F2F9DBD4-F429-4913-82E7-E3E160D4A926
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMCloudDistributionPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMCloudDistributionPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMCloudDistributionPoint

## SYNOPSIS
Changes settings for a cloud-based distribution point.

## SYNTAX

### SetByValue (Default)
```
Set-CMCloudDistributionPoint -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-TrafficOutGB <Int32>] [-StorageQuotaGB <Int32>] [-StorageQuotaGrow <Boolean>]
 [-TrafficOutStopService <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMCloudDistributionPoint -Id <String> [-NewName <String>] [-Description <String>] [-TrafficOutGB <Int32>]
 [-StorageQuotaGB <Int32>] [-StorageQuotaGrow <Boolean>] [-TrafficOutStopService <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCloudDistributionPoint -Name <String> [-NewName <String>] [-Description <String>] [-TrafficOutGB <Int32>]
 [-StorageQuotaGB <Int32>] [-StorageQuotaGrow <Boolean>] [-TrafficOutStopService <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCloudDistributionPoint** cmdlet changes settings for a cloud-based distribution point.

In Microsoft System Center Configuration Manager, you can use a cloud service in Windows Azure to host a distribution point for storing files to download to clients.
You can send packages and apps to and host packages and apps in cloud distribution points. 
For more information about cloud distribution points, see [Planning for Content Management in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266223) on TechNet.

You can use the Set-CMCloudDistributionPoint cmdlet to specify storage alert thresholds and warning levels for content that you deploy to a cloud distribution point.
You can also use the cmdlet to configure settings that enable users and devices to access the content.
You can provide a name and description for the cloud distribution point.

## EXAMPLES

### Example 1: Set values for a distribution point
```
PS C:\>Set-CMCloudDistributionPoint -Id 16777237 -Description "Western distribution point" -Name "West01" -StorageQuotaInGB 50 -TrafficOutInGB 50
```

This command sets the description and name for a distribution point to the provided strings.
It also sets values for the storage quota and data transfer.

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

### -Description


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### -Id
Specifies an array of identifiers for one or more cloud distribution points.
You can use a comma-separated list.

```yaml
Type: String
Parameter Sets: SetById
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for a cloud distribution point.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaGB


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StorageQuotaInGB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaGrow


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

### -TrafficOutGB


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TrafficOutInGB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficOutStopService


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

[Get-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Get-CMCloudDistributionPoint.md)

[New-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/New-CMCloudDistributionPoint.md)

[Remove-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Remove-CMCloudDistributionPoint.md)

[Start-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Start-CMCloudDistributionPoint.md)

[Stop-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Stop-CMCloudDistributionPoint.md)


