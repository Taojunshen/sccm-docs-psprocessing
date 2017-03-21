---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834293
schema: 2.0.0
ms.assetid: AC1A56D7-0868-4302-B93D-423F21BFD2E0
updated_at: 3/21/2017 10:58 PM
ms.date: 3/21/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Rename-CMCategory.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Rename-CMCategory.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/19b0a2cde22ac11c02081e258229d03c5d581339/sccm-cmdlets/ConfigurationManager/vlatest/Rename-CMCategory.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Rename-CMCategory

## SYNOPSIS
Renames a category.

## SYNTAX

### RenameCategoryByValue (Default)
```
Rename-CMCategory -InputObject <IResultObject> -NewName <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RenameCategoryByName
```
Rename-CMCategory -Name <String> -NewName <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Rename-CMCategory** cmdlet renames a category instance.

## EXAMPLES

### Example 1: Rename a category by getting a category object
```
PS ABC:\> $Category = Get-CMCategory -Name "Category01" -CategoryType BaselineCategories
PS ABC:\> Rename-CMCategory -InputObject $Category -NewName "NewCategory01"
```

The first command gets the category object named Category01 of the type BaselineCategories and stores the object in the $Category variable.

The second command renames the category stored in $Category to NewCategory01.

### Example 2: Rename a category by its name and type
```
PS ABC:\> Rename-CMCategory -Name "Category02" -NewName "NewCategory02" -CategoryType BaselineCategories
```

This command renames the category named Category02 of the type BaseineCategories to NewCategory02.

### Example 3: Rename a category by passing a category object through the pipeline
```
PS ABC:\> Get-CMCategory -Name "Category03" -CategoryType BaselineCategories | Rename-CMCategory -NewName "NewCategory03"
```

This command gets the category object named Category03 of the type BaselineCategories and uses the pipeline operator to pass the object to **Rename-CMCategory**, which renames the category to NewCategory03.

## PARAMETERS

### -CategoryType
Specifies a category type.
Valid values are:

- AppCategories
- BaselineCategories
- CatalogCategories
- DriverCategories
- UserCategories

```yaml
Type: CategoryType
Parameter Sets: ByName
Aliases:
Accepted values: AppCategories, BaselineCategories, CatalogCategories, DriverCategories, UserCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

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

### -InputObject
Specifies a category instance object.
To obtain a category instance object, use the [Get-CMCategory](./Get-CMCategory.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RenameCategoryByValue
Aliases: Category

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a category instance.

```yaml
Type: String
Parameter Sets: RenameCategoryByName
Aliases: LocalizedCategoryInstanceName, CategoryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the category instance.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

[New-CMCategory](xref:ConfigurationManager/vlatest/New-CMCategory.md)

[Get-CMCategory](xref:ConfigurationManager/vlatest/Get-CMCategory.md)

[Remove-CMCategory](xref:ConfigurationManager/vlatest/Remove-CMCategory.md)
