---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833972
schema: 2.0.0
ms.assetid: 86D6E727-868D-4CAA-9716-7CFEA70AD699
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMOutOfBandServicePoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMOutOfBandServicePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMOutOfBandServicePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMOutOfBandServicePoint

## SYNOPSIS
Changes configuration settings for an out of band service point.

## SYNTAX

### SetByValue (Default)
```
Set-CMOutOfBandServicePoint -InputObject <IResultObject> [-ErrorRetryCount <Int32>]
 [-ErrorRetryMinutesDelay <Int32>] [-TransmissionThreadCount <Int32>] [-TransmissionStartMins <Int32>]
 [-EnableCrlChecking <Boolean>] [-ProvisioningCertificateThumbprint <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMOutOfBandServicePoint [-SiteCode <String>] [-SiteSystemServerName] <String> [-ErrorRetryCount <Int32>]
 [-ErrorRetryMinutesDelay <Int32>] [-TransmissionThreadCount <Int32>] [-TransmissionStartMins <Int32>]
 [-EnableCrlChecking <Boolean>] [-ProvisioningCertificateThumbprint <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMOutOfBandServicePoint** cmdlet changes configuration settings for an out of band service point.
An out of band service point is a site system role that provisions and configures Intel Active Management Technology (AMT)-based computers for Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Change settings of an out of band service point
```
PS C:\> Set-CMOutOfBandServicePoint -SiteSystemServerName "cmcen-dist02.tsqa.contoso.com" -SiteCode "CM2" -ErrorRetryMinutesDelay 1 -TransmissionThreadCount 1 -TransmissionStartMinutesInterval 1 -EnableCrlChecking 1 -ProvisioningCertificateThumbprint "916EC36F1068D47DE48A02A788A9DB137CD0B674"
```

This command changes the settings of the out of band service point from the System Center Configuration Manager site that has the site code named CM2 on the site system named cmcen-dist02.tsqa.contoso.com.

### Example 2: Change settings of an out of band service point by using an object variable
```
PS C:\> $Osp = Get-CMOutOfBandServicePoint -SiteSystemServerName "cmcen-dist02.tsqa.contoso.com" -SiteCode "CM2"
PS C:\> Set-CMOutOfBandServicePoint -InputObject $Osp -ErrorRetryCount 1 -ErrorRetryMinutesDelay 1 -TransmissionThreadCount 1 -TransmissionStartMinutesInterval 1 -EnableCrlChecking 1 -ProvisioningCertificateThumbprint "916EC36F1068D47DE48A02A788A9DB137CD0B674"
```

The first command gets the out of band service point from the System Center Configuration Manager site that has the site code named CM2 on the site system named cmcen-dist02.tsqa.contoso.com.
The command stores the results in the $Osp variable.

The second command changes the settings of the out of band service point stored in the $Osp variable.

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

### -EnableCrlChecking
Indicates whether the out of band service point verifies the certificate revocation list (CRL) for the provisioning certificate.

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

### -ErrorRetryCount
Specifies the number of retry attempts that Configuration Manager makes after it fails to turn on an AMT-based computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumSendRetryCount
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorRetryMinutesDelay
Specifies the number of minutes that Configuration Manager waits between retry attempts to turn on an AMT-based computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RetryIntervalMinutes
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
Specifies a **CMOutOfBandServicePoint** object.
To obtain a **CMOutOfBandServicePoint** object, use the [Get-CMOutOfBandServicePoint](./Get-CMOutOfBandServicePoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: OutOfBandServicePoint
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

### -ProvisioningCertificateThumbprint
Specifies the thumbprint of the AMT provisioning certificate.

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

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

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
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

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

### -TransmissionStartMins


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ThreadsOffset, TransmissionStartMinutesInterval
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TransmissionThreadCount
Specifies the maximum number of connection threads that the site system role supports.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumThreadCount
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

[Get-CMOutOfBandServicePoint](xref:ConfigurationManager/vlatest/Get-CMOutOfBandServicePoint.md)

[Add-CMOutOfBandServicePoint](xref:ConfigurationManager/vlatest/Add-CMOutOfBandServicePoint.md)

[Remove-CMOutOfBandServicePoint](xref:ConfigurationManager/vlatest/Remove-CMOutOfBandServicePoint.md)
