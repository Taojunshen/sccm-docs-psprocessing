---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833762
schema: 2.0.0
ms.assetid: 3C642D15-E6BF-4416-99F6-98BDBC2A5D36
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMStateMigrationPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMStateMigrationPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Add-CMStateMigrationPoint

## SYNOPSIS
Adds a state migration point in Configuration Manager.

## SYNTAX

### ByValue (Default)
```
Add-CMStateMigrationPoint -StorageFolder <StorageDirectoryData[]> [-DeleteImmediately]
 [-TimeDeleteAfter <Int32>] [-TimeUnit <IntervalType>] [-EnableRestoreOnlyMode <Boolean>]
 [-AllowFallbackSourceLocationForContent <Boolean>] [-BoundaryGroupName <String[]>]
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Add-CMStateMigrationPoint [-SiteSystemServerName] <String> [-SiteCode <String>]
 -StorageFolder <StorageDirectoryData[]> [-DeleteImmediately] [-TimeDeleteAfter <Int32>]
 [-TimeUnit <IntervalType>] [-EnableRestoreOnlyMode <Boolean>]
 [-AllowFallbackSourceLocationForContent <Boolean>] [-BoundaryGroupName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMStateMigrationPoint** cmdlet adds a state migration point in Microsoft System Center Configuration Manager.
A state migration point is a site system role that manages data transfer from client computers during an operating system installation process.

## EXAMPLES

### Example 1: Add a state migration point
```
PS C:\>$s1 = New-CMStoragefolder -StorageFolderName "C:\Sto-1" -MaximumClientNumber 100 -MinimumFreeSpace 100 -SpaceUnit Megabyte
PS C:\> $s2 = New-CMStoragefolder -StorageFolderName "D:\Sto-2" -MaximumClientNumber 100 -MinimumFreeSpace 10 -SpaceUnit Gigabyte
PS C:\> Add-CMStateMigrationPoint -SiteSystemServerName "Contoso-Migration.Contoso.com" -SiteCode "CM2" -StorageFolders $s1,$s2 -DeleteImmediately -EnableRestoreOnlyMode $False -AllowFallbackSourceLocationForContent $False -BoundaryGroupName "CMC"
```

The first command creates a storage folder on the C: drive that has a maximum number of clients setting and a minimum free space setting.
The command stores the result in the $s1 variable.

The second command creates a storage folder on the D: drive that has a maximum number of clients setting and a minimum free space setting.
The command stores the result in the $s2 variable.

The third command adds a state migration point.

## PARAMETERS

### -AllowFallbackSourceLocationForContent


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

### -BoundaryGroupName


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -DeleteImmediately


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

### -EnableRestoreOnlyMode


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
Parameter Sets: ByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode


```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName


```yaml
Type: String
Parameter Sets: ByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageFolder


```yaml
Type: StorageDirectoryData[]
Parameter Sets: (All)
Aliases: StorageFolders

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeDeleteAfter


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeUnit


```yaml
Type: IntervalType
Parameter Sets: (All)
Aliases: 
Accepted values: Hours, Days

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

[Get-CMStateMigrationPoint](xref:ConfigurationManager/vlatest/Get-CMStateMigrationPoint.md)

[Remove-CMStateMigrationPoint](xref:ConfigurationManager/vlatest/Remove-CMStateMigrationPoint.md)

[Set-CMStateMigrationPoint](xref:ConfigurationManager/vlatest/Set-CMStateMigrationPoint.md)

[Get-CMBoundaryGroup](xref:ConfigurationManager/vlatest/Get-CMBoundaryGroup.md)


