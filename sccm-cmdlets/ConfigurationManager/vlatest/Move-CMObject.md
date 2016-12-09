---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834206
schema: 2.0.0
ms.assetid: DA3EDFA4-22E2-47AF-8084-BA9A8A7DBD39
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Move-CMObject.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Move-CMObject.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Move-CMObject.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Move-CMObject

## SYNOPSIS
Moves a Configuration Manager object into a different folder.

## SYNTAX

### SearchByObjectMandatory (Default)
```
Move-CMObject -FolderPath <String> -InputObject <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Move-CMObject -FolderPath <String> -ObjectId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Move-CMObject** cmdlet moves a Microsoft System Center Configuration Manager object into a different folder.
Specify the object to move and the destination folder.
Because an object exists in only one folder, the cmdlet does not specify the current folder.

## EXAMPLES

### Example 1: Move an object
```
PS C:\>Move-CMObject -FolderPath "GKP:\Application\TestFolder" -ObjectId "209224563"
```

This command moves the object that has the specified ID to the folder GKP:\Application\TestFolder.

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

### -FolderPath
Specifies a destination folder path, in the following format: AAA:\\\<object type\>\folder\sub-folder\subfolder, where AAA represents the Configuration Manager site code.
For example, a folder that is named LOB Apps for an application node at a sight designated CM1 has the following file path: CM1:\Application\LOB Apps.

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
Specifies an array of Configuration Manager objects to move.

```yaml
Type: IResultObject[]
Parameter Sets: SearchByObjectMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ObjectId
Specifies an array of IDs of objects to move.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: InstanceKey
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

[Lock-CMObject](xref:ConfigurationManager/vlatest/Lock-CMObject.md)

[Unlock-CMObject](xref:ConfigurationManager/vlatest/Unlock-CMObject.md)


