---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834157
schema: 2.0.0
ms.assetid: 072CB4A9-2915-4126-99E2-A595A94C57F4
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMRemoteControl.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Invoke-CMRemoteControl.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Invoke-CMRemoteControl

## SYNOPSIS
Enables remote control on computers.

## SYNTAX

### InvokeDeviceByValueMandatory (Default)
```
Invoke-CMRemoteControl -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeSiteStatusByNameMandatory
```
Invoke-CMRemoteControl -SiteSystemServerName <String> [-SiteSystemRole <String>] [-SiteCode <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeDeviceByNameMandatory
```
Invoke-CMRemoteControl -DeviceName <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### InvokeDeviceByIdMandatory
```
Invoke-CMRemoteControl -DeviceId <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMRemoteControl** cmdlet enables remote control on the computers that you want to use in a remote control session.
You can enable remote control on computers by specifying the ID or name of the computers, the site systems, or the site status.

Use remote control in Microsoft System Center Configuration Manager to remotely administer, provide assistance, or view any client computer in the hierarchy.
You can use remote control to troubleshoot hardware and software configuration problems on client computers and to provide help desk support when access to the computer of a user is required.
System Center Configuration Manager supports the remote control of workgroup computers and computers that are joined to an Active Directory domain.

## EXAMPLES

### Example 1: Enable remote control on a computer
```
PS C:\>Invoke-CMRemoteControl -DeviceName "CMCEN-DIST02"
```

This command enables remote control on the computer named CMCEN-DIST02.

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

### -DeviceId
Specifies an array of device IDs.

```yaml
Type: String
Parameter Sets: InvokeDeviceByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies an array of device names.

```yaml
Type: String
Parameter Sets: InvokeDeviceByNameMandatory
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


```yaml
Type: IResultObject
Parameter Sets: InvokeDeviceByValueMandatory
Aliases: Device, SiteStatus

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru


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

### -SiteCode
Specifies an array of site codes of Configuration Manager sites that host the site system roles.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemRole
Specifies an array of Configuration Manager roles that the site system performs.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
Aliases: Role

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies an array of fully qualified domain names (FQDN) of the servers that host the site system roles.

```yaml
Type: String
Parameter Sets: InvokeSiteStatusByNameMandatory
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

[Get-CMDevice](xref:ConfigurationManager/vlatest/Get-CMDevice.md)

[Get-CMSiteStatusMessage](xref:ConfigurationManager/vlatest/Get-CMSiteStatusMessage.md)


