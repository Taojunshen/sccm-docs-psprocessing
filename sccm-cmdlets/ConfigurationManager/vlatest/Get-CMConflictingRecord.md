---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834286
schema: 2.0.0
ms.assetid: 5B0C478D-55DA-4A57-9176-47B810CEA35B
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMConflictingRecord.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMConflictingRecord.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMConflictingRecord.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMConflictingRecord

## SYNOPSIS
Gets conflicting Configuration Manager record objects.

## SYNTAX

### SearchByName (Default)
```
Get-CMConflictingRecord [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMConflictingRecord -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConflictingRecord** cmdlet gets one or more conflicting Microsoft System Center Configuration Manager record objects.

When Configuration Manager recognizes a new client, it uses hardware information to check whether it previously created a record for that computer.
For example, you might have reinstalled the operating system.
The previous client record still exists with the same hardware information.
If you manually resolve conflicts, you have the option to merge the new record with the existing record, create a new record, or create a record as a blocked record.
You can also configure Configuration Manager to resolve conflicts automatically.

You can use this cmdlet with the [Block-CMConflictingRecord](./Block-CMConflictingRecord.md) cmdlet or the [Merge-CMConflictingRecord](./Merge-CMConflictingRecord.md) cmdlet.
You can get all the outstanding conflicts for Configuration Manager or specify a conflict by name or by ID.

## EXAMPLES

### Example 1: Get all conflicting records
```
PS C:\> Get-CMConflictingRecord
```

This command gets all the unresolved conflicts for Configuration Manager.

### Example 2: Get a named conflicting record
```
PS C:\> Get-CMConflictingRecord -Name "CR07"
```

This command gets a conflict named CR07.

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
Specifies an ID for the conflicting records.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: Smsid
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the conflicting records.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: AgentName
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

[Block-CMConflictingRecord](xref:ConfigurationManager/vlatest/Block-CMConflictingRecord.md)

[Merge-CMConflictingRecord](xref:ConfigurationManager/vlatest/Merge-CMConflictingRecord.md)
