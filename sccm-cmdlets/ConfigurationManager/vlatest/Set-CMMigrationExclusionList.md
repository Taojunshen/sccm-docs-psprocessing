---
external help file: AdminUI.PS.Migration.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833926
schema: 2.0.0
ms.assetid: B4AFB52F-322C-446C-BE3D-6CB67373D957
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMMigrationExclusionList.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMMigrationExclusionList.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMMigrationExclusionList.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMMigrationExclusionList

## SYNOPSIS
Edits the global exclusion list for migration jobs.

## SYNTAX

```
Set-CMMigrationExclusionList -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMMigrationExclusionList** cmdlet edits the global exclusion list for migration jobs in Microsoft System Center Configuration Manager.

For a collection-based migration, you specify one or more collections to migrate.
For each collection that you specify, the migration job automatically selects all related objects for migration.
Objects on the exclusion list are available for migration, but System Center Configuration Manager does not automatically include these objects when you create a new collection-based migration job.

## EXAMPLES

### Example 1: Specify a migration exclusion list
```
PS C:\> Set-CMMigrationExclusionList -Name "ContosoUsersWest01"
```

This command adds the objects in the array ContosoUsersWest01 to the migration exclusion list.

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

### -Name
Specifies an array of objects that you exclude by default from collection-based migration jobs.

```yaml
Type: String
Parameter Sets: (All)
Aliases: EntityName
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

[Clear-CMMigrationData](xref:ConfigurationManager/vlatest/Clear-CMMigrationData.md)

[Set-CMMigrationSource](xref:ConfigurationManager/vlatest/Set-CMMigrationSource.md)


