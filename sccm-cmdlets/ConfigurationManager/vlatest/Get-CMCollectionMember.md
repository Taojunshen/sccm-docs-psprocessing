---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834230
schema: 2.0.0
ms.assetid: 60C6778B-12CB-4F15-846D-3B8ED4AC58A8
updated_at: 3/14/2017 5:56 PM
ms.date: 3/14/2017
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCollectionMember.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/live/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCollectionMember.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/ccf61168e86d4120cdc26f0ffd9b7560e92d36b5/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMCollectionMember.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMCollectionMember

## SYNOPSIS
Gets a member of a collection.

## SYNTAX

### ByCollectionName
```
Get-CMCollectionMember -CollectionName <String> [-Name <String>] [-SmsId <String>] [-ResourceId <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionId
```
Get-CMCollectionMember -CollectionId <String> [-Name <String>] [-SmsId <String>] [-ResourceId <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollection
```
Get-CMCollectionMember -InputObject <IResultObject> [-Name <String>] [-SmsId <String>] [-ResourceId <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCollectionMember** cmdlet gets a member of a collection.

## EXAMPLES

### Example 1: Get a member of a collection by using the pipeline operator
```
PS C:\> Get-CMCollection -Name "UserCol1" | Get-CMCollectionMember
```

This command gets the collection object named UserCol1 and uses the pipeline operator to pass the object to **Get-CMCollectionMember**, which gets all members in UserCol1.

### Example 2: Get a member of a collection by name
```
PS C:\> Get-CMCollectionMember -CollectionName "DeviceCol1" -Name "domain*"
```

This command gets the all members of the device collection named DeviceCol1 that have a name beginning with domain.

## PARAMETERS

### -CollectionId
Specifies the ID of a collection.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a collection.

```yaml
Type: String
Parameter Sets: ByCollectionName
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

### -InputObject
Specifies a collection object.
To obtain a collection object, use the Get-CMCollection, Get-CMDeviceCollection or Get-CMUserCollection cmdlets.

```yaml
Type: IResultObject
Parameter Sets: ByCollection
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a resource.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifies the ID of a resource.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SmsId
Specifies the SMSID of a resource.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCollection](xref:ConfigurationManager/vlatest/Get-CMCollection.md)

[Get-CMDeviceCollection](xref:ConfigurationManager/vlatest/Get-CMDeviceCollection.md)

[Get-CMUserCollection](xref:ConfigurationManager/vlatest/Get-CMUserCollection.md)


