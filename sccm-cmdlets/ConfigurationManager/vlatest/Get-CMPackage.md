---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833809
schema: 2.0.0
ms.assetid: 4D76D4D0-5D21-4320-BEA6-335CE01284A7
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMPackage.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMPackage.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMPackage

## SYNOPSIS
Gets Configuration Manager packages.

## SYNTAX

### SearchByName (Default)
```
Get-CMPackage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMPackage -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMPackage** cmdlet gets Microsoft System Center Configuration Manager packages.
System Center Configuration Manager uses packages to distribute software to clients.
You can use the *SecuredScopeNames* parameter to specify the security scope of a package to get.

## EXAMPLES

### Example 1: Get all packages
```
PS C:\> Get-CMPackage
```

This command gets all Configuration Manager packages.

### Example 2: Get a package by using an ID
```
PS C:\> Get-CMPackage -Id "CM100002"
```

This command gets the program that has the ID CM100002.

### Example 3: Get a package by using a name
```
PS C:\> Get-CMPackage -Name "Configuration Manager Client Package"
```

This command gets the program named Configuration Manager Client Package.

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
Specifies an array of package IDs.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a package.

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

[Export-CMPackage](xref:ConfigurationManager/vlatest/Export-CMPackage.md)

[Import-CMPackage](xref:ConfigurationManager/vlatest/Import-CMPackage.md)

[New-CMPackage](xref:ConfigurationManager/vlatest/New-CMPackage.md)

[Remove-CMPackage](xref:ConfigurationManager/vlatest/Remove-CMPackage.md)

[Set-CMPackage](xref:ConfigurationManager/vlatest/Set-CMPackage.md)


