---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834263
schema: 2.0.0
ms.assetid: 9C9C7C89-BEC9-4B9D-838B-250771C23C44
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMConditionalAccessPolicy.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMConditionalAccessPolicy.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMConditionalAccessPolicy

## SYNOPSIS
Gets a conditional access policy.

## SYNTAX

### ByValue (Default)
```
Get-CMConditionalAccessPolicy [-TargetedCollection <IResultObject[]>] [-ExcludedCollection <IResultObject[]>]
 [-DefaultRuleOverride <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
Get-CMConditionalAccessPolicy [-TargetedCollectionName <String[]>] [-ExcludedCollectionName <String[]>]
 [-DefaultRuleOverride <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMConditionalAccessPolicy [-TargetedCollectionId <String[]>] [-ExcludedCollectionId <String[]>]
 [-DefaultRuleOverride <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConditionalAccessPolicy** cmdlet gets a conditional access policy.

## EXAMPLES

### Example 1: Get a conditional access policy by name
```
PS C:\> Get-CMConditionalAccessPolicy -TargetedCollection (Get-CMCollection -Name "All Users")
```

This command gets the conditional access policy for the targeted collection named All Users.

### Example 2: Get a conditional access policy by ID
```
PS C:\> Get-CMConditionalAccessPolicy -TargetedCollectionID SMS00002
```

This command gets the conditional access policy for the target collection with the ID of SMS00002.

## PARAMETERS

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

### -ExcludedCollection
Specifies an array of user collection objects.
To obtain a user collection object, use the Get-CMCollection cmdlet.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: ExecludedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedCollectionId
Specifies an array of user collection IDs.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: String[]
Parameter Sets: ById
Aliases: ExecludedCollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludedCollectionName
Specifies an array of user collection names.

Members of these collections do not have to enroll their devices in Microsoft Intune, or be compliant with any deployed compliance policies in order to access Exchange, as long as the default Exchange rules allow access.

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: ExecludedCollectionNames

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

### -TargetedCollection
Specifies an array of user collection objects.
To obtain a user collection object, use the Get-CMCollection cmdlet.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: TargetedCollections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetedCollectionId
Specifies an array of user collection IDs.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: ById
Aliases: TargetedCollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetedCollectionName
Specifies an array of user collection names.

Members of these collections must enroll their devices in Microsoft Intune and be compliant with any deployed compliance policies in order to access Exchange.

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: TargetedCollectionNames

Required: False
Position: Named
Default value: None
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

[New-CMConditionalAccessPolicy](xref:ConfigurationManager/vlatest/New-CMConditionalAccessPolicy.md)

[Remove-CMConditionalAccessPolicy](xref:ConfigurationManager/vlatest/Remove-CMConditionalAccessPolicy.md)

[Set-CMConditionalAccessPolicy](xref:ConfigurationManager/vlatest/Set-CMConditionalAccessPolicy.md)


