---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833913
schema: 2.0.0
ms.assetid: F8EFAEC4-2716-4761-BA06-D4B32F6ECB15
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateGroup.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMSoftwareUpdateGroup.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMSoftwareUpdateGroup

## SYNOPSIS
Gets software update groups.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateGroup [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareUpdateGroup -Id <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateGroup** cmdlet gets one or more software update groups in Microsoft System Center Configuration Manager.
A software update group is a collection of one or more software updates.
You can add software updates to a software update group and then deploy the group to clients.
After you deploy a software update group, you can add new software updates to the group and System Center Configuration Manager automatically deploys them.

## EXAMPLES

### Example 1: Get software update groups
```
PS C:\>Get-CMSoftwareUpdateGroup
```

This command gets all software update groups.

### Example 2: Get a software update group by using an ID
```
PS C:\>Get-CMSoftwareUpdateGroup -Id "ST10000D"
```

This command gets a software update group that has the ID ST10000D.

### Example 3: Get a software update group by using a name
```
PS C:\>Get-CMSoftwareUpdateGroup CMSoftwareUpdateGroup -Name "SUGroupD01"
```

This command gets a software update group object named SUGroupD01.

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

### -Id
Specifies an array of IDs of software update groups.

```yaml
Type: Int32[]
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software update groups.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMSoftwareUpdateGroup](xref:ConfigurationManager/vlatest/New-CMSoftwareUpdateGroup.md)

[Remove-CMSoftwareUpdateGroup](xref:ConfigurationManager/vlatest/Remove-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdateGroup](xref:ConfigurationManager/vlatest/Set-CMSoftwareUpdateGroup.md)


