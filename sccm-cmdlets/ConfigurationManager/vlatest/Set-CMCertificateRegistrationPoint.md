---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833707
schema: 2.0.0
ms.assetid: 37602013-704A-4D5E-8EFF-BA9F722FBD0A
updated_at: 2/17/2017 12:26 AM
ms.date: 2/17/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMCertificateRegistrationPoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMCertificateRegistrationPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4e04bc97493f4205ab86f0f52a705ef3d93cb7ea/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMCertificateRegistrationPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMCertificateRegistrationPoint

## SYNOPSIS
Sets a certificate registration point role on a site system server.

## SYNTAX

### SetByValue
```
Set-CMCertificateRegistrationPoint [-AddCertificate <Hashtable>] [-ConnectionAccountUserName <String>]
 -InputObject <IResultObject> [-PassThru] [-Port <Int32>] [-RemoveCertificate <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCertificateRegistrationPoint [-AddCertificate <Hashtable>] [-ConnectionAccountUserName <String>]
 [-PassThru] [-Port <Int32>] [-RemoveCertificate <String[]>] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCertificateRegistrationPoint** cmdlet updates the settings of a certificate registration point role on a site system server.

## EXAMPLES

### Example 1: Set a certificate registration point role by using the pipeline
```
PS C:\> Get-CMCertificateRegistrationPoint -SiteSystemServerName "SiteServer01.Contoso.com" | Set-CMCertificateRegistrationPoint  -AddCertificate @{"https://ndes2.fabrikam.com/certsrv/mscep/mscep.dll" ="\\Server\ShareFolder\Cert.cer"} -ConnectionAccountUserName (Get-CMUser -Name Contoso\Administrator).UserName -RemoveCertificate @{"https://ndes1.fabrikam.com/certsrv/mscep/mscep.dll"="\\Server\ShareFolder\RootCA.cer"}.Keys[0]
```

This command gets the certificate registration point object for the site system server named SiteServer01.Contoso.com and uses the pipeline operator to pass the object to **Set-CMCertificateRegistrationPoint**.
**Set-CMCertificateRegistrationPoint** adds the certificate named Cert.cer and removes the certificate named RootCA.cer by using the user account named Contoso\Administrator to connect to the Configuration Manager database.

### Example 2: Set a certificate registration point role by name
```
PS C:\> Set-CMCertificateRegistrationPoint -SiteSystemServerName "SiteServer02.Contoso.com" -AddCertificate @{"https://ndes2.fabrikam.com/certsrv/mscep/mscep.dll"="\\Server\ShareFolder\RootCA.cer"} -ConnectionAccountUserName (Get-CMUser -Name Contoso\Admin1).UserName -RemoveCertificate @{"https://ndes1.fabrikam.com/certsrv/mscep/mscep.dll" ="\\Server\ShareFolder\Cert.cer"}.Keys[0]
```

This command adds the certificate named RootCA.cer to the site system server named SiteServer02.Contoso.com, and removes the certificate named Cert.cer, by using the user account named Contoso\Admin1 to connect to the Configuration Manager database.

## PARAMETERS

### -AddCertificate
Specifies, as a hash table, the URL for the Network Device Enrollment Service and the root CA certificate.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: AddCertificates

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

### -ConnectionAccountUserName
Specifies the account that connects the certification registration point to the Configuration Manger database.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserName

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
Specifies a certification registration point object.
To obtain a certificate registration point object, use the Get-CMCertificateRegistrationPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: CertificateRegistrationPoint

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

### -Port
Specifies the HTTPS port number used by the certificate registration point to communicate with the Network Device Enrollment Service.

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

### -RemoveCertificate
Specifies an array of URLs that match corresponding certificates in the original object.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveCertificates, RemoveCertificateUrl, RemoveCertificateUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site server.

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
Specifies the name of the Configuration Manager site system server.

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

[Add-CMCertificateRegistrationPoint](xref:ConfigurationManager/vlatest/Add-CMCertificateRegistrationPoint.md)

[Get-CMCertificateRegistrationPoint](xref:ConfigurationManager/vlatest/Get-CMCertificateRegistrationPoint.md)

[Remove-CMCertificateRegistrationPoint](xref:ConfigurationManager/vlatest/Remove-CMCertificateRegistrationPoint.md)
