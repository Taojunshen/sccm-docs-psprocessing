---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833832
schema: 2.0.0
ms.assetid: 529564E3-1620-41B3-B0AF-504FEB1FB194
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMWindowsFirewallPolicy.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMWindowsFirewallPolicy.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/New-CMWindowsFirewallPolicy.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMWindowsFirewallPolicy

## SYNOPSIS
Creates a new Windows Firewall policy in Configuration Manager.

## SYNTAX

```
New-CMWindowsFirewallPolicy -Name <String> [-Description <String>] [-DomainTurnOnFirewall <SettingType>]
 [-PrivateTurnOnFirewall <SettingType>] [-PublicTurnOnFirewall <SettingType>]
 [-DomainBlockAllInboundTraffic <SettingType>] [-PrivateBlockAllInboundTraffic <SettingType>]
 [-PublicBlockAllInboundTraffic <SettingType>] [-DomainNotification <SettingType>]
 [-PrivateNotification <SettingType>] [-PublicNotification <SettingType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMWindowsFirewallPolicy** cmdlet creates a configuration policy for Windows Firewall in Microsoft System Center Configuration Manager.

Windows Firewall allows or denies incoming connections to an IP address.
The blocking actions allow or deny incoming traffic based on a network location type.
The network location types are: domain, public, and private.

## EXAMPLES

### Example 1: Create a Windows Firewall policy
```
PS C:\> New-CMWindowsFirewallPolicy -Name "test01" -Description "323132" -DomainTurnOnFirewall Yes -PrivateTurnOnFirewall Yes -PublicTurnOnFirewall Yes
```

This command creates a new Windows Firewall policy and enables the firewall for domain, private, and public network location types.

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

### -Description
Specifies a description for the firewall policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription
Required: False
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

### -DomainBlockAllInboundTraffic
Specifies whether to block all incoming traffic for a domain type of network location.The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNotification


```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: DomainNotifications
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainTurnOnFirewall
Specifies whether to turn on a firewall for a domain type of network location. 
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No, NotConfigured
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

### -Name
Specifies a name for the firewall policy in Configuration Manager.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateBlockAllInboundTraffic
Specifies whether to block all incoming traffic for a private type of network location. 
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateNotification


```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: PrivateNotifications
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateTurnOnFirewall
Specifies whether to turn on a firewall for a private type of network location. 
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicBlockAllInboundTraffic
Specifies whether to block all incoming traffic for a public type of network location. 
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNotification


```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: PublicNotifications
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicTurnOnFirewall
Specifies whether to enable Windows Firewall for a public network location. 
The acceptable values for this parameter are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: 
Accepted values: Yes, No, NotConfigured
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

[Set-CMWindowsFirewallPolicy](xref:ConfigurationManager/vlatest/Set-CMWindowsFirewallPolicy.md)


