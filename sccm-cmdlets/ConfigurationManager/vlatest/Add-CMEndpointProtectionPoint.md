---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833669
schema: 2.0.0
ms.assetid: 405EE043-48AC-43DF-BE3F-1566DB9621E9
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMEndpointProtectionPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMEndpointProtectionPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Add-CMEndpointProtectionPoint

## SYNOPSIS
Adds a site system role for Endpoint Protection.

## SYNTAX

### ByValue (Default)
```
Add-CMEndpointProtectionPoint [-LicenseAgreed <Boolean>] -ProtectionService <MapsMembershipType>
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Add-CMEndpointProtectionPoint [-SiteSystemServerName] <String> [-SiteCode <String>] [-LicenseAgreed <Boolean>]
 -ProtectionService <MapsMembershipType> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMEndpointProtectionPoint** cmdlet adds a site system role for System Center 2016 Endpoint Protection to a Microsoft System Center Configuration Manager site.

Endpoint Protection lets you manage antimalware policies and Windows Firewall security for client computers in System Center Configuration Manager.
In order to use Endpoint Protection with System Center Configuration Manager, you must install a single site system role for Endpoint Protection, either in the central site or in a stand-alone primary site.
For more information about Endpoint Protection in System Center Configuration Manager, see [Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427) on TechNet.

## EXAMPLES

### Example 1: Add a site system role
```
PS C:\>Add-CMEndpointProtectionPoint -LicenseAgreed $True -ProtectionService BasicMembership -SiteCode "CM1" -SiteSystemServerName "CMEPPoint.Western.Contoso.com"
```

This command adds an Endpoint Protection point for the site that has the site code CM1.
The specified computer hosts the role.
The command also specifies that you accept the terms of the license agreement and have a basic membership for Endpoint Protection.

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

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LicenseAgreed


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionService


```yaml
Type: MapsMembershipType
Parameter Sets: (All)
Aliases: 
Accepted values: DoNotJoinMaps, BasicMembership, AdvancedMembership

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode


```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName


```yaml
Type: String
Parameter Sets: ByName
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

[Get-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Get-CMEndpointProtectionPoint.md)

[Remove-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Remove-CMEndpointProtectionPoint.md)

[Set-CMEndpointProtectionPoint](xref:ConfigurationManager/vlatest/Set-CMEndpointProtectionPoint.md)

