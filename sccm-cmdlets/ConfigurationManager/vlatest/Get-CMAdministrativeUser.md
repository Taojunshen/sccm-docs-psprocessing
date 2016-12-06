---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834069
schema: 2.0.0
ms.assetid: E10E2966-E438-49C0-A115-868CEDE6D8BB
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAdministrativeUser.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAdministrativeUser.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMAdministrativeUser

## SYNOPSIS
Gets an administrative user.

## SYNTAX

### SearchByName (Default)
```
Get-CMAdministrativeUser [-Name <String>] [-RoleName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAdministrativeUser -Id <String> [-RoleName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAdministrativeUser** cmdlet gets one or more administrative users in Microsoft System Center Configuration Manager.
An administrative user has a defined set of permissions and may be a member of one or more scopes or roles.

## EXAMPLES

### Example 1: Get all the administrative users
```
PS C:\> Get-CMAdministrativeUser
```

This command gets all administrative users.

### Example 2: Get administrative user by name
```
PS C:\> Get-CMAdministrativeUser -Name "testDomain\myAdminUser"
```

This command gets the administrative user named AdminUser1.

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
Specifies the ID of an administrative user.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: AdminId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of the administrative user in the form \<domain\>\\\<user\>.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: DisplayName, LogonName, UserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
Specifies an array of names of security roles.
Valid values are: 

- Application Administrator
- Application Author
- Application Deployment Manager
- Asset Manager
- Compliance Settings Manager
- Discovery Operator
- Endpoint Protection Manager
- Full Administrator
- Infrastructure Administrator
- Operating System Deployment Manager
- Operations Administrator
- Read-only Analyst
- Remote Tools Operator
- Security Administrator
- Software Update Manager
- Custom-defined security roles

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RoleNames

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

[New-CMAdministrativeUser](xref:ConfigurationManager/vlatest/New-CMAdministrativeUser.md)

[Remove-CMAdministrativeUser](xref:ConfigurationManager/vlatest/Remove-CMAdministrativeUser.md)


