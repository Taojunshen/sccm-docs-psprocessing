---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833946
schema: 2.0.0
ms.assetid: 465F235A-C884-464E-8894-8992FB3B4874
updated_at: 2/17/2017 8:44 PM
ms.date: 2/17/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMCertificateRegistrationPoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMCertificateRegistrationPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/856ffc1e46b17afe4598fc0b1014e210c0bfa796/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMCertificateRegistrationPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMCertificateRegistrationPoint

## SYNOPSIS
Removes a certificate registration point role from a site system server.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMCertificateRegistrationPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMCertificateRegistrationPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMCertificateRegistrationPoint** cmdlet removes a certificate registration point role from a site system server.

## EXAMPLES

### Example 1: Remove a certificate registration point role by using the pipeline
```
PS C:\> Get-CMCertificateRegistrationPoint -SiteSystemServerName "SiteSystemserver01.Contoso.com" | Remove-CMCertificateRegistrationPoint -Force
```

This command gets the certificate registration point object for the site system server named SiteSystemserver01.Contoso.com and uses the pipeline operator to pass the object to **Remove-CMCertificateRegistrationPoint**, which removes the certificate registration point.
The command does not prompt the user for confirmation.

### Example 2: Remove a certificate registration point role by name
```
PS C:\> Remove-CMCertificateRegistrationPoint -SiteSystemServerName "SiteSystemserver02.Contoso.com"
```

This command removes the certificate registration point from the site system server named SiteSystemserver02.Contoso.com.

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

### -Force
Forces the command to run without asking for user confirmation.

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
Specifies a certificate registration point role object.
To obtain a certificate registration point role object, use the Get-CMCertificateRegistrationPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: CertificateRegistrationPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site server.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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
Parameter Sets: SearchByNameMandatory
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

[Set-CMCertificateRegistrationPoint](xref:ConfigurationManager/vlatest/Set-CMCertificateRegistrationPoint.md)


