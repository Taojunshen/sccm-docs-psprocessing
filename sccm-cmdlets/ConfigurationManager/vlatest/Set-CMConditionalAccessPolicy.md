---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833760
schema: 2.0.0
ms.assetid: 433C709E-FBB0-449F-A835-9ED3613D2581
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMConditionalAccessPolicy.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMConditionalAccessPolicy.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMConditionalAccessPolicy

## SYNOPSIS
Sets a conditional access policy.

## SYNTAX

```
Set-CMConditionalAccessPolicy [-AddExcludedCollection <IResultObject[]>] [-AddExcludedCollectionId <String[]>]
 [-AddExcludedCollectionName <String[]>] [-AddTargetedCollection <IResultObject[]>]
 [-AddTargetedCollectionId <String[]>] [-AddTargetedCollectionName <String[]>] [-ClearExcludedCollection]
 [-ClearTargetedCollection] [-DefaultRuleOverride <Boolean>] [-InputObject] <IResultObject>
 [-NotificationText <String>] [-PassThru] [-RemoveExcludedCollection <IResultObject[]>]
 [-RemoveExcludedCollectionId <String[]>] [-RemoveExcludedCollectionName <String[]>]
 [-RemoveTargetedCollection <IResultObject[]>] [-RemoveTargetedCollectionId <String[]>]
 [-RemoveTargetedCollectionName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMConditionalAccessPolicy** cmdlet updates the settings of a conditional access policy.

## EXAMPLES

### Example 1: Set a conditional access policy to add collections
```
PS C:\> Get-CMConditionalAccessPolicy | Set-CMConditionalAccessPolicy -NotificationText "Test text 01" -AddExcludedCollectionID EC300016 -AddTargetedCollectionID TC300018
```

This command gets the conditional access policy object and uses the pipeline operator to pass the object to **Set-CMConditionalAccessPolicy**, which adds an excluded collection with the ID of EC300016 and a targeted collection with the id of TC300018.

### Example 2: Set a conditional access policy to remove collections
```
PS C:\> Get-CMConditionalAccessPolicy | Set-CMConditionalAccessPolicy -NotificationText "Text text 02" -RemoveExcludedCollectionID EC300014 -RemoveTargetedCollectionName "All Users"
```

This command gets the conditional access policy object and uses the pipeline operator to pass the object to **Set-CMConditionalAccessPolicy**, which removes the excluded collection with the ID of EC300014, and the targeted collection with the name of All Users.

## PARAMETERS

### -AddExcludedCollection
Adds an array of user collection objects to a conditional access policy.
To obtain a user collection object, use the Get-CMCollection cmdlet.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddExcludedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddExcludedCollectionId
Adds an array of user collection IDs to a conditional access policy.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddExcludedCollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddExcludedCollectionName
Adds an array of user collection names to a conditional access policy.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddExcludedCollectionNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddTargetedCollection
Adds an array of user collection objects to a conditional access policy.
To obtain a user collection object, use the Get-CMCollection cmdlet.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddTargetedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddTargetedCollectionId
Adds an array of user collection IDs to a conditional access policy.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddTargetedCollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddTargetedCollectionName
Adds an array of user collection names to a conditional access policy.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddTargetedCollectionNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearExcludedCollection
Removes all excluded collections from the conditional access policy.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearExcludedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearTargetedCollection
Removes all targeted collections from a conditional access policy.

NOTE:  You must specify at least one targeted collection for a conditional access policy.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearTargetedCollections

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

### -DefaultRuleOverride
Specifies that the devices that are enrolled in Microsoft Intune and compliant with the compliance policies are allowed to access Exchange.
This rule overrides the default Exchange access rule, which means that even if you set the default rule to quarantine or block access, enrolled and compliant devices will still be able to access Exchange.

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
Specifies a conditional access policy object.
To obtain a conditional access policy object, use the Get-CMConditionalAccessPolicy cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NotificationText
Specifies the text of the email that Exchange sends to users when their device is blocked.

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

### -RemoveExcludedCollection
Removes an array of user collection objects from a conditional access policy.
To obtain a user collection object, use the Get-CMCollection cmdlet.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveExcludedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveExcludedCollectionId
Removes an array of user collection IDs from a conditional access policy.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveExcludedCollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveExcludedCollectionName
Removes an array of user collection names from a conditional access policy.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveExcludedCollectionNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveTargetedCollection
Removes an array of user collection objects from a conditional access policy.
To obtain a user collection object, use the Get-CMCollection cmdlet.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveTargetedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveTargetedCollectionId
Removes an array of user collection IDs from a conditional access policy.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveTargetedCollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveTargetedCollectionName
Removes an array of user collection names from a conditional access policy.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveTargetedCollectionNames

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

[Get-CMCollection](xref:ConfigurationManager/vlatest/Get-CMCollection.md)

[Get-CMConditionalAccessPolicy](xref:ConfigurationManager/vlatest/Get-CMConditionalAccessPolicy.md)

[New-CMConditionalAccessPolicy](xref:ConfigurationManager/vlatest/New-CMConditionalAccessPolicy.md)

[Remove-CMConditionalAccessPolicy](xref:ConfigurationManager/vlatest/Remove-CMConditionalAccessPolicy.md)

