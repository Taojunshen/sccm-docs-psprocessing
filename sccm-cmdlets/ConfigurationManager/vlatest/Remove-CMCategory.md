---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833941
schema: 2.0.0
ms.assetid: 1A28C432-B26B-43EE-8C1D-856F16DDB25E
updated_at: 12/7/2016 5:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMCategory.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/f3e8fe7234dce2881d15465fb1eb6990d1f03567/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMCategory.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMCategory

## SYNOPSIS
Removes a configuration category in Configuration Manager.

## SYNTAX

### ByValue (Default)
```
Remove-CMCategory -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMCategory -Name <String[]> [-Force] [-CategoryType <CategoryType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMCategory -Id <String[]> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByCategory
```
Remove-CMCategory [-Force] -CategoryType <CategoryType> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMCategory** cmdlet removes a configuration category in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Remove a configuration category
```
PS C:\>Remove-CMCategory -CategoryType "DriverCategories" -Force -Name "NewLaptopDriverSet"
```

This command removes the category named NewLaptopDriverSet from DriversCategories without prompting you for confirmation.

## PARAMETERS

### -CategoryType
Specifies a category type.
Valid values are: 

- UserCategories
- BaselineCategories
- DriverCategories
- AppCategories
- GlobalCondition
- CatalogCategories

```yaml
Type: CategoryType
Parameter Sets: ByName
Aliases: 
Accepted values: UserCategories, BaselineCategories, DriverCategories, AppCategories, GlobalCondition, CatalogCategories
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: CategoryType
Parameter Sets: ByCategory
Aliases: 
Accepted values: UserCategories, BaselineCategories, DriverCategories, AppCategories, GlobalCondition, CatalogCategories
Required: True
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

### -Id
Specifies an array of IDs of configuration categories.

```yaml
Type: String[]
Parameter Sets: ById
Aliases: CategoryInstanceUniqueid, CategoryId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Category
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration categories.

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: LocalizedCategoryInstanceName, CategoryName
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

[Get-CMCategory](xref:ConfigurationManager/vlatest/Get-CMCategory.md)

[New-CMCategory](xref:ConfigurationManager/vlatest/New-CMCategory.md)
