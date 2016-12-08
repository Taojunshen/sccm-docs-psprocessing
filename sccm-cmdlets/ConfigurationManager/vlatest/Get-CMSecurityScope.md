---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833847
schema: 2.0.0
ms.assetid: 0F19406F-06D0-4A41-8B99-7EE68F379737
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSecurityScope.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSecurityScope.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMSecurityScope

## SYNOPSIS
Gets a security scope.

## SYNTAX

### SearchByName (Default)
```
Get-CMSecurityScope [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSecurityScope -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSecurityScope** cmdlet gets one or more security scopes in Microsoft System Center Configuration Manager.
You can get a security scope by its name or ID.
If you don't provide any parameters, all security scopes are returned.

## EXAMPLES

### Example 1: Get a security scope by name
```
PS C:\> Get-CMSecurityScope -Name "Scope"
```

This command gets the security scope named Scope.

### Example 2: Get a security scope by using a wildcard
```
PS C:\> Get-CMSecurityScope -Name "S*"
```

This command gets all security scope objects that have a name beginning with "S".

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
Specifies the ID of a security scope.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CategoryId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a security scope.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CategoryName
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

[New-CMSecurityScope](xref:ConfigurationManager/vlatest/New-CMSecurityScope.md)

[Remove-CMSecurityScope](xref:ConfigurationManager/vlatest/Remove-CMSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](xref:ConfigurationManager/vlatest/Remove-CMSecurityScopeFromAdministrativeUser.md)

[Set-CMSecurityScope](xref:ConfigurationManager/vlatest/Set-CMSecurityScope.md)


