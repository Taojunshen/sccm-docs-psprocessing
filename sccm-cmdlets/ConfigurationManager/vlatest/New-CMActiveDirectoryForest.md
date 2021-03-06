---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834219
schema: 2.0.0
ms.assetid: 196CA882-2AC7-42C3-9E79-1CCE583C8079
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMActiveDirectoryForest.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMActiveDirectoryForest.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/New-CMActiveDirectoryForest.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMActiveDirectoryForest

## SYNOPSIS
Creates one or more Active Directory forest objects in Configuration Manager.

## SYNTAX

```
New-CMActiveDirectoryForest -ForestFqdn <String> [-Description <String>] [-EnableDiscovery <Boolean>]
 [-PublishingPath <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMActiveDirectoryForest** cmdlet creates an Active Directory forest object that has a fully qualified domain name (FQDN), description, and publishing path that you supply.

If you configured an Active Directory Forest Discovery method, you can enable discovery for an Active Directory forest.
After you enable discovery, Microsoft System Center Configuration Manager discovers Active Directory sites and subnets.

Active Directory Forest Discovery requires a global account to discover or publish to untrusted forests.

## EXAMPLES

### Example 1: Create an Active Directory forest object that has discovery enabled
```
PS C:\> New-CMActiveDirectoryForest -ForestFqdn "tsqa.contoso.com" -EnableDiscovery $True
```

This command creates an Active Directory forest object that has the FQDN tsqa.contoso.com and that has discovery enabled.
You must configure an Active Directory Forest Discovery method before discovery can work.

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

### -Description
Specifies a description for an Active Directory forest object.

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

### -DisableWildcardHandling


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

### -EnableDiscovery
Specifies whether to discover Active Directory sites and subnets.
If you enable discovery, you must configure an Active Directory Forest Discovery method.
The default value is $False.

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

### -ForceWildcardHandling


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

### -ForestFqdn
Specifies an FQDN of a Configuration Manager object.

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

### -PublishingPath
Specifies one or more Configuration Manager sites that publish site information to an Active Directory forest.
You can use a comma-separated list in quotation marks to specify more than one site.

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

[Set-CMActiveDirectoryForest](xref:ConfigurationManager/vlatest/Set-CMActiveDirectoryForest.md)

[Get-CMActiveDirectoryForest](xref:ConfigurationManager/vlatest/Get-CMActiveDirectoryForest.md)

[Remove-CMActiveDirectoryForest](xref:ConfigurationManager/vlatest/Remove-CMActiveDirectoryForest.md)

[Get-CMActiveDirectorySite](xref:ConfigurationManager/vlatest/Get-CMActiveDirectorySite.md)


