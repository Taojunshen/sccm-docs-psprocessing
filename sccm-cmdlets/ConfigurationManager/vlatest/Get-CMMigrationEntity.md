---
external help file: AdminUI.PS.Migration.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833758
schema: 2.0.0
ms.assetid: D02E7E60-2F2E-4EBE-9EB3-CA8CA9914289
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMMigrationEntity.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMMigrationEntity.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMMigrationEntity

## SYNOPSIS
Gets a migration entity in System Center Configuration Manager.

## SYNTAX

### SearchById (Default)
```
Get-CMMigrationEntity [-Id <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByName
```
Get-CMMigrationEntity [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByOthers
```
Get-CMMigrationEntity [-Type <String>] [-IsActive <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMigrationEntity** cmdlet gets the migration entity in Microsoft System Center Configuration Manager.
A migration entity is an object to be migrated that is of any type that is supported by migration.

## EXAMPLES

### Example 1: Get information about all your migration entities
```
PS C:\>Get-CMMigrationEntity
```

This command returns information about all of your migration entities.

### Example 2: Get information about a specific migration entity
```
PS C:\>Get-CMMigrationEntity -Name "MigrationTest"
```

This command returns information about the migration entity with the name MigrationTest.

### Example 3: Get information about active migration entities
```
PS C:\>Get-CMMigrationEntity -IsActive
```

This command returns information about all of your active migration entities.

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
Specifies an identifier in Configuration Manager.

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

### -IsActive
Specifies that this migration entity is active.

```yaml
Type: String
Parameter Sets: SearchByOthers
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: EntityName
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
Parameter Sets: SearchByOthers
Aliases: 
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

[Get-CMMigrationEntityDependency](xref:ConfigurationManager/vlatest/Get-CMMigrationEntityDependency.md)

[New-CMMigrationJob](xref:ConfigurationManager/vlatest/New-CMMigrationJob.md)


