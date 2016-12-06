---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833918
schema: 2.0.0
ms.assetid: CA239E73-691E-4A34-852A-8417420E68E1
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Copy-CMConfigurationPolicy.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Copy-CMConfigurationPolicy.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Copy-CMConfigurationPolicy

## SYNOPSIS
Copies a configuration policy.

## SYNTAX

### SearchByValueMandatory (Default)
```
Copy-CMConfigurationPolicy [-InputObject] <IResultObject> [-NewName] <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Copy-CMConfigurationPolicy [-Id] <Int32> [-NewName] <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Copy-CMConfigurationPolicy [-Name] <String> [-NewName] <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Copy-CMConfigurationPolicy** copies a configuration policy.
A configuration policy can be a client authentication  certificate profile configuration item, a wireless profile configuration item, or others.
See the Alias section for additional policy items that you can use this cmdlet to copy.

## EXAMPLES

### Example 1: Copy a configuration policy by using the pipeline
```
PS C:\> Get-CMConfigurationPolicy -Name "TrustedCACert01" -Fast | Copy-CMConfigurationPolicy -NewName "TrustedCACert01_copy"
```

This command gets the configuration policy object named TrustedCACert01 and uses the pipeline operator to pass the object to **Copy-CMConfiguratinPolicy**, which creates a copy of the policy and names it TrustedCACert01_copy.

### Example 2: Copy a configuration policy by ID
```
PS C:\> Copy-CMConfigurationPolicy -Id 16777454 -NewName "EmailProfile1_copy"
```

This command makes a copy of the configuration policy with the ID of 16777454 and names it EmailProfile1_copy.

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
Specifies the CI_ID of a configuration policy.

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

### -InputObject
Gets a configuration policy object.
To obtain a configuration policy object, use the Get-CMConfigurationPolicy cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ConfigurationPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a configuration policy.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a name for the copy of the configuration policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

[Get-CMConfigurationPolicy](xref:ConfigurationManager/vlatest/Get-CMConfigurationPolicy.md)

[Remove-CMConfigurationPolicy](xref:ConfigurationManager/vlatest/Remove-CMConfigurationPolicy.md)


