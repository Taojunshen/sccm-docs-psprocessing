---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833933
schema: 2.0.0
ms.assetid: 4726F813-5B03-4939-BC9D-C5AC93D795A4
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMStateMigrationPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMStateMigrationPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMStateMigrationPoint

## SYNOPSIS
Gets a state migration point for a Configuration Manager site.

## SYNTAX

### SearchByName
```
Get-CMStateMigrationPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMStateMigrationPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMStateMigrationPoint** cmdlet gets a state migration point for a Microsoft System Center Configuration Manager site.
This site system role stores user information.
You can store user information while an operating system deployment proceeds and then restore user information from the state migration point.

You can use this cmdlet to get state migration point objects to use with the Remove-CMStateMigrationPoint cmdlet.

Each state migration point site server can be a member of only one System Center Configuration Manager site.

## EXAMPLES

### Example 1: Get a migration point
```
PS C:\>Get-CMStateMigrationPoint -SiteCode "CM1" -SiteSystemServerName "SMP01.Western.Contoso.com"
```

This command gets a state migration point that belongs to the specified site and has the specified host name.

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

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

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

### -SiteSystemServerName
Specifies the host name for a state migration point.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName
Required: False
Position: 0
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

[Add-CMStateMigrationPoint](xref:ConfigurationManager/vlatest/Add-CMStateMigrationPoint.md)

[Remove-CMStateMigrationPoint](xref:ConfigurationManager/vlatest/Remove-CMStateMigrationPoint.md)

[Set-CMStateMigrationPoint](xref:ConfigurationManager/vlatest/Set-CMStateMigrationPoint.md)


