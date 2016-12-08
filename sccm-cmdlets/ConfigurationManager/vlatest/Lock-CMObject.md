---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834194
schema: 2.0.0
ms.assetid: CB778D72-D265-4EFA-AE33-A027F7B5A93B
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Lock-CMObject.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Lock-CMObject.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Lock-CMObject

## SYNOPSIS
Locks global objects in Configuration Manager.

## SYNTAX

```
Lock-CMObject [-InputObject] <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Lock-CMObject** cmdlet acquires locks of one or more objects in Microsoft System Center Configuration Manager.
You can use the *InputObject* parameter to specify the input to this cmdlet, or you can pipe the input to this cmdlet.

Serialized Editing of Distributed Objects (SEDO) in System Center Configuration Manager provide a mechanism for assigning and unassigning locks to global System Center Configuration Manager objects in the context of a site, computer and user.
When you use the Administrator Console, SEDO lock and unlock functions occur automatically.
If you use Windows PowerShell cmdlets in a multiple-site environment, we recommend that you lock and unlock objects to prevent inadvertent overwriting of data.
If you want to edit and save a SEDO-enabled object, you must lock the object.
When you obtain the lock, the lock is assigned to you, your computer and the site in which the computer resides.
While the lock is assigned to you, no other user or computer can edit the object until you release the lock.

## EXAMPLES

### Example 1: Lock a global object
```
PS C:\> $CIObj = Get-CMDriverPackage -Id "CM100042"
PS C:\> Lock-CMObject -InputObject $CIObj
```

The first command gets the driver package object that has the ID CM100042, and stores the object in the $CIObj variable.

The second command locks the object stored in $CIObj.

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

### -InputObject
Specifies an array of Configuration Manager objects output from another cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
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

[Unlock-CMObject](xref:ConfigurationManager/vlatest/Unlock-CMObject.md)


