---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833743
schema: 2.0.0
ms.assetid: B521723C-DE6D-4EE3-9742-8BB6F8F44E72
updated_at: 12/7/2016 8:47 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMSecurityRoleToAdministrativeUser.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMSecurityRoleToAdministrativeUser.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/282d10ca7ed3ddf1432b06182fee46c9e52563a4/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMSecurityRoleToAdministrativeUser.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Add-CMSecurityRoleToAdministrativeUser

## SYNOPSIS
Adds a security role to an administrative user or group in Configuration Manager.

## SYNTAX

### AddRoleToAdminByName_Name (Default)
```
Add-CMSecurityRoleToAdministrativeUser -RoleName <String> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Id
```
Add-CMSecurityRoleToAdministrativeUser -RoleId <String> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Object
```
Add-CMSecurityRoleToAdministrativeUser -RoleId <String> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Name
```
Add-CMSecurityRoleToAdministrativeUser -RoleId <String> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByName_Object
```
Add-CMSecurityRoleToAdministrativeUser -RoleName <String> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByName_Id
```
Add-CMSecurityRoleToAdministrativeUser -RoleName <String> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Id
```
Add-CMSecurityRoleToAdministrativeUser -InputObject <IResultObject> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Name
```
Add-CMSecurityRoleToAdministrativeUser -InputObject <IResultObject> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Object
```
Add-CMSecurityRoleToAdministrativeUser -InputObject <IResultObject> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMSecurityRoleToAdministrativeUser** cmdlet adds a security role to an administrative user or administrative group in Microsoft System Center Configuration Manager.

Permissions defined in a role represent object types and actions available for each object type.
System Center Configuration Manager provides some built-in security roles.
You can also create custom security roles.
For more information about security roles, see [Configuring Security for Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=247225) on TechNet.

You can specify an administrative user or group by name or by ID or you can use the use the [Get-CMAdministrativeUser](./Get-CMAdministrativeUser.md) cmdlet to obtain a user or group object.
You can specify a role to add by name or by ID, or you can use the [Get-CMSecurityRole](./Get-CMSecurityRole.md) cmdlet to obtain a role.

## EXAMPLES

### Example 1: Add a named role to a named user group
```
PS C:\>Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName "Western Administrators " -RoleName "SecurityRole17"
```

This command adds a security role named SecurityRole17 to the administrative group named Western Administrators.

### Example 2: Add a role to a named user group identified by using an ID
```
PS C:\>Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName "Western Administrators" -RoleId "SMS38973"
```

This command adds a security role that has the specified ID to the administrative group named Western Administrators.

## PARAMETERS

### -AdministrativeUser
Specifies an administrative user or administrative group object.
To obtain an administrative user or administrative group object, use the [Get-CMAdministrativeUser](./Get-CMAdministrativeUser.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddRoleToAdminById_Object, AddRoleToAdminByName_Object, AddRoleToAdminByObject_Object
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AdministrativeUserId
Specifies an ID of an administrative user or administrative group.

```yaml
Type: Int32
Parameter Sets: AddRoleToAdminById_Id, AddRoleToAdminByName_Id, AddRoleToAdminByObject_Id
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeUserName
Specifies a name of an administrative user or administrative group.

```yaml
Type: String
Parameter Sets: AddRoleToAdminByName_Name, AddRoleToAdminById_Name, AddRoleToAdminByObject_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: AddRoleToAdminByObject_Id, AddRoleToAdminByObject_Name, AddRoleToAdminByObject_Object
Aliases: Role
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleId
Specifies an ID of a role.
A role represents Configuration Manager permissions granted to a user.

```yaml
Type: String
Parameter Sets: AddRoleToAdminById_Id, AddRoleToAdminById_Object, AddRoleToAdminById_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
Specifies a name of a role.
A role represents Configuration Manager permissions granted to a user.

```yaml
Type: String
Parameter Sets: AddRoleToAdminByName_Name, AddRoleToAdminByName_Object, AddRoleToAdminByName_Id
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

[Add-CMSecurityScopeToAdministrativeUser](xref:ConfigurationManager/vlatest/Add-CMSecurityScopeToAdministrativeUser.md)

[Get-CMAdministrativeUser](xref:ConfigurationManager/vlatest/Get-CMAdministrativeUser.md)

[Get-CMSecurityRole](xref:ConfigurationManager/vlatest/Get-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](xref:ConfigurationManager/vlatest/Remove-CMSecurityRoleFromAdministrativeUser.md)


