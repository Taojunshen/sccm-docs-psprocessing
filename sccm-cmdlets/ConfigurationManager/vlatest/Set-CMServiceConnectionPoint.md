---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834026
schema: 2.0.0
ms.assetid: F070D51A-7602-48DE-A367-95F647D42D3F
updated_at: 2/17/2017 8:35 PM
ms.date: 2/17/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMServiceConnectionPoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMServiceConnectionPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/c28949c2167e895d621a0a34a9b5d48507b8a811/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMServiceConnectionPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMServiceConnectionPoint

## SYNOPSIS
Sets a service connection point.

## SYNTAX

### ByValue (Default)
```
Set-CMServiceConnectionPoint [-Mode <ServiceConnectionPointMode>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMServiceConnectionPoint [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-Mode <ServiceConnectionPointMode>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMServiceConnectionPoint** updates the settings of a connection service point.

## EXAMPLES

### Example 1: Set a service connection point
```
PS C:\> Set-CMServiceConnectionPoint -SiteSystemServerName "SiteSystemServer01.Contoso.com" -SiteCode PS1 -Mode Offline
```

This command sets the mode for the site system server named SiteSystemServer01.Contoso.com to offline.

### Example 2: Set a service connection point by using a variable
```
PS C:\> $Server = Get-CMServiceConnectionPoint -SiteCode PS1 -SiteSystemServerName "SiteSystemServer02.Contoso.com"
PS C:\> Set-CMServiceConnectionPoint -InputObject $Server -Mode Offline
```

The first command gets the site system server object named SiteSystemServer02.Contoso.com with the site code PS1 and stores the object in the $Server variable.

The second command sets the mode for the site system server stored in $Server to offline.

### Example 3: Set a service connection point by using the pipeline
```
PS C:\> Get-CMServiceConnectionPoint -SiteCode PS1 -SiteSystemServerName "SiteSystemServer03.Contoso.com" | Set-CMServiceConnectionPoint -Mode Offline
```

This command gets the site system server object named SiteSystemServer03.Contoso.com with the site code PS1 and uses the pipeline operator to pass the object to **Set-CMServiceConnectionPoint**, which sets the mode for the server object to offline.

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

### -InputObject
Specifies a service connection point object.
To obtain a service connection point object, use the Get-CMServiceConnectionPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: ServiceConnectionPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Mode
Specifies a mode for the service connection point.
Valid values are: 

- Online
- Offline

```yaml
Type: ServiceConnectionPointMode
Parameter Sets: (All)
Aliases: 
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a site system server that hosts the service connection point role.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name, ServerName

Required: True
Position: 0
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

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Add-CMServiceConnectionPoint](xref:ConfigurationManager/vlatest/Add-CMServiceConnectionPoint.md)

[Get-CMServiceConnectionPoint](xref:ConfigurationManager/vlatest/Get-CMServiceConnectionPoint.md)

[Remove-CMServiceConnectionPoint](xref:ConfigurationManager/vlatest/Remove-CMServiceConnectionPoint.md)


