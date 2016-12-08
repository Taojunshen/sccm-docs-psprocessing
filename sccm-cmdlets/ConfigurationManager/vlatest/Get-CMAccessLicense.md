---
external help file: AdminUI.PS.CalTracking.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834053
schema: 2.0.0
ms.assetid: F4A560C6-BF3A-423B-B6FB-F779E2863F4F
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAccessLicense.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAccessLicense.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMAccessLicense

## SYNOPSIS
Gets license usage information.

## SYNTAX

### ByName (Default)
```
Get-CMAccessLicense [-License] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMAccessLicense -LicenseName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByCount
```
Get-CMAccessLicense -LicenseName <String> [-Count] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAccessLicense** cmdlet gets license usage information for the servers and clients in the scope of System Center Configuration Manager.
This cmdlet returns a list of features able to be licensed and a list of unique users and devices per licensable feature.

## EXAMPLES

### Example 1: Get all licensable features for all servers and clients
```
PS C:\> Get-CMAccessLicense -License
```

This command gets all licensable features for all servers and clients within the scope of System Center Configuration Manager.

### Example 2: Get the unique users, devices, and license-specific unique ID for a specified license
```
PS C:\> Get-CMAccessLicense -LicenseName ConfigMgr_2012_EndPointClient
```

This command gets the unique users, devices, and license-specific IDs for the license named ConfigMgr_2012_EndPointClient.

## PARAMETERS

### -Count
Indicates that the cmdlet returns a count of unique users and devices for the specified licensable feature.

```yaml
Type: SwitchParameter
Parameter Sets: ByCount
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

### -License
Indicates that the cmdlet gets all licensable features for all of the servers and clients within the scope of System Center Configuration Manager.
You can specify the name of the license that is returned for the *LicenseName* parameter to obtain the unique users and devices for that specific license.

```yaml
Type: SwitchParameter
Parameter Sets: ByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseName
Specifies the name of a licensable feature.
If specified, the cmdlet gets only the unique users and devices for the specified license name.
The acceptable values for this parameter are:

- ConfigMgr_2012_CoreServer
- ConfigMgr_2012_CoreClient
- ConfigMgr_2012_EndpointClient

```yaml
Type: String
Parameter Sets: ByValue, ByCount
Aliases: 
Accepted values: ConfigMgr_2012_CoreServer, ConfigMgr_2012_CoreClient, ConfigMgr_2012_EndpointClient
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


