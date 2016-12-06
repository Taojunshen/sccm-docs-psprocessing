---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834111
schema: 2.0.0
ms.assetid: DB992DC8-0D2B-4704-AA14-0CD157FFA1C2
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMStatusMessageQuery.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMStatusMessageQuery.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMStatusMessageQuery

## SYNOPSIS
Changes settings or security scope or deletes messages for a Configuration Manager status message query.

## SYNTAX

### SetStatusMessageQueryByObjectMandatory (Default)
```
Set-CMStatusMessageQuery -InputObject <IResultObject> [-NewName <String>] [-Expression <String>]
 [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DeleteMessageByIdMandatory
```
Set-CMStatusMessageQuery -Id <String> [-DeleteMessage] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStatusMessageQueryByIdMandatory
```
Set-CMStatusMessageQuery -Id <String> [-NewName <String>] [-Expression <String>] [-Comment <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStatusMessageQueryByNameMandatory
```
Set-CMStatusMessageQuery -Name <String> [-NewName <String>] [-Expression <String>] [-Comment <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteMessageByNameMandatory
```
Set-CMStatusMessageQuery -Name <String> [-DeleteMessage] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteMessageByObjectMandatory
```
Set-CMStatusMessageQuery -InputObject <IResultObject> [-DeleteMessage] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMStatusMessageQuery** cmdlet changes settings for a Microsoft System Center Configuration Manager status message query.
Status message queries return status messages from a System Center Configuration Manager site database.
You can modify a comment, a Windows Management Infrastructure (WMI) expression, or the name of a query.

You can use this cmdlet with the *DeleteMessage* parameter to delete messages that this query finds.

This cmdlet can also add or remove a security scope for a message query.
Every status message query must belong to at least one security scope.

You can specify a name or ID for a query or use the Get-CMStatusMessageQuery cmdlet to obtain a query.

## EXAMPLES

### Example 1: Add a security scope
```
PS C:\>Set-CMStatusMessageQuery -Name "All Status Messages" -SecurityScopeAction AddMembership -SecurityScopeName "Scope22"
```

This command adds the security scope named Scope22 to the query named All Status Messages.

### Example 2: Delete messages
```
PS C:\>Set-CMStatusMessageQuery -DeleteMessage -Name "All Active Directory Security Groups"
```

This command removes messages found by the query named All Active Directory Security Groups from the System Center Configuration Manager database.

### Example 3: Rename a query
```
PS C:\>Set-CMStatusMessageQuery -Name "All Active Directory Security Groups" -NewName "Western Security Groups"
```

This command renames the query All Active Directory Security Groups.
The new name of the query is Western Security Groups.

## PARAMETERS

### -Comment


```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByObjectMandatory, SetStatusMessageQueryByIdMandatory, SetStatusMessageQueryByNameMandatory
Aliases: Comments

Required: False
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

### -DeleteMessage
Indicates that messages found by this query are deleted from the Configuration Manager database.

```yaml
Type: SwitchParameter
Parameter Sets: DeleteMessageByIdMandatory, DeleteMessageByNameMandatory, DeleteMessageByObjectMandatory
Aliases: 

Required: True
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

### -Expression


```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByObjectMandatory, SetStatusMessageQueryByIdMandatory, SetStatusMessageQueryByNameMandatory
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


```yaml
Type: String
Parameter Sets: DeleteMessageByIdMandatory, SetStatusMessageQueryByIdMandatory
Aliases: QueryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SetStatusMessageQueryByObjectMandatory, DeleteMessageByObjectMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name


```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByNameMandatory, DeleteMessageByNameMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName


```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByObjectMandatory, SetStatusMessageQueryByIdMandatory, SetStatusMessageQueryByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru


```yaml
Type: SwitchParameter
Parameter Sets: DeleteMessageByIdMandatory, DeleteMessageByNameMandatory, DeleteMessageByObjectMandatory
Aliases: 

Required: False
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

[Get-CMStatusMessageQuery](xref:ConfigurationManager/vlatest/Get-CMStatusMessageQuery.md)

[New-CMStatusMessageQuery](xref:ConfigurationManager/vlatest/New-CMStatusMessageQuery.md)

[Remove-CMStatusMessageQuery](xref:ConfigurationManager/vlatest/Remove-CMStatusMessageQuery.md)


