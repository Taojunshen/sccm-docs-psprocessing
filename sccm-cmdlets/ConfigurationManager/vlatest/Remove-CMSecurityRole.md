---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834183
schema: 2.0.0
ms.assetid: 2382F219-2290-45C8-905B-E9C2D3BD6CB6
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMSecurityRole.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMSecurityRole.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMSecurityRole

## SYNOPSIS
Removes custom security roles from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMSecurityRole -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSecurityRole -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMSecurityRole -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSecurityRole** cmdlet removes custom security roles from Microsoft System Center Configuration Manager.
Specify the name or ID of a security role you want to remove or use the Get-CMSecurityRole cmdlet to obtain one.

Configuration Manager uses security roles, along with security scopes and collections, to define an administrative scope for each administrative user.
Configuration Manager provides several built-in security roles.
To create a custom security role, copy an existing security role, and then modifying the copy.
You can copy a security role by using the Copy-CMSecurityRole cmdlet.

You can use the Remove-CMSecurityRole cmdlet to remove old, unneeded custom security roles.
You cannot remove built-in security roles.
Every administrative user must have at least one security role.
Before you remove a security role, make sure every user has a role in addition to the one you remove.

## EXAMPLES

### Example 1: Remove a security role by using a name
```
PS C:\>Remove-CMSecurityRole -Name "MainSecurityRole" -Force
```

This command removes a security role named MainSecurityRole from Configuration Manager.
The command uses the *Force* parameter, so it does not prompt you for confirmation.

### Example 2: Remove security roles by using a variable
```
PS C:\>$Roles = Get-CMSecurityRole -Name *Role 
PS C:\> Remove-CMSecurityRole -SecurityRole $Roles
```

The first command uses the Get-CMSecurityRole cmdlet to get each security role that has a name that ends in Role.
It stores them in the $Roles variable.

The second command removes each security role stored in the $Roles variable.

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

### -InputObject
Specifies a security role object.
To obtain a security role object, use the Get-CMSecurityRole cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of security roles.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: RoleName

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

[Copy-CMSecurityRole](xref:ConfigurationManager/vlatest/Copy-CMSecurityRole.md)

[Export-CMSecurityRole](xref:ConfigurationManager/vlatest/Export-CMSecurityRole.md)

[Get-CMSecurityRole](xref:ConfigurationManager/vlatest/Get-CMSecurityRole.md)

[Import-CMSecurityRole](xref:ConfigurationManager/vlatest/Import-CMSecurityRole.md)

[Set-CMSecurityRole](xref:ConfigurationManager/vlatest/Set-CMSecurityRole.md)


