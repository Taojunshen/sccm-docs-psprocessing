---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834043
schema: 2.0.0
ms.assetid: AC569305-8C8B-4A6A-9BE8-4AC78003A7E9
updated_at: 2/17/2017 12:26 AM
ms.date: 2/17/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMClientCertificatePfx.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMClientCertificatePfx.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/4e04bc97493f4205ab86f0f52a705ef3d93cb7ea/sccm-cmdlets/ConfigurationManager/vlatest/Import-CMClientCertificatePfx.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Import-CMClientCertificatePfx

## SYNOPSIS
Imports a client PFX certificate.

## SYNTAX

```
Import-CMClientCertificatePfx -Path <String> -UserName <String> [-Password <SecureString>]
 -CertificateProfilePfx <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMClientCertificatePfx** cmdlet imports a client Personal Information Exchange (PFX) certificate to a site server.

## EXAMPLES

### Example 1: Import a client PFX certificate
```
PS C:\> Import-CMClientCertificatePfx -Path "\\server\ShareFolder\test.pfx" -UserName (Get-CMUser -Name "Contoso\Administrator").SMSID -Password (ConvertTo-SecureString -String "sccm" -AsPlainText -Force) -CertificateProfilePfx (Get-CMCertificateProfilePfx -Name "CertTest" -Fast )
```

This command imports a client PFX certificate for the user named administrator.

## PARAMETERS

### -CertificateProfilePfx
Specifies a PFX certificate profile object.
To obtain a PFX certificate profile object, use the Get-CMCertificateProfilePfx cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Password
Specifies, as a secure string, the password that allows access to the imported PFX certificate.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the path of the client PFX certificate.

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

### -UserName
Specifies the user that the imported PFX certificate targets.
To get the user value, you can use the following command: `(get-cmuser -name domain\username).SMSID`.

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

### IResultObject#SMS_ClientPfxCertificate

## NOTES

## RELATED LINKS

[Get-CMCertificateProfilePfx](xref:ConfigurationManager/vlatest/Get-CMCertificateProfilePfx.md)

[Get-CMClientCertificatePfx](xref:ConfigurationManager/vlatest/Get-CMClientCertificatePfx.md)

[Get-CMUser](xref:ConfigurationManager/vlatest/Get-CMUser.md)

[Remove-CMClientCertificatePfx](xref:ConfigurationManager/vlatest/Remove-CMClientCertificatePfx.md)
