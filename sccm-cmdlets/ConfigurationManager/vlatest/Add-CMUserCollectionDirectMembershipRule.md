---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833768
schema: 2.0.0
ms.assetid: B0E1925F-4D8D-4BFE-9DE7-8C76F10A8383
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMUserCollectionDirectMembershipRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMUserCollectionDirectMembershipRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Add-CMUserCollectionDirectMembershipRule

## SYNOPSIS
Adds a direct membership rule to one or more Configuration Manager user collections.

## SYNTAX

### ByCollectionValueAndResourceValue (Default)
```
Add-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdAndResourceId
```
Add-CMUserCollectionDirectMembershipRule -CollectionId <String> -ResourceId <Int32> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdAndResourceValue
```
Add-CMUserCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameAndResourceValue
```
Add-CMUserCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameAndResourceId
```
Add-CMUserCollectionDirectMembershipRule -CollectionName <String> -ResourceId <Int32> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionValueAndResourceId
```
Add-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <Int32> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMUserCollectionDirectMembershipRule** cmdlet adds a rule that adds a specific resource to the user collections.
You can specify the user collections by using their names, IDs, or by specifying an object that represents the collections.

A direct rule lets you explicitly choose the members of the user collection.
For more information on collection rules in Microsoft System Center Configuration Manager, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Add a direct membership rule to a user collection
```
PS C:\>Add-CMUserCollectionDirectMembershipRule -CollectionName "All Mobile Devices" -ResourceId "Res_94412512"
```

This command adds a direct membership rule that has the ID Res_94412512 to the Configuration Manager user collection named All Mobile Devices.

## PARAMETERS

### -CollectionId
Specifies the ID of the user collection where the rule is applied.

```yaml
Type: String
Parameter Sets: ByCollectionIdAndResourceId, ByCollectionIdAndResourceValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a user collection where the rule is applied.

```yaml
Type: String
Parameter Sets: ByCollectionNameAndResourceValue, ByCollectionNameAndResourceId
Aliases: 

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
Parameter Sets: ByCollectionValueAndResourceValue, ByCollectionValueAndResourceId
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru


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

### -Resource
Specifies the type of the resource that the cmdlet adds to the user collections.

```yaml
Type: IResultObject
Parameter Sets: ByCollectionValueAndResourceValue, ByCollectionIdAndResourceValue, ByCollectionNameAndResourceValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceId
Specifies the ID of a resource that the cmdlet adds to the user collections.

```yaml
Type: Int32
Parameter Sets: ByCollectionIdAndResourceId, ByCollectionNameAndResourceId, ByCollectionValueAndResourceId
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

[Get-CMUserCollection](xref:ConfigurationManager/vlatest/Get-CMUserCollection.md)

[Get-CMUserCollectionDirectMembershipRule](xref:ConfigurationManager/vlatest/Get-CMUserCollectionDirectMembershipRule.md)

[Remove-CMUserCollectionDirectMembershipRule](xref:ConfigurationManager/vlatest/Remove-CMUserCollectionDirectMembershipRule.md)


