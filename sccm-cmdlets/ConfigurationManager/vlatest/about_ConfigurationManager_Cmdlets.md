---
updated_at: 12/1/2016 10:06 PM
ms.date: 12/1/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/about_ConfigurationManager_Cmdlets.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/1312aee056984b5746a8b0e3c3eaae99f795b2f4/sccm-cmdlets/ConfigurationManager/vlatest/about_ConfigurationManager_Cmdlets.md
uid: ConfigurationManager/vlatest/about_ConfigurationManager_Cmdlets.md
ms.topic: conceptual
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---
# ConfigurationManager_Cmdlets
## about_ConfigurationManager_Cmdlets

# SHORT DESCRIPTION
Provides information about the Microsoft System Center Configuration Manager
cmdlets, provider, and updateable help.

# LONG DESCRIPTION
The Windows PowerShell module for System Center Configuration Manager lets
you manage a Configuration Manager hierarchy by using Windows PowerShell
cmdlets and scripts.

## Prerequisites
To use Windows PowerShell in Configuration Manager, you must install the
following:

    - Windows PowerShell 3.0 or later

    - System Center Configuration Manager console

## Using Windows PowerShell for Configuration Manager
You can run Configuration Manager cmdlets and scripts by using the
Configuration Manager console or by using a Windows PowerShell session.
When you run Configuration Manager cmdlets by using the Configuration
Manager console, your session runs in the context of the site.

    To start a Windows PowerShell session from the Configuration Manager
    console

    - In the Configuration Manager console, click the drop down menu.

    - Select Connect via Windows PowerShell.

    To use the Configuration Manager module in a Windows PowerShell session

    - Start Windows PowerShell.

    - Change the directory to
      <ConfigMgrConsoleInstallationPath>\Program Files (x86)\Microsoft
      Configuration Manager\AdminConsole\bin
      and then import the Configuration Manager module by typing the
      following command: Import-module -Name "ConfigurationManager.psd1"

## Windows PowerShell Drive Provider
The Configuration Manager module for Windows PowerShell includes a
Windows PowerShell drive provider for individual sites. By using the
CD command in the Windows PowerShell console, you can change the context
of your session to a different site.

## Updateable Help
The Configuration Manager module for Windows PowerShell supports
Updateable Help. When your computer is connected to the Internet, you
can use the Update-Help cmdlet to start an automatic download of the
Configuration Manager Windows PowerShell help file. After you have
downloaded the help file, you can get information about a cmdlet, which
includes syntax and parameter sets, by typing Get-Help <cmdlet>
-Detailed.

# SEE ALSO
[ConfigurationManager Module](ConfigurationManager.md)
