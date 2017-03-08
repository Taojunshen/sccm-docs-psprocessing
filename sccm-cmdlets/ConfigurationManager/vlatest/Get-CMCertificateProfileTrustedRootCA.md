---
external help file: AdminUI.PS.Dcm-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834174
schema: 2.0.0
ms.assetid: B0351D61-35E9-42F7-BD61-DDB7A66039A3
updated_at: 2/17/2017 8:44 PM
ms.date: 2/17/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificateProfileTrustedRootCA.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificateProfileTrustedRootCA.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/856ffc1e46b17afe4598fc0b1014e210c0bfa796/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificateProfileTrustedRootCA.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMCertificateProfileTrustedRootCA

## SYNOPSIS
Gets a trusted CA certificate profile.

## SYNTAX

### ByValue (Default)
```
Get-CMCertificateProfileTrustedRootCA [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMCertificateProfileTrustedRootCA [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMCertificateProfileTrustedRootCA [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificateProfileTrustedRootCA** function gets a trusted CA certificate profile.

## EXAMPLES

### Example 1: Get a trusted CA certificate profile by ID
```
PS C:\> Get-CMCertificateProfileTrustedRootCA -Id 16777479
```

This command gets the trusted CA certificate profile with the ID 16777479.

### Example 2: Get a trusted CA certificate profile by name
```
PS C:\> Get-CMCertificateProfileTrustedRootCA -Name "Test01" -Fast
```

This command gets the trusted CA certificate profile named Test01, but does not return lazy properties.

## PARAMETERS

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

### -Id
Specifies the ID of a trusted CA certificate profile.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a trusted CA certificate profile.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
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

[New-CMCertificateProfileTrustedRootCA](xref:ConfigurationManager/vlatest/New-CMCertificateProfileTrustedRootCA.md)

[Set-CMCertificateProfileTrustedRootCA](xref:ConfigurationManager/vlatest/Set-CMCertificateProfileTrustedRootCA.md)


