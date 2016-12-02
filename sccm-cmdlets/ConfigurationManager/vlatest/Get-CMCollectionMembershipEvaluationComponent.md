---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834233
schema: 2.0.0
ms.assetid: 7D654E76-C29F-49C5-9795-A9B845086DAE
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCollectionMembershipEvaluationComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCollectionMembershipEvaluationComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMCollectionMembershipEvaluationComponent

## SYNOPSIS
Gets how often Configuration Manager evaluates collection membership.

## SYNTAX

```
Get-CMCollectionMembershipEvaluationComponent [-SiteSystemServerName <String>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCollectionMembershipEvaluationComponent** cmdlet gets the value for how often Microsoft System Center Configuration Manager evaluates collections.
Configuration Manager queries the database at a regular interval to check for changes in collection membership.
You can specify which value to get by site server name or site code.

## EXAMPLES

### Example 1: Get an evaluation period for a site code
```
PS C:\>Get-CMCollectionMembershipEvaluationComponent -SiteCode "CM4"
```

This command gets the evaluation frequency for collection membership for the specified site code.

### Example 2: Get an evaluation period for a system
```
PS C:\>Get-CMCollectionMembershipEvaluationComponent -SiteSystemServerName "CM01.West01.Contoso.com"
```

This command gets the evaluation frequency for the server named CM01.West01.Contoso.com.

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

### -SiteCode


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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMCollectionMembershipEvaluationComponent](xref:ConfigurationManager/vlatest/Set-CMCollectionMembershipEvaluationComponent.md)

