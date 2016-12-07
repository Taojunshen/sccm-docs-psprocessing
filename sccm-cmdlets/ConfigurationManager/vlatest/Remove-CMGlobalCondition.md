---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834116
schema: 2.0.0
ms.assetid: 607E38C4-5D67-42E4-8D3F-3D636EF15FC0
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMGlobalCondition.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMGlobalCondition.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMGlobalCondition

## SYNOPSIS
Removes a global condition object.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMGlobalCondition -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMGlobalCondition -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMGlobalCondition -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMGlobalCondition** cmdlet removes a global condition object.

Microsoft System Center Configuration Manager uses global conditions to represent business or technical conditions.
Global conditions specify how to provide and deploy applications to client devices.

You can specify a global condition by name or ID or use the **Get-CMGlobalCondition** cmdlet to obtain a global condition object.
You cannot remove read-only global conditions.

## EXAMPLES

### Example 1: Remove a global condition
```
PS C:\>Remove-CMGlobalCondition -Name "GC56" -Force
```

This command removes a global condition named GC56.
Because the command uses the *Force* parameter, the system does not prompt you before it removes the condition.

### Example 2: Remove a global condition using a variable
```
PS C:\>$CMGC = Get-CMGlobalCondition -Name "GC57"
PS C:\> Remove-CMGlobalCondition -InputObject $CMGC
Remove
Are you sure you wish to remove GlobalCondition: 
LocalizedDisplayName=" GC57"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

The first command uses the **Get-CMGlobalCondition** cmdlet to get the global condition named GC57 and stores it in the $CMGC variable.

The second command removes the global condition stored in that variable.
This command does not use the *Force* parameter, so it prompts you for confirmation before it removes the global condition.

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
Performs the action without a confirmation message.

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
Specifies an array of identifiers of global conditions.
This value corresponds to the **CI_ID** property of a global condition object.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CIId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a global condition object.
To obtain a global condition object, use the **Get-CMGlobalCondition** cmdlet.

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
Specifies an array of names for global conditions.
This value corresponds to the **LocalizedDisplayName** property of a global condition object.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName
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

[Get-CMGlobalCondition](xref:ConfigurationManager/vlatest/Get-CMGlobalCondition.md)

[New-CMGlobalCondition](xref:ConfigurationManager/vlatest/New-CMGlobalCondition.md)

[Set-CMGlobalCondition](xref:ConfigurationManager/vlatest/Set-CMGlobalCondition.md)


