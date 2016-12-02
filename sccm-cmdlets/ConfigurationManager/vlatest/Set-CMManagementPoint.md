---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833919
schema: 2.0.0
ms.assetid: 5687A04C-C8E3-4902-A157-FC5807D7BFF9
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMManagementPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMManagementPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMManagementPoint

## SYNOPSIS
Changes settings for a management point in Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMManagementPoint -InputObject <IResultObject> [-EnableSsl <Boolean>]
 [-ClientConnectionType <ClientConnectionTypes>] [-AllowDevice <Boolean>] [-GenerateAlert <Boolean>]
 [-UseSiteDatabase <Boolean>] [-SqlServerFqdnName <String>] [-SqlServerInstanceName <String>]
 [-DatabaseName <String>] [-UserName <String>] [-UseComputerAccount] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMManagementPoint [-SiteSystemServerName] <String> [-SiteCode <String>] [-EnableSsl <Boolean>]
 [-ClientConnectionType <ClientConnectionTypes>] [-AllowDevice <Boolean>] [-GenerateAlert <Boolean>]
 [-UseSiteDatabase <Boolean>] [-SqlServerFqdnName <String>] [-SqlServerInstanceName <String>]
 [-DatabaseName <String>] [-UserName <String>] [-UseComputerAccount] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMManagementPoint** cmdlet changes settings for a management point in Microsoft System Center Configuration Manager.
A management point is a System Center Configuration Manager site that provides policy and service information to clients and receives configuration data from clients.

## EXAMPLES

### Example 1: Change management point settings for site system and site code
```
PS C:\>Set-CMManagementPoint -SiteSystemServerName "CMDEV-TEST02.TSQA.CORP.CONTOSO.COM" -SiteCode "CM2" -EnableSSL $False -UseSiteDatabase $True
```

This command changes settings for a management point in a Configuration Manager installation.
The command specifies the following information about the management point: 

- The new management point appears on the site system named CMDEV-TEST02.TSQA.CONTOSO.COM.
- The site has code CM2.
- The management point queries a site database for information. 
- The command enables SSL for the management point.

### Example 2: Change management point settings for site system and site code, connection type, and database name
```
PS C:\>Set-CMManagementPoint -SiteSystemServerName "CMDEV-TEST02.TSQA.CORP.CONTOSO.COM " -SiteCode "CM2" -ClientConnectionType InternetAndIntranet -AllowDevice $True -EnableSSL $True -GenerateAlert $False -UseSiteDatabase $False -SQLServerFqdnName "CMDEV-TEST02.TSQA.CORP.CONTOSO.COM" -SQLServerInstanceName "MSSQLServer" -DatabaseName "ContosoSQL01"
```

This command changes settings for a management point in a Configuration Manager installation.
The command specifies the following information about the management point: 

- The new management point appears on the site system named CMDEV-TEST02.TSQA.CONTOSO.COM.
This name is also the fully qualified domain name for the SQL Server instance named MSSQLServer.
- The site has code CM2.
- The management point accepts connections from Internet and intranet clients and from portable devices. 
- The management point has the associated database name ContosoSQL01. 
- The command enables SSL for the management point.

## PARAMETERS

### -AllowDevice
Indicates whether the management point supports device clients.

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

### -ClientConnectionType
Specifies the type of the client connection.
The acceptable values for this parameter are:

- Internet
- InternetAndIntranet
- Intranet

```yaml
Type: ClientConnectionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Internet, Intranet, InternetAndIntranet

Required: False
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

### -DatabaseName
Specifies the name of the site database or site database replica that the management point uses to query for site database information.

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

### -EnableSsl
Indicates whether to enable SSL.

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

### -GenerateAlert
Indicates whether the management point generates health alerts.

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

### -InputObject
Specifies the management point for which you change values by using a management point object.
To obtain a management point object, use the Get-CMManagementPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: ManagementPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -SiteCode
Specifies the site code of the System Center Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlServerFqdnName
Specifies the server name of the site database or site database replica that the management point uses to query for site database information.
You must specify this parameter if Internet-based client systems communicate with the site system.

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

### -SqlServerInstanceName
Specifies the name of the SQL Server instance that clients use to communicate with the site system.

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

### -UseComputerAccount
Indicates that the management point uses its own computer account instead of a domain user account to access site database information.

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

### -UseSiteDatabase
Indicates whether the management point queries a site database instead of a site database replica for information.

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

### -UserName
Specifies a domain user account that the management point uses to access site information.

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

[Add-CMManagementPoint](xref:ConfigurationManager/vlatest/Add-CMManagementPoint.md)

[Get-CMManagementPoint](xref:ConfigurationManager/vlatest/Get-CMManagementPoint.md)

[Remove-CMManagementPoint](xref:ConfigurationManager/vlatest/Remove-CMManagementPoint.md)


