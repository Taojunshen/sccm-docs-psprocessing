---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833903
schema: 2.0.0
ms.assetid: 302A6C32-CFCD-4AB4-99BC-481B2E97604E
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMIosAppStoreDeploymentType.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMIosAppStoreDeploymentType.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMIosAppStoreDeploymentType.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMIosAppStoreDeploymentType

## SYNOPSIS
Sets an iOS App Store deployment type.

## SYNTAX

### ByAppName (Default)
```
Set-CMIosAppStoreDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -ApplicationName <String>
 -DeploymentTypeName <String> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppId
```
Set-CMIosAppStoreDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -ApplicationId <Int32>
 -DeploymentTypeName <String> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAppValue
```
Set-CMIosAppStoreDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -DeploymentTypeName <String>
 -Application <IResultObject> [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>]
 [-PassThru] [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDTValue
```
Set-CMIosAppStoreDeploymentType [-Url <String>] [-AddRequirement <Rule[]>] -InputObject <IResultObject>
 [-NewName <String>] [-RemoveRequirement <Rule[]>] [-RemoveLanguage <String[]>] [-PassThru]
 [-AddLanguage <String[]>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIosAppStoreDeploymentType** cmdlet changes the settings for an iOS App Store deployment type.

## EXAMPLES

### Example 1: Remove a language from a deployment type
```
PS C:\> Set-CMIOSAppStoreDeploymentType -ApplicationName "testIOSapp" -DeploymentTypeName "DTIOSapp02" -NewName "DTIOSapp02_updated" -Url "https://itunes.apple.com/us/app/warhammer-40-000-deathwatch/id791134629?mt=8" -PassThru -Comment "test-set-CMIOSAppStoreDeploymentType" -RemoveLanguage "en-US"
```

This command removes English from the deployment type named DTIOSapp02 for the application named testIOSapp.
The command also renames the deployment type to DTIOSapp02_updated.
The *PassThru* parameter indicates that an object is returned from this command.

### Example 2: Change the display name of a deployment type by using the pipeline
```
PS C:\> Get-CMDeploymentType -ApplicationName "testIOSapp" -DeploymentTypeName "DTIOSapp01" | Set-CMIOSAppStoreDeploymentType -NewName "DTIOSapp01_Updated"
```

This command gets the deployment type object named DTIOSapp01 for the application named testIOSapp and uses the pipeline operator to pass the object to **Set-CMIOSAppStoreDeploymentType**.
**Set-CMIOSAppStoreDeploymentType** changes the name of the deployment type to DTIOSapp01_Updated.

## PARAMETERS

### -AddLanguage
Adds an array of languages that this deployment type supports.
Provide the languages in the "languagecode2-country" or "languagecode2" format, for example: en, en-US, ja-JP, zh-CN.

For more information about the **CultureInfo.Name** property, see [https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.name.aspx](https://msdn.microsoft.com/en-us/library/system.globalization.cultureinfo.name.aspx).

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
To obtain an application object, use the [Get-CMApplication](./Get-CMApplication.md) cmdlet.

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
Specifies an iOS App Store deployment type object.
To obtain a deployment type object, use the [Get-CMDeploymentType](./Get-CMDeploymentType.md) cmdlet.

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
Specifies a new name for this deployment type.

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

### -Url
Specifies the URL of an application in the Apple App Store.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContentLocation
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

[Add-CMIosAppStoreDeploymentType](xref:ConfigurationManager/vlatest/Add-CMIosAppStoreDeploymentType.md)

[Get-CMDeploymentType](xref:ConfigurationManager/vlatest/Get-CMDeploymentType.md)


