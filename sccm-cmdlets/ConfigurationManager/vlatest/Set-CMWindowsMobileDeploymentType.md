---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834168
schema: 2.0.0
ms.assetid: 079BA78F-2757-4D49-9AE7-51953468AC60
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMWindowsMobileDeploymentType.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMWindowsMobileDeploymentType.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMWindowsMobileDeploymentType

## SYNOPSIS
Sets a Windows Mobile cabinet deployment type.

## SYNTAX

### ByAppName (Default)
```
Set-CMWindowsMobileDeploymentType [-EnableUninstall <Boolean>] [-AddRequirement <Rule[]>]
 -ApplicationName <String> -DeploymentTypeName <String> [-NewName <String>] [-ContentLocation <String>]
 [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru] [-AddLanguage <String[]>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByAppId
```
Set-CMWindowsMobileDeploymentType [-EnableUninstall <Boolean>] [-AddRequirement <Rule[]>]
 -ApplicationId <Int32> -DeploymentTypeName <String> [-NewName <String>] [-ContentLocation <String>]
 [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru] [-AddLanguage <String[]>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByAppValue
```
Set-CMWindowsMobileDeploymentType [-EnableUninstall <Boolean>] [-AddRequirement <Rule[]>]
 -DeploymentTypeName <String> -Application <IResultObject> [-NewName <String>] [-ContentLocation <String>]
 [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru] [-AddLanguage <String[]>]
 [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDTValue
```
Set-CMWindowsMobileDeploymentType [-EnableUninstall <Boolean>] [-AddRequirement <Rule[]>]
 -InputObject <IResultObject> [-NewName <String>] [-ContentLocation <String>] [-RemoveRequirement <Rule[]>]
 [-RemoveLanguage <String[]>] [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMWindowsMobileDeploymentType** cmdlet changes the settings for a Windows Mobile cabinet deployment type.

## EXAMPLES

### Example 1: Change the display name of a deployment type by using the pipeline
```
PS C:\> Get-CMDeploymentType -ApplicationName "Application1" -DeploymentTypeName "DT4" | Set-CMWindowsMobileDeploymentType -EnableUninstall $False -NewName "DT4_New" -RemoveLanguage "en-US","zh-CN" -Comment "Deployment Type updated" -PassThru
```

This command gets the Windows Mobile cabinet deployment type object named DT4 for the application named Application1 and uses the pipeline operator to pass the object to **Set-CMWindowsMobileDeploymentType**.
**Set-CMWindowsMobileDeploymentType** changes the name of the deployment type to DT4_New and removes English and Chinese from the array of supported languages.
Setting the *EnableUninstall* parameter to $False indicates that the user is not allowed to uninstall this application.

### Example 2: Rename a deployment type
```
PS C:\> Set-CMWindowsMobileDeploymentType -ApplicationName "Application1" -DeploymentTypeName "DT4" -EnableUninstall $False -NewName DT4_New -RemoveLanguage "en-US","zh-CN" -Comment "Deployment Type updated" -PassThru
```

This command changes the name of the Windows Mobile cabinet deployment type named DT4 for the application named Application1 to DT4_New, and removes English and Chinese from the array of supported languages.
Setting the *EnableUninstall* parameter to $False indicates that the user is not allowed to uninstall this application.

## PARAMETERS

### -AddLanguage
Adds an array of languages that this deployment type supports.
Provide the languages in the "languagecode2-country" or "languagecode2" format, for example: en, en-US, ja-JP, zh-CN.

For more information about the CultureInfo.Name Property, see [https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.name.aspx](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.name.aspx).

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddLanguages, Languages, Language

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRequirement
Adds an array of requirements for this deployment type.

```yaml
Type: Rule[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Application
Specifies an application object that is associated with this deployment type.
To obtain an application object, use the Get-CMApplication cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByAppValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
Specifies the ID of the application that is associated with this deployment type.

```yaml
Type: Int32
Parameter Sets: ByAppId
Aliases: CI_ID, CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies the name of the application that is associated with this deployment type.

```yaml
Type: String
Parameter Sets: ByAppName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
Specifies a description for this deployment type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdministratorComment

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ContentLocation
Specifies the path of the content.
The site system server requires permissions to read the content files.

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

### -DeploymentTypeName
Specifies a display name for this deployment type.

```yaml
Type: String
Parameter Sets: ByAppName, ByAppId, ByAppValue
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

### -EnableUninstall
Indicates whether the user is allowed to uninstall this application.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowUserToUninstall, AllowsUsersToUninstallThisContent, EnableUserUninstall

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ForceForUnknownPublisher

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
Specifies a deployment type object.
To obtain a deployment type object, use the Get-CMDeploymentType cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByDTValue
Aliases: DeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the deployment type.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewDeploymentTypeName

Required: False
Position: Named
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

### -RemoveLanguage
Removes an array of existing languages from this deployment type.
Provide the languages in the "languagecode2-country" or "languagecode2" format, for example: en, en-US, ja-JP, zh-CN.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveLanguages

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRequirement
Removes the existing installation requirements from this deployment type.

```yaml
Type: Rule[]
Parameter Sets: (All)
Aliases: RemoveRequirements

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

[Add-CMWindowsMobileDeploymentType](xref:ConfigurationManager/vlatest/Add-CMWindowsMobileDeploymentType.md)

[Get-CMApplication](xref:ConfigurationManager/vlatest/Get-CMApplication.md)

[Get-CMDeploymentType](xref:ConfigurationManager/vlatest/Get-CMDeploymentType.md)


