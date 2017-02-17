---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834294
schema: 2.0.0
ms.assetid: D4ADE497-4DDA-48FC-B727-B9FB14494F12
updated_at: 2/17/2017 12:26 AM
ms.date: 2/17/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCertificateProfilePfx.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCertificateProfilePfx.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4e04bc97493f4205ab86f0f52a705ef3d93cb7ea/sccm-cmdlets/ConfigurationManager/vlatest/New-CMCertificateProfilePfx.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMCertificateProfilePfx

## SYNOPSIS
Creates a PFX certificate profile.

## SYNTAX

```
New-CMCertificateProfilePfx [-Description <String>] [-KeyStorageProvider <KeyStorageProviderSettingType>]
 -Name <String> -SupportedPlatform <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCertificateProfilePfx** cmdlet creates a Personal Information Exchange (PFX) certificate profile.

## EXAMPLES

### Example 1: Create a PFX certificate profile
```
PS C:\> New-CMCertificateProfilePfx -Name "TestCertificatieProfilePfx1" -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client")
```

This command creates a PFX certificate profile named TestCertificatieProfilePfx1 for all Windows 10 Client platforms.

### Example 2: Create a PFX certificate profile to install to TPM
```
PS C:\> New-CMCertificateProfilePfx -Name "Test2" -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client") -Description "Test cmcertificationprofilepfx description" -KeyStorageProvider InstallToTPM_IfPresent
```

This command creates a PFX certificate profile named Test2 for all Windows 10 Client platforms and sets the key storage provider to install to TPM, if present.

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
Specifies a description for the PFX certificate profile.

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

### -KeyStorageProvider
Specifies the Key Storage Provider.
Valid values are:

- InstallToTPM_FailIfNotPresent
- InstallToTPM_IfPresent
- InstallToSoftwareKeyStorageProvider
- InstallToNGC_FailIfNotPresent

```yaml
Type: KeyStorageProviderSettingType
Parameter Sets: (All)
Aliases:
Accepted values: None, InstallToTPM_FailIfNotPresent, InstallToTPM_IfPresent, InstallToSoftwareKeyStorageProvider, InstallToNGC_FailIfNotPresent

Required: False
Position: Named
Default value: InstallToTPM_IfPresent
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the PFX certificate profile.

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

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Get-CMCertificateProfilePfx](xref:ConfigurationManager/vlatest/Get-CMCertificateProfilePfx.md)

[Get-CMSupportedPlatform](xref:ConfigurationManager/vlatest/Get-CMSupportedPlatform.md)

[Set-CMCertificateProfilePfx](xref:ConfigurationManager/vlatest/Set-CMCertificateProfilePfx.md)
