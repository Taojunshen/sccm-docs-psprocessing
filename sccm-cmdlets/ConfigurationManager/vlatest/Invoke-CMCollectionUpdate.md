---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834113
schema: 2.0.0
ms.assetid: 789484FC-87E4-4EA3-946A-57659F622D05
updated_at: 3/14/2017 5:56 PM
ms.date: 3/14/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMCollectionUpdate.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMCollectionUpdate.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/ccf61168e86d4120cdc26f0ffd9b7560e92d36b5/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMCollectionUpdate.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Invoke-CMCollectionUpdate

## SYNOPSIS
Updates the membership of a collection.

## SYNTAX

### SearchByValueMandatory (Default)
```
Invoke-CMCollectionUpdate -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMCollectionUpdate -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMCollectionUpdate -CollectionId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMCollectionUpdate** cmdlet updates the membership of a collection.

## EXAMPLES

### Example 1: Update the membership of a collection using the pipeline
```
PS C:\> Get-CMCollection -Id MP500014 | Invoke-CMCollectionUpdate
```

This command gets the collection object with the ID of MP500014 and uses the pipeline operator to pass the object to **Invoke-CMCollectionUpdate**, which updates the membership of the collection.

### Example 2: Update the membership of a collection by name
```
PS C:\> Invoke-CMCollectionUpdate -Name "UserCol1"
```

This command updates the membership of the collection named UserCol1.

## PARAMETERS

### -CollectionId
Specifies the ID of a collection.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
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
Specifies a collection object.
To obtain a collection object, use the Get-CMCollection, Get-CMDeviceCollection, or Get-CMUserCollection cmdlets.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a collection.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

[Get-CMCollection](xref:ConfigurationManager/vlatest/Get-CMCollection.md)

[Get-CMDeviceCollection](xref:ConfigurationManager/vlatest/Get-CMDeviceCollection.md)

[Get-CMUserCollection](xref:ConfigurationManager/vlatest/Get-CMUserCollection.md)


