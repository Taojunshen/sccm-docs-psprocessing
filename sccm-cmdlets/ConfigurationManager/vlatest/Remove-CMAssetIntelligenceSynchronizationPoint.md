---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833912
schema: 2.0.0
ms.assetid: F8A5A3D8-DF47-4073-93A6-632BE7A2570C
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAssetIntelligenceSynchronizationPoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAssetIntelligenceSynchronizationPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Remove-CMAssetIntelligenceSynchronizationPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Remove-CMAssetIntelligenceSynchronizationPoint

## SYNOPSIS
Removes an Asset Intelligence synchronization point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMAssetIntelligenceSynchronizationPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMAssetIntelligenceSynchronizationPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAssetIntelligenceSynchronizationPoint** cmdlet removes an Asset Intelligence synchronization point from a site system.
After you remove an Asset Intelligence synchronization point, the Microsoft System Center Configuration Manager sites that used the synchronization point cannot connect to System Center Online.

## EXAMPLES

### Example 1: Remove an Asset Intelligence synchronization point
```
PS C:\> Remove-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "CMDIV-WEST04.CORP.CONTOSO.COM" -SiteCode "CM1"
```

This command removes the Asset Intelligence synchronization point on the System Center Configuration Manager site that has the site code CM1 on the site system server named CMDIV-WEST04.CORP.CONTOSO.COM.

### Example 2: Remove an Asset Intelligence synchronization point by using an object variable
```
PS C:\> $AIsync = Get-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "WEST04.CORP.CONTOSO.COM" -SiteCode "ST1"
PS C:\> Remove-CMAssetIntelligenceSynchronizationPoint -InputObject $AIsync
```

The first command gets the Asset Intelligence synchronization point on the System Center Configuration Manager site that has the site code ST1 on the site system server named CMDIV-WEST04.CORP.CONTOSO.COM.
The command stores the results in the $AIsync variable.

The second command removes the Asset Intelligence synchronization point stored in the $AIsync variable.

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
Specifies an Asset Intelligence synchronization point object.
To get a **CMAssetIntelligenceSynchronizationPoint** object, use the Get-CMAssetIntelligenceSynchronizationPoint cmdlet.

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

### -SiteCode
Specifies the three-letter site code of the Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies an array of fully qualified domain names (FQDN) of the servers that host the site system role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName
Required: True
Position: 0
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

[Add-CMAssetIntelligenceSynchronizationPoint](xref:ConfigurationManager/vlatest/Add-CMAssetIntelligenceSynchronizationPoint.md)

[Get-CMAssetIntelligenceSynchronizationPoint](xref:ConfigurationManager/vlatest/Get-CMAssetIntelligenceSynchronizationPoint.md)

[Set-CMAssetIntelligenceSynchronizationPoint](xref:ConfigurationManager/vlatest/Set-CMAssetIntelligenceSynchronizationPoint.md)


