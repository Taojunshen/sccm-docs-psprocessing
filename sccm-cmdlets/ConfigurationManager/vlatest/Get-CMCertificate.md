---
external help file: AdminUI.PS.Certificates.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834161
schema: 2.0.0
ms.assetid: 20865371-37E6-4090-9921-E2051D26D873
updated_at: 3/16/2017 10:23 PM
ms.date: 3/16/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificate.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificate.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/878d763dc5aa42ef726c148331bcba954cf6773e/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificate.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMCertificate

## SYNOPSIS
Gets a certificate.

## SYNTAX

```
Get-CMCertificate [-Id <String>] [-Thumbprint <String>] [-CertificateType <CertificateType>]
 [-KeyType <KeyType>] [-Fast] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificate** cmdlet gets a certificate.

## EXAMPLES

### Example 1:
```
PS ABC:\> Get-CMCertificate
```

This command gets all certificates.

### Example 2:
```
PS ABC:\> Get-CMCertificate -Id "{4680a1bb-ae51-4bdf-8f27-979eb49e444e}" -Thumbprint e1c2fff14282b61f79f78fbfca6721f0517ab767 -CertificateType DistributionPoint -KeyType SelfSigned
```

This command gets the self-signed distribution point certificate with the specified ID and thumbprint.

## PARAMETERS

### -CertificateType
Specifies the certificate type.
Valid values are:

- BootMedia
- DistributionPoint
- IsvProxy

```yaml
Type: CertificateType
Parameter Sets: (All)
Aliases:
Accepted values: BootMedia, DistributionPoint, IsvProxy

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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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

### -Id
Specifies the ID of a certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SmsId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyType
Specifies the key type of the certificate.
Valid values are:

- SelfSigned
- Issued

```yaml
Type: KeyType
Parameter Sets: (All)
Aliases:
Accepted values: SelfSigned, Issued

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Thumbprint
Specifies the thumbprint of the certificate.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Import-CMCertificate](xref:ConfigurationManager/vlatest/Import-CMCertificate.md)

[Update-CMCertificate](xref:ConfigurationManager/vlatest/Update-CMCertificate.md)

[Block-CMCertificate](xref:ConfigurationManager/vlatest/Block-CMCertificate.md)

[Unblock-CMCertificate](xref:ConfigurationManager/vlatest/Unblock-CMCertificate.md)
