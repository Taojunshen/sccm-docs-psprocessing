---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833750
schema: 2.0.0
ms.assetid: EE34D675-431A-4CE6-A3C0-3114CF29C023
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMMdmEnrollmentManager.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMMdmEnrollmentManager.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMMdmEnrollmentManager

## SYNOPSIS
Gets a Device Enrollment Manager.

## SYNTAX

### ByName (Default)
```
Get-CMMdmEnrollmentManager [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByValue
```
Get-CMMdmEnrollmentManager -Id <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMdmEnrollmentManger** cmdlet gets one or more Device Enrollment Managers.

## EXAMPLES

### Example 1: Get a device enrollment manager by name
```
PS C:\> Get-CMMdmEnrollmentManager -name "Contoso\User01"
```

This command gets the device enrollment manager named User01.

### Example 2: Get a device enrollment manager by ID
```
PS C:\>Get-CMMdmEnrollmentManager -ID "1234567890"
```

This command gets the device enrollment manager named 1234567890.

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
Specifies an array of Configuration Manager user IDs.

```yaml
Type: Int32[]
Parameter Sets: ByValue
Aliases: Ids, ResourceId, ResourceIds
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a Configuration Manager user.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 
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

### IResultObject#SMS_MDMDeviceEnrollmentManagers

## NOTES

## RELATED LINKS

[Add-CMMdmEnrollmentManager](xref:ConfigurationManager/vlatest/Add-CMMdmEnrollmentManager.md)

[Remove-CMMdmEnrollmentManager](xref:ConfigurationManager/vlatest/Remove-CMMdmEnrollmentManager.md)


