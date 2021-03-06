---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833662
schema: 2.0.0
ms.assetid: 6122AB0E-4285-41D0-9AC7-9A465A345FA0
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMExchangeServerConnectorAccessRule.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMExchangeServerConnectorAccessRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/New-CMExchangeServerConnectorAccessRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMExchangeServerConnectorAccessRule

## SYNOPSIS
Configures access settings for a mobile device that uses a Microsoft Exchange Server connector.

## SYNTAX

```
New-CMExchangeServerConnectorAccessRule -RuleName <String> -AccessLevel <AccessLevelType> -Device <DeviceType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServerConnectorAccessRule** cmdlet configures access settings for a mobile device that uses a Microsoft Exchange Server connector.

## EXAMPLES

### Example 1: Configure email management settings for a mobile device
```
PS C:\> New-CMExchangeServerConnectorAccessRule -RuleName "AccessRule01" -AccessLevel Allow -Device DeviceType
```

This command creates an access rule for a device type named AccessRule01 that has the Allow access level.

## PARAMETERS

### -AccessLevel
Specifies the type of access for the mobile device.
The acceptable values for this parameter are:

- Allow 
- Block 
- Quarantine

```yaml
Type: AccessLevelType
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Block, Quarantine
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Device
Specifies the device type of the mobile device.
The acceptable values for this parameter are:

- DeviceModel 
- DeviceType

```yaml
Type: DeviceType
Parameter Sets: (All)
Aliases: 
Accepted values: DeviceType, DeviceModel
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

### -RuleName
Specifies a name for the access rule.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorApplicationSetting](xref:ConfigurationManager/vlatest/New-CMExchangeServerConnectorApplicationSetting.md)

[New-CMExchangeServerConnectorEmailManagementSetting](xref:ConfigurationManager/vlatest/New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorPasswordSetting](xref:ConfigurationManager/vlatest/New-CMExchangeServerConnectorPasswordSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](xref:ConfigurationManager/vlatest/New-CMExchangeServerConnectorSecuritySetting.md)


