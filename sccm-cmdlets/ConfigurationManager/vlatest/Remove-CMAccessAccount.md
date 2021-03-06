---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833861
schema: 2.0.0
ms.assetid: D9439146-832E-49E5-A105-B06F9B5B1296
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAccessAccount.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAccessAccount.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAccessAccount.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Remove-CMAccessAccount

## SYNOPSIS
Removes users or groups from an access account.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMAccessAccount -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByApplicationName
```
Remove-CMAccessAccount -ApplicationName <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByApplicationId
```
Remove-CMAccessAccount -ApplicationId <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByBootImageName
```
Remove-CMAccessAccount -BootImageName <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByBootImageId
```
Remove-CMAccessAccount -BootImageId <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDriverPackageName
```
Remove-CMAccessAccount -DriverPackageName <String> -AccountType <AccessAccountType> [-UserName <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDriverPackageId
```
Remove-CMAccessAccount -DriverPackageId <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSImageName
```
Remove-CMAccessAccount -OperatingSystemImageName <String> -AccountType <AccessAccountType> [-UserName <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSImageId
```
Remove-CMAccessAccount -OperatingSystemImageId <String> -AccountType <AccessAccountType> [-UserName <String>]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByOSInstallerName
```
Remove-CMAccessAccount -OperatingSystemInstallerName <String> -AccountType <AccessAccountType>
 [-UserName <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSInstallerId
```
Remove-CMAccessAccount -OperatingSystemInstallerId <String> -AccountType <AccessAccountType>
 [-UserName <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByPackageName
```
Remove-CMAccessAccount -PackageName <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByPackageId
```
Remove-CMAccessAccount -PackageId <String> -AccountType <AccessAccountType> [-UserName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageName
```
Remove-CMAccessAccount -SoftwareUpdateDeploymentPackageName <String> -AccountType <AccessAccountType>
 [-UserName <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageId
```
Remove-CMAccessAccount -SoftwareUpdateDeploymentPackageId <String> -AccountType <AccessAccountType>
 [-UserName <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAccessAccount** cmdlet removes users or groups from an access account.

An access account is a list of users or groups that can access an established service or application that is located on a distribution point.
For example, members in the Software Update Point Connection Access Account can access two services to manage software updates: Windows Server Update Services (WSUS) and WSUS Synchronization Manager.

## EXAMPLES

### Example 1: Remove a user from an access account for an application by using its name
```
PS C:\> Remove-CMAccessAccount -ApplicationName "SharePoint 2010" -Type WindowsUser -UserName "CONTOSO\ENarvaez" -Confirm
```

This command removes a Windows user from the access account for an application that is specified by using its name.
You must confirm the action before the command performs it.

### Example 2: Remove a group from an access account for a package by using its ID
```
PS C:\> $ID = Get-CMAccessAccount -PackageId "CM1100002" 
PS C:\> Remove-CMAccessAccount -PackageId $ID -Type WindowsGroup -UserName "CONTOSO\Guest"
```

The first command gets the package object ID, and then stores it in the variable $ID.

The second command removes a group from the access account for the specified package.
No confirmation is required.

## PARAMETERS

### -AccountType
Specifies an account type.
Valid values are: Guest, User, WindowsGroup, and WindowsUser.

```yaml
Type: AccessAccountType
Parameter Sets: (All)
Aliases: 
Accepted values: User, Guest, Administrator, WindowsUser, WindowsGroup
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
Specifies the ID of an application.

```yaml
Type: String
Parameter Sets: SearchByApplicationId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
Specifies the name of an application.

```yaml
Type: String
Parameter Sets: SearchByApplicationName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId
Specifies the ID of a boot image.

```yaml
Type: String
Parameter Sets: SearchByBootImageId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageName
Specifies the name of a boot image.

```yaml
Type: String
Parameter Sets: SearchByBootImageName
Aliases: 
Required: True
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

### -DriverPackageId
Specifies the ID of a driver package.

```yaml
Type: String
Parameter Sets: SearchByDriverPackageId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageName
Specifies the name of a driver package.

```yaml
Type: String
Parameter Sets: SearchByDriverPackageName
Aliases: 
Required: True
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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: DriverPackage, Application, OperatingSystemImage, OperatingSystemInstaller, Package, SoftwareUpdateDeploymentPackage, BootImage
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperatingSystemImageId
Specifies the ID of an operating system image.

```yaml
Type: String
Parameter Sets: SearchByOSImageId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageName
Specifies the name of an operating system image.

```yaml
Type: String
Parameter Sets: SearchByOSImageName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstallerId
Specifies the ID of an operating system installer.

```yaml
Type: String
Parameter Sets: SearchByOSInstallerId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstallerName
Specifies the name of an operating system installer.

```yaml
Type: String
Parameter Sets: SearchByOSInstallerName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageId
Specifies the ID of a deployed software script or program.

```yaml
Type: String
Parameter Sets: SearchByPackageId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName
Specifies the name of a deployed software script or program.

```yaml
Type: String
Parameter Sets: SearchByPackageName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateDeploymentPackageId
Specifies the ID of a deployed software update.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateDeploymentPackageId
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateDeploymentPackageName
Specifies the name of a deployed software update.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateDeploymentPackageName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies a Windows user account name in domain\user format.

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

[New-CMAccessAccount](xref:ConfigurationManager/vlatest/New-CMAccessAccount.md)

[Get-CMAccessAccount](xref:ConfigurationManager/vlatest/Get-CMAccessAccount.md)

[Set-CMAccessAccount](xref:ConfigurationManager/vlatest/Set-CMAccessAccount.md)

[Get-CMApplication](xref:ConfigurationManager/vlatest/Get-CMApplication.md)

[Get-CMBootImage](xref:ConfigurationManager/vlatest/Get-CMBootImage.md)

[Get-CMDriverPackage](xref:ConfigurationManager/vlatest/Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](xref:ConfigurationManager/vlatest/Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](xref:ConfigurationManager/vlatest/Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](xref:ConfigurationManager/vlatest/Get-CMPackage.md)

[Get-CMSoftwareUpdateDeploymentPackage](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdateDeploymentPackage.md)


