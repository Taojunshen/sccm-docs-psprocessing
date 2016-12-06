---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834144
schema: 2.0.0
ms.assetid: F354A3B1-3569-4CC5-962B-5050F0A67DDD
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMVhd.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMVhd.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMVhd

## SYNOPSIS
Modifies VHD images.

## SYNTAX

### SetByValue (Default)
```
Set-CMVhd -InputObject <IResultObject> [-NewName <String>] [-VhdFilePath <String>] [-Version <String>]
 [-Description <String>] [-TaskSequencePackageId <String>] -DistributionPointServerName <String[]>
 [-Timeout <TimeSpan>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMVhd -VhdPackageId <String> [-NewName <String>] [-VhdFilePath <String>] [-Version <String>]
 [-Description <String>] [-TaskSequencePackageId <String>] -DistributionPointServerName <String[]>
 [-Timeout <TimeSpan>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMVhd -Name <String> [-NewName <String>] [-VhdFilePath <String>] [-Version <String>]
 [-Description <String>] [-TaskSequencePackageId <String>] -DistributionPointServerName <String[]>
 [-Timeout <TimeSpan>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMVhd** cmdlet modifies one or more virtual hard disk (VHD) images that were created through the operating system deployment feature.

## EXAMPLES

### Example 1: Change the distribution point server for a VHD
```
PS C:\>Set-CMVhd -Name "Windows 10 Enterprise" -DistributionPointServerNames "distribution-server.contoso.com"
```

This command changes the distribution point server for the virtual hard disk (VHD) named Windows 10 Enterprise.

### Example 2: Rename a VHD
```
PS C:\>Set-CMVhd -Name "Windows 10 Enterprise"-NewName "User Desktop Image"
```

This command renames the VHD named Windows 10 Enterprise.
In this example, the VHD is renamed to User Desktop Image.

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
Specifies a description for the VHD.

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

### -DistributionPointServerName


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DistributionPointServerNames
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

### -InputObject
Specifies a VHD image.
To obtain a VHD image, use the Get-CMVhd cmdlet.

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
Specifies an array of names of VHD images.

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
Specifies a new name for the VHD image.

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

### -TaskSequencePackageId
Specifies an ID for a task sequence package.

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

### -Timeout


```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies a version for the VHD.
Use any string.

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

### -VhdFilePath


```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath, Path
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdPackageId


```yaml
Type: String
Parameter Sets: SetById
Aliases: Id, PackageId
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

[Get-CMVhd](xref:ConfigurationManager/vlatest/Get-CMVhd.md)

[New-CMVhd](xref:ConfigurationManager/vlatest/New-CMVhd.md)

[Remove-CMVhd](xref:ConfigurationManager/vlatest/Remove-CMVhd.md)


