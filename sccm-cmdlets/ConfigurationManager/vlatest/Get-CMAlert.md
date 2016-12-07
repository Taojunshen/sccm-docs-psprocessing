---
external help file: AdminUI.PS.Alerts.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834073
schema: 2.0.0
ms.assetid: AB20D6C3-3817-400F-B098-371536B4513C
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAlert.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAlert.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMAlert

## SYNOPSIS
Gets Configuration Manager alerts.

## SYNTAX

### SearchByName (Default)
```
Get-CMAlert [[-Name] <String>] [-TypeInstanceId <String>] [-TypeId <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAlert [-Id] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAlert** cmdlet gets one or more Microsoft System Center Configuration Manager alerts.
You can get a specific alert by specifying the name or ID of the alert.

## EXAMPLES

### Example 1: Get all alerts
```
PS C:\>Get-CMAlert
```

This command gets all alerts that System Center Configuration Manager manages.

### Example 2: Get alerts by using name
```
PS C:\>Get-CMAlert -Name "D*"
```

This command gets all alerts that have a name that begins with the letter D.

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
Specifies an alert ID.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an alert name.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeId


```yaml
Type: Int32
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeInstanceId


```yaml
Type: String
Parameter Sets: SearchByName
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

[Enable-CMAlert](xref:ConfigurationManager/vlatest/Enable-CMAlert.md)

[Remove-CMAlert](xref:ConfigurationManager/vlatest/Remove-CMAlert.md)

[Set-CMAlert](xref:ConfigurationManager/vlatest/Set-CMAlert.md)

[Suspend-CMAlert](xref:ConfigurationManager/vlatest/Suspend-CMAlert.md)

[Disable-CMAlert](xref:ConfigurationManager/vlatest/Disable-CMAlert.md)


