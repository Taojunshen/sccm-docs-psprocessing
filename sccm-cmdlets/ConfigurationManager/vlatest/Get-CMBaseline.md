---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834130
schema: 2.0.0
ms.assetid: C01E6314-2F4A-4D25-B420-F73CA7F48CBD
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMBaseline.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMBaseline.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMBaseline.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMBaseline

## SYNOPSIS
Gets configuration baselines.

## SYNTAX

### SearchByName (Default)
```
Get-CMBaseline [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBaseline [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByParentBaselineIdMandatory
```
Get-CMBaseline -ParentBaselineId <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByParentBaselineNameMandatory
```
Get-CMBaseline -ParentBaselineName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByParentBaseline
```
Get-CMBaseline [-ParentBaseline] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBaseline** cmdlet gets one or more configuration baselines.

## EXAMPLES

### Example 1: Get configuration baselines by using a parent baseline name
```
PS C:\> Get-CMBaseline -ParentBaselineName "ParentBaselineContoso01"
```

This command gets the child configuration baselines in the parent baseline configuration item named ParentBaselineContoso01.

### Example 2: Get configuration baselines by using a parent baseline ID
```
PS C:\> Get-CMBaseline -ParentBaselineId "16777357"
```

This command gets the child configuration baselines in the parent baseline configuration item that has the identity 16777357.

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

### -Id
Specifies an array of IDs of configuration baselines.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration baselines.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName
Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentBaseline
Specifies a **CMParentBaseline** object.

```yaml
Type: IResultObject
Parameter Sets: SearchByParentBaseline
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentBaselineId
Specifies the ID of a parent baseline object.

```yaml
Type: Int32
Parameter Sets: SearchByParentBaselineIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentBaselineName
Specifies the name of a parent baseline.

```yaml
Type: String
Parameter Sets: SearchByParentBaselineNameMandatory
Aliases: 
Required: True
Position: Named
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

[Disable-CMBaseline](xref:ConfigurationManager/vlatest/Disable-CMBaseline.md)

[Enable-CMBaseline](xref:ConfigurationManager/vlatest/Enable-CMBaseline.md)

[Export-CMBaseline](xref:ConfigurationManager/vlatest/Export-CMBaseline.md)

[Import-CMBaseline](xref:ConfigurationManager/vlatest/Import-CMBaseline.md)

[New-CMBaseline](xref:ConfigurationManager/vlatest/New-CMBaseline.md)

[Remove-CMBaseline](xref:ConfigurationManager/vlatest/Remove-CMBaseline.md)

[Set-CMBaseline](xref:ConfigurationManager/vlatest/Set-CMBaseline.md)

[Get-CMBaselineSummarizationSchedule](xref:ConfigurationManager/vlatest/Get-CMBaselineSummarizationSchedule.md)


