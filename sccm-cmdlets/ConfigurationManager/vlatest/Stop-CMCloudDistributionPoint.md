---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834235
schema: 2.0.0
ms.assetid: 4C9E537F-007B-45FE-B82F-CE17CB39B29B
updated_at: 12/6/2016 11:47 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Stop-CMCloudDistributionPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/322e1e3dae6ba53c3384ca0bf1a1079481b8ae30/sccm-cmdlets/ConfigurationManager/vlatest/Stop-CMCloudDistributionPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Stop-CMCloudDistributionPoint

## SYNOPSIS
Stops the cloud distribution point service.

## SYNTAX

### SearchByValueMandatory (Default)
```
Stop-CMCloudDistributionPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Stop-CMCloudDistributionPoint -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Stop-CMCloudDistributionPoint -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Stop-CMCloudDistributionPoint** cmdlet stops the cloud distribution point service.

If you use the **Stop-CMCloudDistributionPoint** cmdlet, System Center Configuration Manager does not delete content from the distribution point and does not prevent the site server from transferring additional content to the distribution point.
While the cloud distribution point service is stopped, the cloud distribution point does not distribute content.
Use the [Start-CMCloudDistributionPoint](./Start-CMCloudDistributionPoint.md) cmdlet to restart distribution.

For example, you might want to stop a cloud service when usage reaches a data threshold and then restart it at a later time.

## EXAMPLES

### Example 1: Stop the cloud distribution point service using an ID
```
PS C:\>Stop-CMCloudDistributionPoint -Id "16777242"
```

This command stops the cloud distribution point service for the cloud distribution point that has the specified identifier.

### Example 2: Stop the cloud distribution point service using a name
```
PS C:\>Stop-CMCloudDistributionPoint -Name "West01"
```

This command stops the cloud distribution point service for the cloud distribution point named West01.

### Example 3: Stop the cloud distribution point service using an object
```
PS C:\>$DistPnt = Get-CMCloudDistributionPoint -Id "16777242"
PS C:\> Stop-CMCloudDistributionPoint -InputObject $DistPnt
```

The first command uses the **Get-CMCloudDistributionPoint** cmdlet to get the distribution point with the specified identifier, and then stores it in the $DistPnt variable.

The second command stops the cloud distribution point service for the distribution point stored in $DistPnt.

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

### -InputObject
Specifies a cloud distribution point object.
To get a cloud distribution point object, you can use the **Get-CMCloudDistributionPoint** cmdlet.

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
Specifies the name of a cloud distribution point.

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

[Get-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Get-CMCloudDistributionPoint.md)

[New-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/New-CMCloudDistributionPoint.md)

[Remove-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Remove-CMCloudDistributionPoint.md)

[Set-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Set-CMCloudDistributionPoint.md)

[Start-CMCloudDistributionPoint](xref:ConfigurationManager/vlatest/Start-CMCloudDistributionPoint.md)
