---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833890
schema: 2.0.0
ms.assetid: 346AC378-4A7D-4F06-BE42-EBB231762E27
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMIntuneSubscriptionAppleProperty.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMIntuneSubscriptionAppleProperty.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMIntuneSubscriptionAppleProperty.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMIntuneSubscriptionAppleProperty

## SYNOPSIS
Updates a Microsoft Intune subscription to enable iOS and Mac OS X (MDM) enrollment.

## SYNTAX

```
Set-CMIntuneSubscriptionAppleProperty [-Enable <Boolean>] [-ApnsCertificatePath <String>]
 [-ApnsCertificatePassword <SecureString>] [-CertificateExpiryAlertDays <Int32>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscriptionAppleProperty** cmdlet updates the settings of a Microsoft Intune subscription to enable iOS and Mac OS X (MDM) enrollment.

## EXAMPLES

### Example 1: Enable iOS and Mac OS X (MDM) enrollment
```
PS C:\> Set-CMIntuneSubscriptionAppleProperty -Enable $True -ApnsCertificatePath "C:\Certs\test.pem" -ApnsCertificatePassword $null -CertificateExpiryAlertDays 30
```

This command enables iOS and Mac OS X (MDM) enrollment for the Microsoft Intune subscription.

## PARAMETERS

### -ApnsCertificatePassword
Specifies, as a secure string, the password for the APNs certificate.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: CertificatePassword
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApnsCertificatePath
Specifies the path to the Apple Push Notification service (APNs) certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path, CertificatePath
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateExpiryAlertDays
Specifies the number of days before the APNs certificate expires to show an alert.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ApnsCertificateExpiryAlertDays
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

### -Enable
Indicates whether iOS and Mac OS X (MDM) enrollment is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Enabled, EnableIosEnrollment, EnableMacEnrollment, EnableMdmEnrollment
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

[Set-CMIntuneSubscriptionAndroidProperty](xref:ConfigurationManager/vlatest/Set-CMIntuneSubscriptionAndroidProperty.md)

[Set-CMIntuneSubscriptionAppleDepProperty](xref:ConfigurationManager/vlatest/Set-CMIntuneSubscriptionAppleDepProperty.md)

[Set-CMIntuneSubscriptionPassportForWorkProperty](xref:ConfigurationManager/vlatest/Set-CMIntuneSubscriptionPassportForWorkProperty.md)

[Set-CMIntuneSubscriptionWindowsPhoneProperty](xref:ConfigurationManager/vlatest/Set-CMIntuneSubscriptionWindowsPhoneProperty.md)

[Set-CMIntuneSubscriptionWindowsProperty](xref:ConfigurationManager/vlatest/Set-CMIntuneSubscriptionWindowsProperty.md)


