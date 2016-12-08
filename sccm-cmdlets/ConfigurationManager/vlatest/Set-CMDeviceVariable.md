---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833806
schema: 2.0.0
ms.assetid: 7FFB20CC-CC5E-4817-9DE8-CE34A40A8C11
updated_at: 12/8/2016 3:33 AM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMDeviceVariable.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/3f2e54f6163618b87e89b0d1fa27e9897f65a1e2/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMDeviceVariable.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMDeviceVariable

## SYNOPSIS
Modifies a device variable.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMDeviceVariable -InputObject <IResultObject> -VariableName <String> [-NewVariableName <String>]
 [-NewVariableValue <String>] [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByIdMandatory
```
Set-CMDeviceVariable -ResourceId <String> -VariableName <String> [-NewVariableName <String>]
 [-NewVariableValue <String>] [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMDeviceVariable -DeviceName <String> -VariableName <String> [-NewVariableName <String>]
 [-NewVariableValue <String>] [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDeviceVariable** cmdlet modifies a device variable.
Individual devices have device variables.
Task sequence processing uses device variables.

## EXAMPLES

### Example 1: Modify a device variable
```
PS C:\>Set-CMDeviceVariable -DeviceName "gateway-server.contoso.com" -VariableName "ServerIPAddress" -NewVariableValue "192.168.100.10"
```

This command modifies the device variable ServerIPAddress associated with the device gateway-server.contoso.com.
In this example, the value of the variable is set to 192.168.100.10.

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
Parameter Sets: SetByValueMandatory
Aliases: Device
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsMask
Indicates whether a value displays in the Configuration Manager console.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewVariableName
Specifies a name for the variable that this cmdlet modifies.

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

### -NewVariableValue
Specifies a value for the variable that this cmdlet modifies.

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

### -ResourceId
Specifies a Systems Management Server (SMS) ID.

```yaml
Type: String
Parameter Sets: SetByIdMandatory
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

[Get-CMDeviceVariable](xref:ConfigurationManager/vlatest/Get-CMDeviceVariable.md)

[New-CMDeviceVariable](xref:ConfigurationManager/vlatest/New-CMDeviceVariable.md)

[Remove-CMDeviceVariable](xref:ConfigurationManager/vlatest/Remove-CMDeviceVariable.md)
