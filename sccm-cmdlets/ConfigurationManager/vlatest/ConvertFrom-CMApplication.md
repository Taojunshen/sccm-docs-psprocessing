---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833872
schema: 2.0.0
ms.assetid: 29E31091-FF04-446F-82EC-FD3FFF90B526
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/ConvertFrom-CMApplication.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/ConvertFrom-CMApplication.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/ConvertFrom-CMApplication.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# ConvertFrom-CMApplication

## SYNOPSIS
Converts an application SDK object to an application object.

## SYNTAX

```
ConvertFrom-CMApplication -InputObject <Application> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **ConvertFrom-CMApplication** cmdlet converts an application SDK object to an application object.

## EXAMPLES

### Example 1: Convert an application object
```
PS C:\> $SdkApp = Get-CMApplication -Name "Application01" | ConvertTo-CMApplication
PS C:\> $SdkApp | ConvertFrom-CMApplication
```

The first command gets the application object named Application01 and uses the pipeline operator to pass the object to **ConvertTo-CMApplication**, which converts the application object into an application SDK object.
The command then stores the object in the $SdkApp variable.

The second command converts the application SDK object stored in $SdkApp to an application object.

### Example 2: Convert an application object
```
PS C:\> $SdkApp = Get-CMApplication -Name "Application02" | ConvertTo-CMApplication
PS C:\> ConvertFrom-CMApplication -InputObject $SdkApp
```

The first command gets the application object named Application02 and uses the pipeline operator to pass the object to **ConvertTo-CMApplication**, which converts the application object into an application SDK object.
The command then stores the object in the $SdkApp variable.

The second command converts the application SDK object stored in $SdkApp to an application object.

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

### -InputObject
Specifies an application SDK object.
To obtain an application object, use the [ConvertTo-CMApplication](./ConvertTo-CMApplication.md) cmdlet or the [Convert-CMApplication](./Convert-CMApplication.md) cmdlet.

```yaml
Type: Application
Parameter Sets: (All)
Aliases: Application
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Convert-CMApplication](xref:ConfigurationManager/vlatest/Convert-CMApplication.md)

[ConvertTo-CMApplication](xref:ConfigurationManager/vlatest/ConvertTo-CMApplication.md)

[Get-CMApplication](xref:ConfigurationManager/vlatest/Get-CMApplication.md)

[Export-CMApplication](xref:ConfigurationManager/vlatest/Export-CMApplication.md)

[Get-CMApplication](xref:ConfigurationManager/vlatest/Get-CMApplication.md)

[Import-CMApplication](xref:ConfigurationManager/vlatest/Import-CMApplication.md)

[Remove-CMApplication](xref:ConfigurationManager/vlatest/Remove-CMApplication.md)

[Resume-CMApplication](xref:ConfigurationManager/vlatest/Resume-CMApplication.md)

[Set-CMApplication](xref:ConfigurationManager/vlatest/Set-CMApplication.md)

[Suspend-CMApplication](xref:ConfigurationManager/vlatest/Suspend-CMApplication.md)


