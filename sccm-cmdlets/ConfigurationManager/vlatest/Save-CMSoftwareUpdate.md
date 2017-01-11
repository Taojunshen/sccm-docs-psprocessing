---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833589
schema: 2.0.0
ms.assetid: A7674431-A404-4964-A1E4-1E056EB48EF0
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Save-CMSoftwareUpdate.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Save-CMSoftwareUpdate.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Save-CMSoftwareUpdate.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Save-CMSoftwareUpdate

## SYNOPSIS
Saves software updates to update groups and packages.

## SYNTAX

### SearchByNameMandatory (Default)
```
Save-CMSoftwareUpdate -SoftwareUpdateName <String[]> [-Location <String>] -DeploymentPackageName <String>
 [-SoftwareUpdateLanguage <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Save-CMSoftwareUpdate -SoftwareUpdateId <String[]> [-Location <String>] -DeploymentPackageName <String>
 [-SoftwareUpdateLanguage <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Save-CMSoftwareUpdate -SoftwareUpdate <IResultObject> [-Location <String>] -DeploymentPackageName <String>
 [-SoftwareUpdateLanguage <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory_UpdateGroup
```
Save-CMSoftwareUpdate -SoftwareUpdateGroupId <String[]> [-Location <String>] -DeploymentPackageName <String>
 [-SoftwareUpdateLanguage <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory_UpdateGroup
```
Save-CMSoftwareUpdate -SoftwareUpdateGroupName <String[]> [-Location <String>] -DeploymentPackageName <String>
 [-SoftwareUpdateLanguage <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory_UpdateGroup
```
Save-CMSoftwareUpdate -SoftwareUpdateGroup <IResultObject> [-Location <String>] -DeploymentPackageName <String>
 [-SoftwareUpdateLanguage <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Save-CMSoftwareUpdate** cmdlet saves one or more software updates to update groups and packages.

You can specify one or more software updates associated with deployment packages.
You can also specify the location to save the updates and the language of the software updates.
Languages determine which summary details a software update synchronizes and the file languages to be downloaded for software updates.

## EXAMPLES

### Example 1: Save a software update and add a language to it
```
PS C:\> Save-CMSoftwareUpdate -SoftwareUpdateName "Cumulative Update for Windows 10 (KB3095020)" -DeploymentPackageName "Package01" -SoftwareUpdateLanguage "English"
```

This command saves the software update named Cumulative Update for Windows 10 (KB3095020) for the deployment package named Package01 adding English to its array of languages.

### Example 2: Save a software update from a software update group
```
PS C:\> Get-CMSoftwareUpdateGroup -Name "TestSUgroup10" | Save-CMSoftwareUpdate -DeploymentPackageName "Package01"
```

This command gets the software update group object named TestSUgroup10 and uses the pipeline operator to pass the object to **Save-CMSoftwareUpdate**, which saves the software update with the package name Package01.

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

### -DeploymentPackageName
Specifies a name of a deployment package.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: Named
Default value: None
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

### -Location
Specifies a location to save a software update.

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

### -SoftwareUpdate
Specifies a software update object.
To obtain a software update object, use the [Get-CMSoftwareUpdate](./Get-CMSoftwareUpdate.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroup
Specifies a software update group object.
To obtain a software update group object, use the [Get-CMSoftwareUpdateGroup](./Get-CMSoftwareUpdateGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_UpdateGroup
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId
Specifies an array of IDs of software update groups.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_UpdateGroup
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName
Specifies an array of names of software update groups.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_UpdateGroup
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateId
Specifies an array of IDs of software updates.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateLanguage
Specifies an array of software update languages.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName
Specifies an array of software update names.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName
Required: True
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

[Get-CMSoftwareUpdate](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdate.md)

[Get-CMSoftwareUpdateGroup](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdate](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdate.md)

[Sync-CMSoftwareUpdate](xref:ConfigurationManager/vlatest/Sync-CMSoftwareUpdate.md)


