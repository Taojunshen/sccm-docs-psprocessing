---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834181
schema: 2.0.0
ms.assetid: F27EC489-FE2F-4E0B-A376-2C3DF975E044
updated_at: 3/8/2017 3:12 AM
ms.date: 3/8/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMClientCertificatePfx.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMClientCertificatePfx.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/084a840c19ff550066f775fa8796b32e3bfaeb1d/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMClientCertificatePfx.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMClientCertificatePfx

## SYNOPSIS
Gets a client PFX certificate.

## SYNTAX

```
Get-CMClientCertificatePfx [-UserName <String>] [-Thumbprint <String>] [-InputObject <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientCertificatePfx** cmdlet gets a client Personal Information Exchange (PFX) certificate.

## EXAMPLES

### Example 1: Get a client PFX certificate
```
PS C:\> Get-CMClientCertificatePfx -UserName (Get-CMUser -Name "Contoso\Administrator").SMSID -Thumbprint  e1c2fff14282b61f79f78fbfca6721f0517ab767
```

This command gets the Pfx client certificate for the user named Administrator with the specified thumbprint.

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
Specifies a PFX certificate profile object.
To obtain a PFX certificate profile object, use the Get-CMCertificateProfilePfx cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: CertificateProfilePfx

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Thumbprint
Specifies the thumbprint of the client PFX certificate. If you do not specify this parameter, all certificates for the user are returned.

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

### -UserName
Specifies the name of the user whose client PFX certificate you want to get.
To get a value for this parameter, you can use the following command: `(Get-CMUser -Name "Contoso\Administrator").SMSID`.

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

### IResultObject#SMS_ClientPfxCertificate

## NOTES

## RELATED LINKS

[Get-CMCertificateProfilePfx](xref:ConfigurationManager/vlatest/Get-CMCertificateProfilePfx.md)

[Get-CMUser](xref:ConfigurationManager/vlatest/Get-CMUser.md)

[Import-CMClientCertificatePfx](xref:ConfigurationManager/vlatest/Import-CMClientCertificatePfx.md)

[Remove-CMClientCertificatePfx](xref:ConfigurationManager/vlatest/Remove-CMClientCertificatePfx.md)
