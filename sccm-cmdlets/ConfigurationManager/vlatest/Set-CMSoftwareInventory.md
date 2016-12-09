---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834050
schema: 2.0.0
ms.assetid: 8210D2F5-9101-47D0-81E7-5F837F5F4F60
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMSoftwareInventory.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMSoftwareInventory.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMSoftwareInventory.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMSoftwareInventory

## SYNOPSIS
Modifies an object that collects software inventory data on files.

## SYNTAX

### SetById (Default)
```
Set-CMSoftwareInventory -Id <String> [-NewName <String>] [-Publisher <String>] [-FamilyId <Int32>]
 [-Tag1Id <Int32>] [-Tag2Id <Int32>] [-Tag3Id <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSoftwareInventory -Name <String[]> [-NewName <String>] [-Publisher <String>] [-FamilyId <Int32>]
 [-Tag1Id <Int32>] [-Tag2Id <Int32>] [-Tag3Id <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMSoftwareInventory -InputObject <IResultObject> [-NewName <String>] [-Publisher <String>]
 [-FamilyId <Int32>] [-Tag1Id <Int32>] [-Tag2Id <Int32>] [-Tag3Id <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareInventory** cmdlet modifies an object that collects information about files on client devices in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Set a software inventory object
```
PS C:\> Set-CMSoftwareInventory -Name "MSXML 6.0 Parser"
```

This command starts collecting software inventory data on the file named MSXML 6.0 Parser.

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

### -FamilyId
Specifies the ID of the family used to classify inventoried software in Configuration Manager.

```yaml
Type: Int32
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
Parameter Sets: SetById
Aliases: SoftwareKey
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMSoftwareInventory** object.
To obtain a **CMSoftwareInventory** object, use the [Get-CMSoftwareInventory](./Get-CMSoftwareInventory.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software files.

```yaml
Type: String[]
Parameter Sets: SetByName
Aliases: CommonName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for inventoried software in Configuration Manager.

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

### -Publisher
Specifies the name of a software publisher in Configuration Manager.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CommonPublisher
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag1Id
Specifies the ID of a tag to classify inventoried software in Configuration Manager.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag2Id
Specifies the ID of a tag to classify inventoried software in Configuration Manager.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag3Id
Specifies the ID of a tag to classify inventoried software in Configuration Manager.

```yaml
Type: Int32
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

[Get-CMSoftwareInventory](xref:ConfigurationManager/vlatest/Get-CMSoftwareInventory.md)

[Undo-CMSoftwareInventory](xref:ConfigurationManager/vlatest/Undo-CMSoftwareInventory.md)
