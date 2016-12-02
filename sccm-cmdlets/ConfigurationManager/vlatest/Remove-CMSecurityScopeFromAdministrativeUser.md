---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834196
schema: 2.0.0
ms.assetid: 5647FB87-7F94-4AEA-95A1-A8AF521325E9
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMSecurityScopeFromAdministrativeUser.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMSecurityScopeFromAdministrativeUser.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMSecurityScopeFromAdministrativeUser

## SYNOPSIS
Removes the association between security scopes and an administrative user.

## SYNTAX

### RemoveScopeFromAdminByName_Name (Default)
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScopeName <String> -AdministrativeUserName <String>
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminById_Name
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScopeId <String> -AdministrativeUserName <String>
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminById_Id
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScopeId <String> -AdministrativeUserId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminById_Object
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScopeId <String> -AdministrativeUser <IResultObject>
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminByName_Id
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScopeName <String> -AdministrativeUserId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminByName_Object
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScopeName <String> -AdministrativeUser <IResultObject>
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminByObject_Id
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScope <IResultObject> -AdministrativeUserId <Int32>
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminByObject_Name
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScope <IResultObject> -AdministrativeUserName <String>
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminByObject_Object
```
Remove-CMSecurityScopeFromAdministrativeUser -SecurityScope <IResultObject> -AdministrativeUser <IResultObject>
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSecurityScopeFromAdministrativeUser** cmdlet removes the association between one or more security scopes and an administrative user.

After you remove the association between a security scope and an administrative user, the administrative user cannot view the objects in Microsoft System Center Configuration Manager that are associated with the security scope, and no longer has the permission to perform the tasks that are related to those objects.

## EXAMPLES

### Example 1: Remove a security scope from an administrative user
```
PS C:\>Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUserName "Contoso\PattiFuller" -SecurityScopeName "SecScope02"
```

This command removes the association between the security scope named SecScope02 and the administrative user named Contoso\PattiFuller.

## PARAMETERS

### -AdministrativeUser
Specifies a **CMAdministrativeUser** object.
To obtain a **CMAdministrativeUser** object, use the Get-CMAdministrativeUser cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveScopeFromAdminById_Object, RemoveScopeFromAdminByName_Object, RemoveScopeFromAdminByObject_Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AdministrativeUserId
Specifies the ID of an administrative user.

```yaml
Type: Int32
Parameter Sets: RemoveScopeFromAdminById_Id, RemoveScopeFromAdminByName_Id, RemoveScopeFromAdminByObject_Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeUserName
Specifies the name of an administrative user.

```yaml
Type: String
Parameter Sets: RemoveScopeFromAdminByName_Name, RemoveScopeFromAdminById_Name, RemoveScopeFromAdminByObject_Name
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

### -Force
Forces the command to run without asking for user confirmation.

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

### -SecurityScope
Specifies a security scope object.
To obtain a security scope object, use the Get-CMSecurityScope cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveScopeFromAdminByObject_Id, RemoveScopeFromAdminByObject_Name, RemoveScopeFromAdminByObject_Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SecurityScopeId
Specifies the ID of a security scope.

```yaml
Type: String
Parameter Sets: RemoveScopeFromAdminById_Name, RemoveScopeFromAdminById_Id, RemoveScopeFromAdminById_Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeName
Specifies the name of a security scope.
A security scope name can be Default or the name of a custom security scope.

```yaml
Type: String
Parameter Sets: RemoveScopeFromAdminByName_Name, RemoveScopeFromAdminByName_Id, RemoveScopeFromAdminByName_Object
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

[Get-CMSecurityScope](xref:ConfigurationManager/vlatest/Get-CMSecurityScope.md)

[New-CMSecurityScope](xref:ConfigurationManager/vlatest/New-CMSecurityScope.md)

[Remove-CMSecurityScope](xref:ConfigurationManager/vlatest/Remove-CMSecurityScope.md)

[Set-CMSecurityScope](xref:ConfigurationManager/vlatest/Set-CMSecurityScope.md)

