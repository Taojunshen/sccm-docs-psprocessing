---
external help file: AdminUI.PS.Dcm-help.xml
ms.assetid: E45BED4A-8286-46FF-A3F1-4E54B7D77F90
online version: https://go.microsoft.com/fwlink/?linkid=834170
schema: 2.0.0
updated_at: 3/15/2017 9:36 PM
ms.date: 3/15/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificateProfileScep.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificateProfileScep.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/cada5695dfea912d5e249f0f0da4d1b9f2169f8d/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCertificateProfileScep.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMCertificateProfileScep

## SYNOPSIS
Gets a SCEP certificate profile.

## SYNTAX

### ByValue (Default)
```
Get-CMCertificateProfileScep [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMCertificateProfileScep [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMCertificateProfileScep [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificateProfileScep** function gets a SCEP certificate profile.

## EXAMPLES

### Example 1: Get a SCEP certificate profile by ID
```
PS C:\> Get-CMcertificateProfileScep -Id 16777476
```

This command gets the SCEP certificate profile with the ID of 16777476.

### Example 2: Get a SCEP certificate profile by name
```
PS C:\> Get-CMCertificateProfileScep -Name "TestSCEPProfile"
```

This command gets the SCEP certificate profile with the name TestSCEPProfile.

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
Specifies the CI_ID of a SCEP certificate profile.

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
Specifies the name of a SCEP certificate profile.

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

[New-CMCertificateProfileScep](xref:ConfigurationManager/vlatest/New-CMCertificateProfileScep.md)

[Set-CMCertificateProfileScep](xref:ConfigurationManager/vlatest/Set-CMCertificateProfileScep.md)


