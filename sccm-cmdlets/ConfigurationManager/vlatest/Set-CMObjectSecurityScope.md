---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833954
schema: 2.0.0
ms.assetid: 0D58EEC5-1105-4C96-9CCB-CC0DDDE2F240
updated_at: 12/7/2016 10:23 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMObjectSecurityScope.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/7e5b4c3ad3b309b969cc9a0403712b3ad7fae461/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMObjectSecurityScope.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMObjectSecurityScope

## SYNOPSIS
Sets the security scopes for Configuration Manager objects.

## SYNTAX

```
Set-CMObjectSecurityScope -InputObject <IResultObject[]> -Action <SecurityScopeActionType> -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMObjectSecurityScope** cmdlet adds and removes security scopes for Microsoft System Center Configuration Manager objects.

This cmdlet has been deprecated and may be removed in a future release.
Use [Add-CMObjectSecurityScope](./Add-CMObjectSecurityScope.md) and [Remove-CMObjectSecurityScope](./Remove-CMObjectSecurityScope.md) to add and remove security scopes from Configuration Manager objects.

## EXAMPLES

### Example 1: Add a security scope to application objects by using the pipeline
```
PS C:\>Get-CMApplication -Name "Application*" | Set-CMObjectSecurityScope -Action AddMembership -Name "Scope1"
```

This command gets all application objects that have a name beginning with Application and uses the pipeline operator to pass the objects to **Set-CMObjectSecurityScope**.
**Set-CMObjectSecurityScope** adds the security scope named Scope1 to each application object.

### Example 2: Add a security scope to application objects
```
PS C:\>Set-CMObjectSecurityScope -InputObject (Get-CMApplication -Name "Application*") -Action AddMembership -Name "Scope1"
```

This command gets all application objects that have a name beginning with Application and adds the security scope named Scope1 to each application object.

## PARAMETERS

### -Action
Specifies the action that this cmdlet takes on the security scope.
Valid values are: 

- AddMembership
- RemoveMembership

```yaml
Type: SecurityScopeActionType
Parameter Sets: (All)
Aliases: SecurityScopeAction
Accepted values: AddMembership, RemoveMembership
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
Specifies an array of Configuration Manager objects associated with a security scope.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a security scope.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecurityScopeName
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

[Add-CMObjectSecurityScope](xref:ConfigurationManager/vlatest/Add-CMObjectSecurityScope.md)

[Get-CMObjectSecurityScope](xref:ConfigurationManager/vlatest/Get-CMObjectSecurityScope.md)

[Remove-CMObjectSecurityScope](xref:ConfigurationManager/vlatest/Remove-CMObjectSecurityScope.md)
