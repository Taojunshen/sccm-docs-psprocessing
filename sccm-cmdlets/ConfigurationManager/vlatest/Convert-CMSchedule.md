---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833868
schema: 2.0.0
ms.assetid: 8D8F8DC3-4AC4-417A-BA50-30E81D02EE6E
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Convert-CMSchedule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Convert-CMSchedule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Convert-CMSchedule

## SYNOPSIS
Converts schedule tokens into and from interval strings.

## SYNTAX

### ByToken (Default)
```
Convert-CMSchedule [-ScheduleToken] <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByString
```
Convert-CMSchedule [-ScheduleString] <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Convert-CMSchedule** cmdlet decodes and encodes schedule tokens into and from Microsoft System Center Configuration Manager interval strings.

## EXAMPLES

### Example 1: Convert a schedule string
```
PS C:\>Convert-CMSchedule -ScheduleString "02C159C0381A200002C159C0381B200002C159C0381C200002C159C0381D200002C159C0381E2000"
```

This command converts a schedule string into a schedule token.

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

### -ScheduleString
Specifies an array of interval strings.

```yaml
Type: String[]
Parameter Sets: ByString
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleToken
Specifies an array of Configuration Manager schedule objects output from another cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: ByToken
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMClientStatusUpdateSchedule](xref:ConfigurationManager/vlatest/Get-CMClientStatusUpdateSchedule.md)

[Get-CMBaselineSummarizationSchedule](xref:ConfigurationManager/vlatest/Get-CMBaselineSummarizationSchedule.md)

[Get-CMOperatingSystemImageUpdateSchedule](xref:ConfigurationManager/vlatest/Get-CMOperatingSystemImageUpdateSchedule.md)

[Get-CMEndpointProtectionSummarizationSchedule](xref:ConfigurationManager/vlatest/Get-CMEndpointProtectionSummarizationSchedule.md)

[Get-CMSoftwareUpdateSummarizationSchedule](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdateSummarizationSchedule.md)

[New-CMSchedule](xref:ConfigurationManager/vlatest/New-CMSchedule.md)


