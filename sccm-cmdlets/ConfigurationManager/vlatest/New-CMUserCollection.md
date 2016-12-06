---
external help file: AdminUI.PS.Collections-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833807
schema: 2.0.0
ms.assetid: 1543ACE3-2915-4522-9A1D-04902FB557DF
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMUserCollection.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/New-CMUserCollection.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# New-CMUserCollection

## SYNOPSIS
Creates a collection for users and adds the collection to the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
New-CMUserCollection [-Comment <String>] -LimitingCollectionName <String> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
New-CMUserCollection [-Comment <String>] -InputObject <IResultObject> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
New-CMUserCollection [-Comment <String>] -LimitingCollectionId <String> -Name <String>
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMUserCollection** cmdlet creates a collection based on a specific limiting collection.
The limiting collection determines which users can be a member of the user collection that you create.
For example, when you use the All Users collection as the limiting collection, the new collection can include any user in the Microsoft System Center Configuration Manager hierarchy.
You specify the limiting collection by providing its name or ID.

Users are added to the collection by membership rules.
To add members to the user collection use one of the following membership rule cmdlets: 

- Add-CMDeviceCollectionQueryMembershipRule
- Add-CMUserCollectionDirectMembershipRule
- Add-CMUserCollectionExcludeMembershipRule
- Add-CMUserCollectionIncludeMembershipRule

Collections represent logical groupings of resources, such as users and devices.
For more information about Configuration Manager collections, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

### Example 1: Create a user collection
```
PS C:\>New-CMUserCollection -Name "Sales" -LimitingCollectionName "All Users"
```

This command creates a collection for all users in the Sales department.
Specifying All Users for the *LimitingCollectionName* parameter indicates that the new collection can include any user in the Configuration Manager hierarchy.

## PARAMETERS

### -Comment


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

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: LimitingCollection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LimitingCollectionId


```yaml
Type: String
Parameter Sets: ById
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitingCollectionName


```yaml
Type: String
Parameter Sets: ByName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name


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

### -RefreshSchedule


```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshType


```yaml
Type: CollectionRefreshType
Parameter Sets: (All)
Aliases: 
Accepted values: None, Manual, Periodic, Continuous, Both
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

[Add-CMDeviceCollectionQueryMembershipRule](xref:ConfigurationManager/vlatest/Add-CMDeviceCollectionQueryMembershipRule.md)

[Add-CMUserCollectionDirectMembershipRule](xref:ConfigurationManager/vlatest/Add-CMUserCollectionDirectMembershipRule.md)

[Add-CMUserCollectionExcludeMembershipRule](xref:ConfigurationManager/vlatest/Add-CMUserCollectionExcludeMembershipRule.md)

[Add-CMUserCollectionIncludeMembershipRule](xref:ConfigurationManager/vlatest/Add-CMUserCollectionIncludeMembershipRule.md)

[Get-CMUserCollection](xref:ConfigurationManager/vlatest/Get-CMUserCollection.md)


