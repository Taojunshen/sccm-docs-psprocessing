---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834301
schema: 2.0.0
ms.assetid: 621AC1DA-C4DB-4559-90BF-B6EAEB9560D3
updated_at: 2/17/2017 12:26 AM
ms.date: 2/17/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCertificateProfileTrustedRootCA.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCertificateProfileTrustedRootCA.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4e04bc97493f4205ab86f0f52a705ef3d93cb7ea/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCertificateProfileTrustedRootCA.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMCertificateProfileTrustedRootCA

## SYNOPSIS
Creates a trusted CA certificate profile.

## SYNTAX

```
New-CMCertificateProfileTrustedRootCA [-Description <String>] [-DestinationStore <CertificateStore>]
 -Name <String> -Path <String> -SupportedPlatform <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCertificateProfileTrustedRootCA** cmdlet creates a trusted certification authority (CA) certificate profile.

## EXAMPLES

### Example 1: Create a trusted CA certificate profile
```
PS C:\> New-CMCertificateProfileTrustedRootCA -Name "Test01" -Path "\\Server01\ShareFolder\RootCA.cer" -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client")
```

This command creates a trusted CA certificate profile named Test01 from the RootCA.cer certificate for all Windows 10 Client platforms.

### Example 2: Create a trusted CA certificate profile and set the destination store
```
PS C:\> New-CMCertificateProfileTrustedRootCA -Name "Test02" -Path \\Server01\ShareFolder\RootCA.cer -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client") -Description "TestRootCertificate" -DestinationStore SystemIntermediate
```

This command creates a trusted CA certificate profile named Test02 from the RootCA.cer certificate for all Windows 10 Client platforms.
Additionally, the command sets the destination store to Computer certificate store - Intermediate.

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
Specifies a description for the trusted CA certificate profile.

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

### -DestinationStore
Specifies the destination store for the trusted CA certificate.
Valid values are:

- SystemRoot
- SystemIntermediate
- UserIntermediate

```yaml
Type: CertificateStore
Parameter Sets: (All)
Aliases: Store
Accepted values: SystemRoot, SystemIntermediate, UserIntermediate

Required: False
Position: Named
Default value: SystemRoot
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

### -Name
Specifies a name for the trusted CA certificate profile.

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

### -Path
Specifies the path to the trusted CA certificate file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificatePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportedPlatform
Specifies a supported platform object.
To obtain a supported platform object, use the Get-CMSupportedPlatform cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SupportedPlatforms

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

[Get-CMCertificateProfileTrustedRootCA](xref:ConfigurationManager/vlatest/Get-CMCertificateProfileTrustedRootCA.md)

[Get-CMSupportedPlatform](xref:ConfigurationManager/vlatest/Get-CMSupportedPlatform.md)

[Set-CMCertificateProfileTrustedRootCA](xref:ConfigurationManager/vlatest/Set-CMCertificateProfileTrustedRootCA.md)
