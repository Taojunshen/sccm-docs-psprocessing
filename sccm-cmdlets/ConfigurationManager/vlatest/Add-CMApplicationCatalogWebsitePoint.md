---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833586
schema: 2.0.0
ms.assetid: E45EF36A-ED49-4B86-B635-B299D124D14B
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMApplicationCatalogWebsitePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Add-CMApplicationCatalogWebsitePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Add-CMApplicationCatalogWebsitePoint

## SYNOPSIS
Adds an Application Catalog website point to a Configuration Manager site.

## SYNTAX

### AppWebSitePointByValue (Default)
```
Add-CMApplicationCatalogWebsitePoint [-IisWebsite <String>] [-WebApplicationName <String>]
 [-NetBiosName <String>] [-OrganizationName <String>] -ApplicationWebServicePointServerName <String> [-Http]
 [-Port <Int32>] [-ColorRed <Int32>] [-ColorGreen <Int32>] [-ColorBlue <Int32>] [-Color <Color>]
 [-ClientConnectionType <ClientConnectionTypes>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AppWebSitePointWithSsl
```
Add-CMApplicationCatalogWebsitePoint [-IisWebsite <String>] [-WebApplicationName <String>]
 [-NetBiosName <String>] [-OrganizationName <String>] [-SiteSystemServerName] <String> [-SiteCode <String>]
 -ApplicationWebServicePointServerName <String> [-Https] [-Port <Int32>] [-ColorRed <Int32>]
 [-ColorGreen <Int32>] [-ColorBlue <Int32>] [-Color <Color>] [-ClientConnectionType <ClientConnectionTypes>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AppWebSite
```
Add-CMApplicationCatalogWebsitePoint [-IisWebsite <String>] [-WebApplicationName <String>]
 [-NetBiosName <String>] [-OrganizationName <String>] [-SiteSystemServerName] <String> [-SiteCode <String>]
 -ApplicationWebServicePointServerName <String> -CommunicationType <ComputerCommunicationType> [-Port <Int32>]
 [-ColorRed <Int32>] [-ColorGreen <Int32>] [-ColorBlue <Int32>] [-Color <Color>]
 [-ClientConnectionType <ClientConnectionTypes>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### AppWebSitePoint
```
Add-CMApplicationCatalogWebsitePoint [-IisWebsite <String>] [-WebApplicationName <String>]
 [-NetBiosName <String>] [-OrganizationName <String>] [-SiteSystemServerName] <String> [-SiteCode <String>]
 -ApplicationWebServicePointServerName <String> [-Http] [-Port <Int32>] [-ColorRed <Int32>]
 [-ColorGreen <Int32>] [-ColorBlue <Int32>] [-Color <Color>] [-ClientConnectionType <ClientConnectionTypes>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AppWebSitePointWithSslByValue
```
Add-CMApplicationCatalogWebsitePoint [-IisWebsite <String>] [-WebApplicationName <String>]
 [-NetBiosName <String>] [-OrganizationName <String>] -ApplicationWebServicePointServerName <String> [-Https]
 [-Port <Int32>] [-ColorRed <Int32>] [-ColorGreen <Int32>] [-ColorBlue <Int32>] [-Color <Color>]
 [-ClientConnectionType <ClientConnectionTypes>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AppWebSiteByValue
```
Add-CMApplicationCatalogWebsitePoint [-IisWebsite <String>] [-WebApplicationName <String>]
 [-NetBiosName <String>] [-OrganizationName <String>] -ApplicationWebServicePointServerName <String>
 -CommunicationType <ComputerCommunicationType> [-Port <Int32>] [-ColorRed <Int32>] [-ColorGreen <Int32>]
 [-ColorBlue <Int32>] [-Color <Color>] [-ClientConnectionType <ClientConnectionTypes>]
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMApplicationCatalogWebsitePoint** cmdlet adds an Application Catalog website point to a Microsoft System Center Configuration Manager site.
This site system role supports the Application Catalog website and the Software Library.

Specify the site that this website point supports and the server that hosts the website point.
You can specify the website name and NetBIOS name of the Application Catalog.
You can also specify port numbers for HTTP and HTTPS.

You can customize the page that users see when they connect to the Application Catalog.
Specify custom values for the colors blue, green, and red.
You can also specify a name for users to see in the browser, such as a company name or a division within a company.

## EXAMPLES

### Example 1: Add an Application Catalog website point
```
PS C:\>Add-CMApplicationCatalogWebsitePoint -ColorBlue 52 -ColorGreen 201 -ColorRed 168 -SiteCode "CM4" -SiteSystemServerName "ApplicationCatalog.Western.Contoso.com"
```

This command adds an Application Catalog website point site system role for the site that has the site code CM4.
A server named ApplicationCatalog.Western.Contoso.com hosts the website point.
The command specifies values for the three colors.

## PARAMETERS

### -ApplicationWebServicePointServerName


```yaml
Type: String
Parameter Sets: (All)
Aliases: SiteSystemServerNameConfiguredForApplicationCatalogWebServicePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientConnectionType


```yaml
Type: ClientConnectionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Intranet, Internet, InternetAndIntranet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Color


```yaml
Type: Color
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ColorBlue


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ColorGreen


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ColorRed


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommunicationType


```yaml
Type: ComputerCommunicationType
Parameter Sets: AppWebSite, AppWebSiteByValue
Aliases: ClientCommunicationType
Accepted values: Http, Https

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

### -Http


```yaml
Type: SwitchParameter
Parameter Sets: AppWebSitePointByValue, AppWebSitePoint
Aliases: ConfiguredAsHttpConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Https


```yaml
Type: SwitchParameter
Parameter Sets: AppWebSitePointWithSsl, AppWebSitePointWithSslByValue
Aliases: ConfiguredAsHttpsConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IisWebsite


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

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: AppWebSitePointByValue, AppWebSitePointWithSslByValue, AppWebSiteByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NetBiosName


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

### -OrganizationName


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

### -Port


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PortForHttpConnection, PortForHttpsConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode


```yaml
Type: String
Parameter Sets: AppWebSitePointWithSsl, AppWebSite, AppWebSitePoint
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
Parameter Sets: AppWebSitePointWithSsl, AppWebSite, AppWebSitePoint
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplicationName


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

[Get-CMApplicationCatalogWebsitePoint](xref:ConfigurationManager/vlatest/Get-CMApplicationCatalogWebsitePoint.md)

[Remove-CMApplicationCatalogWebSitePoint](xref:ConfigurationManager/vlatest/Remove-CMApplicationCatalogWebSitePoint.md)

[Set-CMApplicationCatalogWebsitePoint](xref:ConfigurationManager/vlatest/Set-CMApplicationCatalogWebsitePoint.md)


