---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834135
schema: 2.0.0
ms.assetid: DB1B3B24-B73F-4626-B482-1CB739D0A72C
updated_at: 12/6/2016 11:13 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMMdmEnrollmentManager.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMMdmEnrollmentManager.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/d1c6f0eeb340f832b2254d78bbd1bc9245dc24fc/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMMdmEnrollmentManager.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMMdmEnrollmentManager

## SYNOPSIS
Removes a Device Enrollment Manager.

## SYNTAX

### ByValue (Default)
```
Remove-CMMdmEnrollmentManager [-Force] -InputObject <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMMdmEnrollmentManager [-Force] -Id <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMMdmEnrollmentManager [-Force] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMMdmEnrollmentManager** cmdlet removes a Device Enrollment Manager from the Microsoft Intune subscription.

## EXAMPLES

### Example 1: Remove a device enrollment manager using the pipeline
```
PS C:\> Get-CMUser -Name "Contoso\User01"| Remove-CMMdmEnrollmentManager
```

This command gets the user object named User01 and uses the pipeline operator to pass the object to **Remove-CMMdmEnrollmentManager**, which removes the device enrollment manager.

### Example 2: Remove a device enrollment manager by name
```
PS C:\> Remove-CMMdmEnrollmentManager -Name "Contoso\User02"
```

This command removes the device enrollment manager named User02.

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
Specifies an array of Configuration Manager user IDs.

```yaml
Type: Int32[]
Parameter Sets: ById
Aliases: Ids
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an array of user objects or Device Enrollment Manager objects.
To obtain a user object, use the [Get-CMUser](./Get-CMUser.md) cmdlet.
To obtain a Device Enrollment Manager user object, use the Get-CMMdmEnrollmentManager cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: User, EnrollmentManager, Users, EnrollmentManagers
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a Configuration Manager user.

```yaml
Type: String
Parameter Sets: ByName
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

[Add-CMMdmEnrollmentManager](xref:ConfigurationManager/vlatest/Add-CMMdmEnrollmentManager.md)

[Get-CMMdmEnrollmentManager](xref:ConfigurationManager/vlatest/Get-CMMdmEnrollmentManager.md)

[Get-CMUser](xref:ConfigurationManager/vlatest/Get-CMUser.md)


