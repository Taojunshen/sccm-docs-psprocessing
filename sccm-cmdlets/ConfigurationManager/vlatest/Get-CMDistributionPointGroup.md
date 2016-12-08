---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833656
schema: 2.0.0
ms.assetid: B616CC22-3B89-436A-BDDB-3BC01C5DAD7D
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDistributionPointGroup.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMDistributionPointGroup.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMDistributionPointGroup

## SYNOPSIS
Gets distribution point groups.

## SYNTAX

### SearchByName (Default)
```
Get-CMDistributionPointGroup [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDistributionPointGroup -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDistributionPointGroup** cmdlet gets one or more distribution point groups.

## EXAMPLES

### Example 1: Get a distribution point group by using an ID
```
PS C:\> Get-CMDistributionPointGroup -Id "{6617708D-0F98-4898-8D05-9E882C23DCB2}"
```

This command get the distribution point group that has the ID 6617708D-0F98-4898-8D05-9E882C23DCB2.

### Example 2: Get a distribution point group by using a name
```
PS C:\> Get-CMDistributionPointGroup -Name "Dpg01" -Id "{FA921CF2-89C9-407D-A21D-FE6947F2C00A}"
```

This command gets the distribution point group named Dpg01 and that has the ID FA921CF2-89C9-407D-A21D-FE6947F2C00A.

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
Specifies an array of IDs of distribution point groups.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: GroupId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a distribution point group.

```yaml
Type: String
Parameter Sets: SearchByName
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

## NOTES

## RELATED LINKS

[New-CMDistributionPointGroup](xref:ConfigurationManager/vlatest/New-CMDistributionPointGroup.md)

[Remove-CMDistributionPointGroup](xref:ConfigurationManager/vlatest/Remove-CMDistributionPointGroup.md)

[Set-CMDistributionPointGroup](xref:ConfigurationManager/vlatest/Set-CMDistributionPointGroup.md)


