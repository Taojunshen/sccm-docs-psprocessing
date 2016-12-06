---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834106
schema: 2.0.0
ms.assetid: 0249609D-987D-4F8C-85AD-B4BFD4970484
updated_at: 12/5/2016 10:55 PM
ms.date: 12/5/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAppVVirtualEnvironment.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/f95cf139be40af870257194c70c82183d89f7a0c/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMAppVVirtualEnvironment.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMAppVVirtualEnvironment

## SYNOPSIS
Gets an App-V virtual environment.

## SYNTAX

### SearchByName (Default)
```
Get-CMAppVVirtualEnvironment [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMAppVVirtualEnvironment -Id <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAppVVirtualEnvironment** cmdlet gets one or more Microsoft Application Virtualization (App-V) virtual environment objects from Microsoft System Center Configuration Manager.
You can specify App-V environments by name or ID.

## EXAMPLES

### Example 1: Get all virtual environments
```
PS C:\>Get-CMAppVVirtualEnvironment
```

This command gets all App-V virtual environments.

### Example 2: Get virtual environments by using a wildcard
```
PS C:\>Get-CMAppVVirtualEnvironment -Name "T*"
```

This command gets all App-V virtual environments that have names that begin with the letter T.

### Example 3: Get virtual environment by an ID
```
PS C:\>Get-CMAppVVirtualEnvironment -Id "16781806"
```

This command gets an App-V virtual environment that has the ID 16781806.

## PARAMETERS

### -DisableWildcardHandling


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
Specifies an array of IDs of virtual environments.

```yaml
Type: Int32[]
Parameter Sets: SearchById
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of App-V virtual environment objects.
You can use a wildcard.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

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

[New-CMAppVVirtualEnvironment](xref:ConfigurationManager/vlatest/New-CMAppVVirtualEnvironment.md)

[Remove-CMAppVVirtualEnvironment](xref:ConfigurationManager/vlatest/Remove-CMAppVVirtualEnvironment.md)

[Set-CMAppVVirtualEnvironment](xref:ConfigurationManager/vlatest/Set-CMAppVVirtualEnvironment.md)


