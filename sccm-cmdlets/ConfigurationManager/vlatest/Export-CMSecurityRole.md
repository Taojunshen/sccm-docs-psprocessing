---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834036
schema: 2.0.0
ms.assetid: 22B77C84-02CE-4101-8EAB-44700D126880
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMSecurityRole.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMSecurityRole.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Export-CMSecurityRole.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Export-CMSecurityRole

## SYNOPSIS
Exports a security role to an XML file.

## SYNTAX

### ByValue (Default)
```
Export-CMSecurityRole -Path <String> -Role <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Export-CMSecurityRole -Path <String> -RoleName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Export-CMSecurityRole -Path <String> -RoleId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMSecurityRole** cmdlet exports a security role configuration from Microsoft System Center Configuration Manager to an XML file.

## EXAMPLES

### Example 1: Export a security role
```
PS C:\>Export-CMSecurityRole -Path "\\Contoso01\Export\Sec_Roles\Security_Manager" -RoleId "SMS000CR"
```

This command exports the security role named SMS000CR to the file named Security_Manager.

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

### -Path
Specifies the path to which you export the XML file for the security role.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role


```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleId
Specifies the ID of a role.

```yaml
Type: String
Parameter Sets: ById
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName


```yaml
Type: String
Parameter Sets: ByName
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

[Copy-CMSecurityRole](xref:ConfigurationManager/vlatest/Copy-CMSecurityRole.md)

[Get-CMSecurityRole](xref:ConfigurationManager/vlatest/Get-CMSecurityRole.md)

[Import-CMSecurityRole](xref:ConfigurationManager/vlatest/Import-CMSecurityRole.md)

[Set-CMSecurityRole](xref:ConfigurationManager/vlatest/Set-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](xref:ConfigurationManager/vlatest/Remove-CMSecurityRoleFromAdministrativeUser.md)

[Remove-CMSecurityRole](xref:ConfigurationManager/vlatest/Remove-CMSecurityRole.md)


