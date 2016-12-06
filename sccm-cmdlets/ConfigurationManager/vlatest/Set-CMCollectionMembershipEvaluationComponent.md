---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833744
schema: 2.0.0
ms.assetid: DC548AD7-17F7-4455-8857-6342043439FA
updated_at: 12/5/2016 10:55 PM
ms.date: 12/5/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMCollectionMembershipEvaluationComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/f95cf139be40af870257194c70c82183d89f7a0c/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMCollectionMembershipEvaluationComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMCollectionMembershipEvaluationComponent

## SYNOPSIS
Sets how often Configuration Manager evaluates collections for membership.

## SYNTAX

```
Set-CMCollectionMembershipEvaluationComponent [-SiteSystemServerName <String>] [-SiteCode <String>]
 -EvaluationMins <Int32> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCollectionMembershipEvaluationComponent** cmdlet changes how often Microsoft System Center Configuration Manager evaluates collections.
Configuration Manager queries the database at a regular interval to check for changes in collection membership.
You can specify which site to change by site server name or site code.

## EXAMPLES

### Example 1: Set an evaluation period for a site code
```
PS C:\>Set-CMCollectionMembershipEvaluationComponent -MinutesInterval 5 -SiteCode "CM4"
```

This command sets the evaluation frequency to five minutes for the specified site code.

### Example 2: Set an evaluation period for a system
```
PS C:\>Set-CMCollectionMembershipEvaluationComponent -MinutesInterval 6 -SiteSystemName "CM01.West01.Contoso.com"
```

This command sets the evaluation frequency to six minutes for the server named CM01.West01.Contoso.com.

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

### -EvaluationMins


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinutesInterval

Required: True
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

### -SiteCode
Specifies an array of a site codes for Configuration Manager sites.

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

### -SiteSystemServerName


```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

[Get-CMCollectionMembershipEvaluationComponent](xref:ConfigurationManager/vlatest/Get-CMCollectionMembershipEvaluationComponent.md)


