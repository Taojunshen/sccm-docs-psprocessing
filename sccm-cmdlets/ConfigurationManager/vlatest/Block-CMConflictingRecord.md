---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833823
schema: 2.0.0
ms.assetid: 28AA7E3C-EC13-4CE4-851D-7F6C765E48F9
updated_at: 12/7/2016 8:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Block-CMConflictingRecord.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/282d10ca7ed3ddf1432b06182fee46c9e52563a4/sccm-cmdlets/ConfigurationManager/vlatest/Block-CMConflictingRecord.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Block-CMConflictingRecord

## SYNOPSIS
Creates a blocked Configuration Manager record for client that has a conflicting record.

## SYNTAX

### SearchByValueMandatory (Default)
```
Block-CMConflictingRecord -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Block-CMConflictingRecord -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Block-CMConflictingRecord -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Block-CMConflictingRecord** cmdlet blocks a record for a client that has a conflicting record in Microsoft System Center Configuration Manager.

When Configuration Manager recognizes a new client, it uses hardware information to check whether it previously created a record for that computer.
For example, you might have reinstalled the operating system.
The previous client record still exists with the same hardware information.
If you manually resolve conflicts, you have the option to merge the new record with the existing record, create a new record, or create a record as a blocked record.
You can also configure Configuration Manager to resolve conflicts automatically.

You can specify a conflict by using a name or ID or you can use the [Get-CMConflictingRecord](./Get-CMConflictingRecord.md) cmdlet to obtain one.

## EXAMPLES

### Example 1: Create a blocked record for a named conflict
```
PS C:\>Block-CMConflictingRecord -Name "CR07"
```

This command creates a blocked record for the conflict named CR07.

### Example 2: Create a blocked record by using a variable
```
PS C:\>$CMCR = Get-CMConflictingRecord -Name "CR07"
PS C:\> Block-CMConflictingRecord -ConflictingRecord $CMCR
```

The first command gets a conflicting record named CR07 and saves it in the $CMCR variable.

The second command creates a blocked record for the conflict in $CMCR.

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

### -Id
Specifies an ID for the conflicting records.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: SmsId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ConflictingRecord
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for the conflicting records.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: AgentName
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

[Get-CMConflictingRecord](xref:ConfigurationManager/vlatest/Get-CMConflictingRecord.md)

[Merge-CMConflictingRecord](xref:ConfigurationManager/vlatest/Merge-CMConflictingRecord.md)
