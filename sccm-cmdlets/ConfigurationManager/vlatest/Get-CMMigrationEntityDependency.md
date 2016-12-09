---
external help file: AdminUI.PS.Migration.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833766
schema: 2.0.0
ms.assetid: E9057BB2-EFBE-45F9-AF07-71933FF4BB4E
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMMigrationEntityDependency.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMMigrationEntityDependency.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMMigrationEntityDependency.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMMigrationEntityDependency

## SYNOPSIS
Gets a dependency for a migration entity in Configuration Manager.

## SYNTAX

### SearchById (Default)
```
Get-CMMigrationEntityDependency [-Id <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByType
```
Get-CMMigrationEntityDependency [-Type <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMigrationEntityDependency** cmdlet gets a migration entity dependency in Microsoft System Center Configuration Manager.
A migration entity dependency is an object upon which another object to be migrated is dependent.

## EXAMPLES

### Example 1: Get information about all migration entity dependencies
```
PS C:\> Get-CMMigrationEntityDependency
```

This command returns information about all your migration entity dependencies.

### Example 2: Get information about a specific migration entity dependency
```
PS C:\> Get-CMMigrationEntityDependency -Id "121989"
```

This command returns information about the migration entity dependency that has the ID 121989.

## PARAMETERS

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

### -Id
Specifies an ID in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: EntityId
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Specifies a type in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByType
Aliases: DependencyType
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


