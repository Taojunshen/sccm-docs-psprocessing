---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834211
schema: 2.0.0
ms.assetid: BAAFB5BA-EC7B-48DE-B029-4AA132BD9AEE
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMAccessAccount.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMAccessAccount.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/New-CMAccessAccount.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# New-CMAccessAccount

## SYNOPSIS
Adds users or groups to an access account.

## SYNTAX

### SearchByValue (Default)
```
New-CMAccessAccount [-InputObject] <IResultObject> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByApplicationName
```
New-CMAccessAccount -ApplicationName <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByApplicationId
```
New-CMAccessAccount -ApplicationId <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByBootImageName
```
New-CMAccessAccount -BootImageName <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByBootImageId
```
New-CMAccessAccount -BootImageId <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByDriverPackageName
```
New-CMAccessAccount -DriverPackageName <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByDriverPackageId
```
New-CMAccessAccount -DriverPackageId <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSImageName
```
New-CMAccessAccount -OperatingSystemImageName <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSImageId
```
New-CMAccessAccount -OperatingSystemImageId <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByOSInstallerName
```
New-CMAccessAccount -OperatingSystemInstallerName <String> -AccountType <AccessAccountType>
 [-UserName <String>] -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByOSInstallerId
```
New-CMAccessAccount -OperatingSystemInstallerId <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByPackageName
```
New-CMAccessAccount -PackageName <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByPackageId
```
New-CMAccessAccount -PackageId <String> -AccountType <AccessAccountType> [-UserName <String>]
 -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageName
```
New-CMAccessAccount -SoftwareUpdateDeploymentPackageName <String> -AccountType <AccessAccountType>
 [-UserName <String>] -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateDeploymentPackageId
```
New-CMAccessAccount -SoftwareUpdateDeploymentPackageId <String> -AccountType <AccessAccountType>
 [-UserName <String>] -Access <AccessRight> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAccessAccount** cmdlet adds users or groups to an access account.

An access account is a list of users or groups that can access an established service or application that is located on a distribution point.
For example, members in the Software Update Point Connection access account can access two services to manage software updates: Windows Server Update Services (WSUS) and WSUS Synchronization Manager.

## EXAMPLES

### Example 1: Modify access to an application by using the application ID
```
PS C:\> $ID = Get-CMAccessAccount -ApplicationID "12994680"
PS C:\> New-CMAccessAccount -ApplicationID $ID -Type WindowsUser Username "CONTOSO\EDaugherty" -Access "FullControl"
```

The first command gets an application ID, and then stores it in the $ID variable.

The second command gets the application that is identified by $ID and adds a user to the access account.
The permissions of the new user are set to FullControl.

## PARAMETERS

### -Access
Specifies the access rights that are associated with an access account.
Valid values are: No Access, Read, Change, and Full Control.

```yaml
Type: AccessRight
Parameter Sets: (All)
Aliases: 
Accepted values: NoAccess, Read, Change, FullControl
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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
Aliases: Application, BootImage, DriverPackage, OperatingSystemImage, OperatingSystemInstaller, Package, SoftwareUpdateDeploymentPackage
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

[Get-CMAccessAccount](xref:ConfigurationManager/vlatest/Get-CMAccessAccount.md)

[Set-CMAccessAccount](xref:ConfigurationManager/vlatest/Set-CMAccessAccount.md)

[Remove-CMAccessAccount](xref:ConfigurationManager/vlatest/Remove-CMAccessAccount.md)

[Get-CMApplication](xref:ConfigurationManager/vlatest/Get-CMApplication.md)

[Get-CMBootImage](xref:ConfigurationManager/vlatest/Get-CMBootImage.md)

[Get-CMDriverPackage](xref:ConfigurationManager/vlatest/Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](xref:ConfigurationManager/vlatest/Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](xref:ConfigurationManager/vlatest/Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](xref:ConfigurationManager/vlatest/Get-CMPackage.md)

[Get-CMSoftwareUpdateDeploymentPackage](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdateDeploymentPackage.md)


