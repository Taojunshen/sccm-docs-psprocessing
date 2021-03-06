---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834273
schema: 2.0.0
ms.assetid: CD47E9D6-4600-43D9-917C-77501237D683
updated_at: 12/6/2016 11:47 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Undo-CMSoftwareInventory.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Undo-CMSoftwareInventory.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/322e1e3dae6ba53c3384ca0bf1a1079481b8ae30/sccm-cmdlets/ConfigurationManager/vlatest/Undo-CMSoftwareInventory.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Undo-CMSoftwareInventory

## SYNOPSIS
Stops collecting software inventory data on files.

## SYNTAX

### SearchByValueMandatory (Default)
```
Undo-CMSoftwareInventory -SoftwareInventory <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Undo-CMSoftwareInventory -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Undo-CMSoftwareInventory -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Undo-CMSoftwareInventory** cmdlet stops collecting information about files that are contained on client devices.

## EXAMPLES

### Example 1: Stop collecting software inventory data on a file
```
PS C:\>Undo-CMSoftwareInventory -Name "MSXML 6.0 Parser"
```

This command stops collecting software inventory data on the file named MSXML 6.0 Parser.

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
Specifies an array of IDs of software files.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: SoftwareKey
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software files.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: CommonName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInventory
Specifies a **CMSoftwareInventory** object.
To obtain a **CMSoftwareInventory** object, use the [Get-CMSoftwareInventory](./Get-CMSoftwareInventory.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: InputObject
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-CMSoftwareInventory](xref:ConfigurationManager/vlatest/Get-CMSoftwareInventory.md)

[Set-CMSoftwareInventory](xref:ConfigurationManager/vlatest/Set-CMSoftwareInventory.md)
