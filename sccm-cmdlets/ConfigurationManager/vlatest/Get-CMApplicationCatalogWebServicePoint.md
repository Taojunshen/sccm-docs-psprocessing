---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834087
schema: 2.0.0
ms.assetid: F8EC64DE-F2D9-4AD0-86DB-0C978E8DD372
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMApplicationCatalogWebServicePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMApplicationCatalogWebServicePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMApplicationCatalogWebServicePoint

## SYNOPSIS
Gets an Application Catalog web service point.

## SYNTAX

### SearchByName
```
Get-CMApplicationCatalogWebServicePoint [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMApplicationCatalogWebServicePoint -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMApplicationCatalogWebServicePoint** cmdlet gets a Microsoft System Center Configuration Manager Application Catalog web service point object that has a specified site code for a fully qualified domain name (FQDN).

Before you can configure an Application Catalog web service point you must first install and configure site system roles in Configuration Manager.
For more information, see [Install and Configure Site System Roles for Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=262649) on TechNet.

## EXAMPLES

### Example 1: Get a system role
```
PS C:\> Get-CMApplicationCatalogWebServicePoint -SiteSystemServerName "western.contoso.com" -SiteCode "CM1"
```

This command gets an Application Catalog web service point named western.contoso.com that has the site code CM1.

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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for an Application Catalog web service point object.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies an FQDN for an Application Catalog web service point.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName
Required: False
Position: 0
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

[Add-CMApplicationCatalogWebServicePoint](xref:ConfigurationManager/vlatest/Add-CMApplicationCatalogWebServicePoint.md)

[Remove-CMApplicationCatalogWebServicePoint](xref:ConfigurationManager/vlatest/Remove-CMApplicationCatalogWebServicePoint.md)


