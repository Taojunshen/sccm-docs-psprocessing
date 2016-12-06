---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834267
schema: 2.0.0
ms.assetid: C935BAD3-3AE4-43E7-B02E-68C2ECD43EA2
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMConfigurationItem.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMConfigurationItem.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMConfigurationItem

## SYNOPSIS
Gets Configuration Manager configuration items.

## SYNTAX

### SearchByName (Default)
```
Get-CMConfigurationItem [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMConfigurationItem [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConfigurationItem** cmdlet gets configuration item objects in Microsoft System Center Configuration Manager.
You can use this cmdlet to get items for other cmdlets to use.
For instance, you might get configuration items so you can use the Set-CMConfigurationItem to change settings on them.

Configuration items contain one or more settings, along with compliance rules.
For more information about configuration items, see [Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014) on TechNet.

## EXAMPLES

### Example 1: Get an item using a name
```
PS C:\>Get-CMConfigurationItem -Name "ConfigItem76"
```

This command gets a configuration item named ConfigItem76.

### Example 2: Get an item to use with another cmdlet
```
PS C:\>$CIObj=Get-CMConfigurationItem -Id "16777568"
PS C:\> Remove-CMConfigurationItem -InputObject $CIObj
```

The first command gets a configuration item with the specified identifier and stores it in the $CIObj variable.

The second command removes the item in the $CIObj variable.

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
Specifies an array of identifiers for one or more configuration items.
You can use a comma separated list.

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
Specifies an array of names of configuration items.
You can use a comma separated list.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014)

[Export-CMConfigurationItem](xref:ConfigurationManager/vlatest/Export-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](xref:ConfigurationManager/vlatest/Get-CMConfigurationItemXMLDefinition.md)

[Import-CMConfigurationItem](xref:ConfigurationManager/vlatest/Import-CMConfigurationItem.md)

[New-CMConfigurationItem](xref:ConfigurationManager/vlatest/New-CMConfigurationItem.md)

[Remove-CMConfigurationItem](xref:ConfigurationManager/vlatest/Remove-CMConfigurationItem.md)

[Set-CMConfigurationItem](xref:ConfigurationManager/vlatest/Set-CMConfigurationItem.md)

[Get-CMConfigurationItemHistory](xref:ConfigurationManager/vlatest/Get-CMConfigurationItemHistory.md)


