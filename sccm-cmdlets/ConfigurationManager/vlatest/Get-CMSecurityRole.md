---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833842
schema: 2.0.0
ms.assetid: EC701CF2-B169-4E10-A386-A1DCE7CB52A4
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSecurityRole.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSecurityRole.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSecurityRole.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMSecurityRole

## SYNOPSIS
Gets security roles.

## SYNTAX

### SearchByName (Default)
```
Get-CMSecurityRole [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSecurityRole -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSecurityRole** cmdlet gets one or more security roles in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get all security roles
```
PS C:\> Get-CMSecurityRole
```

This command gets all security roles in Configuration Manager.

### Example 2: Get a security role by using an ID
```
PS C:\> Get-CMSecurityRole -Id "SMS000CR"
```

This command gets the security role that has the ID SMS000CR.

### Example 3: Get a security role by using a wildcard
```
PS C:\> Get-CMSecurityRole -Name App*
```

This command gets all security roles that have a name that starts with App.

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
Specifies an array of IDs of security roles.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: RoleId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of security roles.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: RoleName
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

[Copy-CMSecurityRole](xref:ConfigurationManager/vlatest/Copy-CMSecurityRole.md)

[Export-CMSecurityRole](xref:ConfigurationManager/vlatest/Export-CMSecurityRole.md)

[Import-CMSecurityRole](xref:ConfigurationManager/vlatest/Import-CMSecurityRole.md)

[Remove-CMSecurityRole](xref:ConfigurationManager/vlatest/Remove-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](xref:ConfigurationManager/vlatest/Remove-CMSecurityRoleFromAdministrativeUser.md)

[Set-CMSecurityRole](xref:ConfigurationManager/vlatest/Set-CMSecurityRole.md)


