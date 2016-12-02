---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833672
schema: 2.0.0
ms.assetid: B1E83113-4742-40EC-A78F-EC46C8C50A5E
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMEmailNotificationComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMEmailNotificationComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMEmailNotificationComponent

## SYNOPSIS
Gets an email notification components.

## SYNTAX

```
Get-CMEmailNotificationComponent [-SiteSystemServerName <String>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEmailNotificationComponent** cmdlet gets one or more email notification components Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get an email notification component by using a site code
```
PS C:\>Get-CMEmailNotificationComponent -SiteCode "CM2"
```

This command gets a notification component for the site that has the site code CM2.

### Example 2: Get an email notification component by using a site system server name
```
PS C:\>Get-CMEmailNotificationComponent -SiteSystemServerName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM"
```

This command gets a notification component for the site that has the server that has the specified name.

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

### -SiteCode


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

### -SiteSystemServerName


```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

[Set-CMEmailNotificationComponent](xref:ConfigurationManager/vlatest/Set-CMEmailNotificationComponent.md)

