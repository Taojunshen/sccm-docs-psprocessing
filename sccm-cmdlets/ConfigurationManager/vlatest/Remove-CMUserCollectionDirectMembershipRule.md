---
external help file: AdminUI.PS.Collections-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834264
schema: 2.0.0
ms.assetid: AB985DAA-B7DE-4FC1-8429-20398128AA1E
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMUserCollectionDirectMembershipRule.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMUserCollectionDirectMembershipRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMUserCollectionDirectMembershipRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMUserCollectionDirectMembershipRule

## SYNOPSIS
Removes a direct membership rule from one or more user collections in the Configuration Manager hierarchy.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMUserCollectionDirectMembershipRule -CollectionName <String> -ResourceName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMUserCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMUserCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMUserCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMUserCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMUserCollectionDirectMembershipRule -CollectionId <String> -ResourceName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMUserCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMUserCollectionDirectMembershipRule** cmdlet removes a direct rule from the specified collections.
You can specify the collections by using their names, IDs, or by specifying an object that represents the collections.

For more information about collection rules in Microsoft System Center Configuration Manager, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Remove all direct membership rules from a user collection
```
PS C:\> Remove-CMUserCollectionDirectMembershipRule -CollectionID "CM0001A" -ResourceId "12733"
```

This command removes all the direct membership rules of the user collection that has the ID CM0001A.

## PARAMETERS

### -CollectionId


```yaml
Type: String
Parameter Sets: ByIdAndValue, ByIdAndId, ByIdAndName
Aliases: Id
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName


```yaml
Type: String
Parameter Sets: ByNameAndName, ByNameAndValue, ByNameAndId
Aliases: Name
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

### -Force


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
Parameter Sets: ByValueAndValue, ByValueAndId, ByValueAndName
Aliases: Collection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Resource


```yaml
Type: IResultObject
Parameter Sets: ByNameAndValue, ByIdAndValue, ByValueAndValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId


```yaml
Type: String
Parameter Sets: ByNameAndId, ByIdAndId, ByValueAndId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName


```yaml
Type: String
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
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

[Add-CMUserCollectionDirectMembershipRule](xref:ConfigurationManager/vlatest/Add-CMUserCollectionDirectMembershipRule.md)

[Get-CMUserCollection](xref:ConfigurationManager/vlatest/Get-CMUserCollection.md)

[Get-CMUserCollectionDirectMembershipRule](xref:ConfigurationManager/vlatest/Get-CMUserCollectionDirectMembershipRule.md)

[Remove-CMUserCollectionExcludeMembershipRule](xref:ConfigurationManager/vlatest/Remove-CMUserCollectionExcludeMembershipRule.md)

[Remove-CMUserCollectionIncludeMembershipRule](xref:ConfigurationManager/vlatest/Remove-CMUserCollectionIncludeMembershipRule.md)

[Remove-CMUserCollectionQueryMembershipRule](xref:ConfigurationManager/vlatest/Remove-CMUserCollectionQueryMembershipRule.md)


