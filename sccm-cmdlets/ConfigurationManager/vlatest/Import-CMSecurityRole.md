---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834075
schema: 2.0.0
ms.assetid: 00C0842E-0AA5-462E-9C22-18254F2407DB
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMSecurityRole.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMSecurityRole.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMSecurityRole.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Import-CMSecurityRole

## SYNOPSIS
Imports a security role into Configuration Manager.

## SYNTAX

```
Import-CMSecurityRole -Overwrite <Boolean> -XmlFileName <String> [-NewRoleName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMSecurityRole** cmdlet imports a security role that was exported from another Microsoft System Center Configuration Manager hierarchy.

## EXAMPLES

### Example 1: Import a security role
```
PS C:\>Import-CMSecurityRole -Overwrite $True -XmlFileName "RemoteAdminSecurity.xml"
```

This command imports a security role into Configuration Manager from the XML export file named RemoteAdminSecurity.
The command specifies that the security role that you import overwrites an existing security role with the same name.

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

### -NewRoleName


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

### -Overwrite
Indicates whether the security role that you import overwrites an existing security role with the same name that you specify in the *XmlFileName* parameter.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: OverwrittenExisted
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

### -XmlFileName
Specifies the XML export file that contains the security role definition.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RolesXml
Required: True
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

[Get-CMSecurityRole](xref:ConfigurationManager/vlatest/Get-CMSecurityRole.md)

[Remove-CMSecurityRole](xref:ConfigurationManager/vlatest/Remove-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](xref:ConfigurationManager/vlatest/Remove-CMSecurityRoleFromAdministrativeUser.md)

[Set-CMSecurityRole](xref:ConfigurationManager/vlatest/Set-CMSecurityRole.md)


