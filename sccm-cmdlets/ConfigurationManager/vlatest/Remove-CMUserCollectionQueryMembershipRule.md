---
external help file: AdminUI.PS.Collections-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834277
schema: 2.0.0
ms.assetid: EE51B872-1986-4551-B4C0-7E92529AA20C
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMUserCollectionQueryMembershipRule.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMUserCollectionQueryMembershipRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMUserCollectionQueryMembershipRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMUserCollectionQueryMembershipRule

## SYNOPSIS
Removes a query membership rule from one or more user collection in the Configuration Manager hierarchy.

## SYNTAX

### ByValue (Default)
```
Remove-CMUserCollectionQueryMembershipRule -InputObject <IResultObject> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMUserCollectionQueryMembershipRule -CollectionName <String> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMUserCollectionQueryMembershipRule -CollectionId <String> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMUserCollectionQueryMembershipRule** cmdlet removes a query rule from the specified user collections.
You can specify the user collections by using their names, IDs, or by specifying an input object that represents the collections.

For more information about membership rules in Microsoft System Center Configuration Manager, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Remove a rule from a collection by using the collection name
```
PS C:\> Remove-CMUserCollectionQueryMembershipRule -CollectionName "Remote Users" -RuleName "Remote Users by Domain"
```

This command removes the rule named Remote Users by Domain from the collection named Remote Users.

## PARAMETERS

### -CollectionId


```yaml
Type: String
Parameter Sets: ById
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
Parameter Sets: ByName
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
Parameter Sets: ByValue
Aliases: Collection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RuleName


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

[Add-CMUserCollectionQueryMembershipRule](xref:ConfigurationManager/vlatest/Add-CMUserCollectionQueryMembershipRule.md)

[Get-CMUserCollection](xref:ConfigurationManager/vlatest/Get-CMUserCollection.md)

[Get-CMUserCollectionQueryMembershipRule](xref:ConfigurationManager/vlatest/Get-CMUserCollectionQueryMembershipRule.md)


