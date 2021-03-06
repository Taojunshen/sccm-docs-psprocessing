---
external help file: AdminUI.PS.Alerts.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833969
schema: 2.0.0
ms.assetid: 4E9F8E2E-9C21-46C9-8818-F1DF00616E4D
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Enable-CMAlert.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Enable-CMAlert.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Enable-CMAlert.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Enable-CMAlert

## SYNOPSIS
Enables Configuration Manager alerts.

## SYNTAX

### SearchByValueMandatory (Default)
```
Enable-CMAlert -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Enable-CMAlert -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Enable-CMAlert -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Enable-CMAlert** cmdlet enables one or more Microsoft System Center Configuration Manager alerts.

## EXAMPLES

### Example 1: Enable an alert by using alert ID
```
PS C:\>Enable-CMAlert -Id "16777223"
```

This command enables an alert that has the ID 16777223.

### Example 2: Enable an alert by using an alert object variable
```
PS C:\> $AlertObj = Get-CMAlert -Id "16777218"
PS C:\> Enable-CMAlert -InputObject $AlertObj
```

The first command gets the alert object that has the ID 16777218, and then stores it in the $AlertObj variable.

The second command enables the alert stored in the $AlertObj variable.

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
Specifies an alert ID.
You can obtain the ID of an alert by using the [Get-CMAlert](./Get-CMAlert.md) cmdlet.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMAlert** object.
To obtain a **CMAlert** object, use **Get-CMAlert**.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Alert
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an alert name.
You can obtain the name of an alert by using **Get-CMAlert**.

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

[Get-CMAlert](xref:ConfigurationManager/vlatest/Get-CMAlert.md)

[Remove-CMAlert](xref:ConfigurationManager/vlatest/Remove-CMAlert.md)

[Set-CMAlert](xref:ConfigurationManager/vlatest/Set-CMAlert.md)

[Suspend-CMAlert](xref:ConfigurationManager/vlatest/Suspend-CMAlert.md)

[Disable-CMAlert](xref:ConfigurationManager/vlatest/Disable-CMAlert.md)


