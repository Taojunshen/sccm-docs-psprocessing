---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833621
schema: 2.0.0
ms.assetid: 388164F7-DE65-45A1-B3D9-1D0BB6B7AEBD
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMDeviceCollectionVariable.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMDeviceCollectionVariable.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/New-CMDeviceCollectionVariable.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMDeviceCollectionVariable

## SYNOPSIS
Creates a device collection variable.

## SYNTAX

### NewByValueMandatory (Default)
```
New-CMDeviceCollectionVariable -InputObject <IResultObject> -VariableName <String> [-Value <String>]
 [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewByIdMandatory
```
New-CMDeviceCollectionVariable -CollectionId <String> -VariableName <String> [-Value <String>]
 [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewByNameMandatory
```
New-CMDeviceCollectionVariable -CollectionName <String> -VariableName <String> [-Value <String>]
 [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMDeviceCollectionVariable** cmdlet creates a device collection variable.
You can use a device collection variable to define custom task sequence variables and their associated values to be used by the resources in a collection.
Task sequence variables are a set of name and value pairs that provide a mechanism to configure and customize the steps of a task sequence when the task sequence is deployed to a specific collection.

## EXAMPLES

### Example 1: Create a device collection variable
```
PS C:\> $Collection = Get-CMCollection -Name "Device"
PS C:\> New-CMDeviceCollectionVariable -Collection $Collection -VariableName "testTS" -Value "test001"
```

The first command gets the device collection object named Device and stores the object in the $Collection variable.

The second command creates a collection variable named testTS with the value test001 for the collection object stored in $Collection.

## PARAMETERS

### -CollectionId
Specifies the ID of a device collection.

```yaml
Type: String
Parameter Sets: NewByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a device collection.

```yaml
Type: String
Parameter Sets: NewByNameMandatory
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
Specifies a device collection object.
To obtain a collection object, use the [Get-CMCollection](./Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: NewByValueMandatory
Aliases: Collection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsMask
Indicates whether the collection variable value displays in the Configuration Manager console.

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

### -Value
Specifies a value for the collection variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VariableValue
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VariableName
Specifies a name for the collection variable.

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

[Planning a Task Sequence Strategy in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=260806)

[Get-CMCollection](xref:ConfigurationManager/vlatest/Get-CMCollection.md)

[Get-CMDeviceCollectionVariable](xref:ConfigurationManager/vlatest/Get-CMDeviceCollectionVariable.md)

[Set-CMDeviceCollectionVariable](xref:ConfigurationManager/vlatest/Set-CMDeviceCollectionVariable.md)

[Remove-CMDeviceCollectionVariable](xref:ConfigurationManager/vlatest/Remove-CMDeviceCollectionVariable.md)

[Get-CMUserCollection](xref:ConfigurationManager/vlatest/Get-CMUserCollection.md)


