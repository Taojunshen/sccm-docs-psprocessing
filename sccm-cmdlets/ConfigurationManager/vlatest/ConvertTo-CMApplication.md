---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833884
schema: 2.0.0
ms.assetid: 84CEC68E-3693-4DFD-B853-AC5032E465E6
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/ConvertTo-CMApplication.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/ConvertTo-CMApplication.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/ConvertTo-CMApplication.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# ConvertTo-CMApplication

## SYNOPSIS
Converts an application object to an application SDK object.

## SYNTAX

```
ConvertTo-CMApplication -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **ConvertTo-CMApplication** cmdlet converts an application object to an application SDK object.

## EXAMPLES

### Example 1: Get an application and convert it
```
PS C:\> Get-CMApplication -Name "Application01" | ConvertTo-CMApplication
```

This command gets the application object named Application01 and uses the pipeline operator to pass the object to **ConvertTo-CMApplication**, which converts the application object to an application SDK object.

### Example 2: Convert an application
```
PS C:\>ConvertTo-CMApplication -InputObject (Get-CMApplication -Name "Application02")
```

This command gets the application object named Application02 and converts the application object to an application SDK object.

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
Specifies an application object.
To obtain an application object, use the [Get-CMApplication](./Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: Application, DeploymentType
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

[ConvertFrom-CMApplication](xref:ConfigurationManager/vlatest/ConvertFrom-CMApplication.md)

[Get-CMApplication](xref:ConfigurationManager/vlatest/Get-CMApplication.md)

[Export-CMApplication](xref:ConfigurationManager/vlatest/Export-CMApplication.md)

[Import-CMApplication](xref:ConfigurationManager/vlatest/Import-CMApplication.md)

[New-CMApplication](xref:ConfigurationManager/vlatest/New-CMApplication.md)

[Remove-CMApplication](xref:ConfigurationManager/vlatest/Remove-CMApplication.md)

[Resume-CMApplication](xref:ConfigurationManager/vlatest/Resume-CMApplication.md)

[Set-CMApplication](xref:ConfigurationManager/vlatest/Set-CMApplication.md)

[Suspend-CMApplication](xref:ConfigurationManager/vlatest/Suspend-CMApplication.md)


