---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833644
schema: 2.0.0
ms.assetid: 783C11B5-AF37-4B77-A78D-C43C7E1330DE
updated_at: 12/7/2016 8:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDeviceVariable.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/282d10ca7ed3ddf1432b06182fee46c9e52563a4/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDeviceVariable.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMDeviceVariable

## SYNOPSIS
Gets device variables.

## SYNTAX

### SearchByValueMandatory (Default)
```
Get-CMDeviceVariable -InputObject <IResultObject> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDeviceVariable -ResourceId <String> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameMandatory
```
Get-CMDeviceVariable -DeviceName <String> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeviceVariable** cmdlet gets device variables.
Individual devices have device variables.
Task sequence processing uses device variables.

## EXAMPLES

### Example 1: Get a variable value by using its name
```
PS C:\>Get-CMDeviceVariable -DeviceName "Computer073" -VariableName "HostDrive"
```

This command gets the value of the variable named HostDrive for the specified computer.

## PARAMETERS

### -DeviceName
Specifies a device name.
You can specify a NetBIOS name or a fully qualified domain name (FQDN).

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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Device
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ResourceId
Specifies a Systems Management Server (SMS) ID.

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

### -VariableName
Specifies the name of the device variable.

```yaml
Type: String
Parameter Sets: (All)
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

[New-CMDeviceVariable](xref:ConfigurationManager/vlatest/New-CMDeviceVariable.md)

[Remove-CMDeviceVariable](xref:ConfigurationManager/vlatest/Remove-CMDeviceVariable.md)

[Set-CMDeviceVariable](xref:ConfigurationManager/vlatest/Set-CMDeviceVariable.md)

[Get-CMDevice](xref:ConfigurationManager/vlatest/Get-CMDevice.md)


