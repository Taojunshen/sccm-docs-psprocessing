---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833968
schema: 2.0.0
ms.assetid: F2F2FB26-C763-4B52-A354-214E27F7C59F
updated_at: 12/6/2016 11:13 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMCollection.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMCollection.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/d1c6f0eeb340f832b2254d78bbd1bc9245dc24fc/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMCollection.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMCollection

## SYNOPSIS
Removes a collection.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMCollection -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMCollection -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMCollection -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMCollection** cmdlet removes a collection from Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Remove a specified collection
```
PS C:\> Remove-CMCollection -Name "testUser" -Force
```

This command removes the collection named testUser.
Specifying the *Force* parameter means that the user is not prompted for confirmation before the collection is removed.

### Example 2: Get a collection object and remove it
```
PS C:\> Get-CMCollection -Name "testUser" | Remove-CMCollection -Force
```

This command gets the collection object named testUser and uses the pipeline operator to pass the object to **Remove-CMCollection**, which removes the collection.
Specifying the *Force* parameter means that the user is not prompted for confirmation before the collection is removed.

## PARAMETERS

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
Specifies a collection ID.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CollectionId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a collection object.
To obtain a collection object, use the [Get-CMCollection](./Get-CMCollection.md) cmdlet.

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

[Export-CMCollection](xref:ConfigurationManager/vlatest/Export-CMCollection.md)

[Import-CMCollection](xref:ConfigurationManager/vlatest/Import-CMCollection.md)

[New-CMCollection](xref:ConfigurationManager/vlatest/New-CMCollection.md)

[Set-CMCollection](xref:ConfigurationManager/vlatest/Set-CMCollection.md)


