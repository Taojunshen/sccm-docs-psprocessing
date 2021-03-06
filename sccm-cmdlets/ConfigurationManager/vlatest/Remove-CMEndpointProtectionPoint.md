---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834090
schema: 2.0.0
ms.assetid: A5A05130-1B29-4F27-8AC3-39BE3F13D305
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMEndpointProtectionPoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMEndpointProtectionPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMEndpointProtectionPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMEndpointProtectionPoint

## SYNOPSIS
Removes an Endpoint Protection point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMEndpointProtectionPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMEndpointProtectionPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMEndpointProtectionPoint** cmdlet removes a System Center 2016 Endpoint Protection point from Microsoft System Center Configuration Manager.
For more information about Endpoint Protection in Configuration Manager, see [Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427) on TechNet.

## EXAMPLES

### Example 1: Remove an Endpoint Protection point
```
PS C:\> Remove-CMEndpointProtectionPoint -SiteSystemServerName "CMServer01.Contoso.com" -SiteCode "CM1"
```

This command removes an Endpoint Protection point.

### Example 2: Remove an Endpoint Protection point by using an input object
```
PS C:\> $EPP = Get-CMEndpointProtectionPoint -SiteCode "CM1" -SiteSystemServerName "CMServer01.Contoso.com" 
PS C:\> Remove-CMEndpointProtectionPoint -InputObject $EPP
```

The first command uses the **Get-CMEndpointProtectionPoint** cmdlet to get an Endpoint Protection point object and assign it to the variable $EPP.

The second command removes the Endpoint Protection point object that is assigned to the variable $EPP.

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

### -InputObject
Specifies the input to this cmdlet.
To obtain an input object, use the Get-CMEndpointProtectionPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: EndpointProtectionPoint
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName
Required: True
Position: 0
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

[Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427)

[Add-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Add-CMEndpointProtectionPoint.md)

[Get-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Get-CMEndpointProtectionPoint.md)

[Set-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Set-CMEndpointProtectionPoint.md)


