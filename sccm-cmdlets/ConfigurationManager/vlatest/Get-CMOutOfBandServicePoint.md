---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833805
schema: 2.0.0
ms.assetid: 7EED830A-6F36-4870-9160-155E2F6AB6A8
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMOutOfBandServicePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMOutOfBandServicePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Get-CMOutOfBandServicePoint

## SYNOPSIS
Gets an out of band service point.

## SYNTAX

### SearchByName
```
Get-CMOutOfBandServicePoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMOutOfBandServicePoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOutOfBandServicePoint** cmdlet gets an out of band service point.
An out of band service point is a site system role that provisions and configures Intel Active Management Technology (AMT)-based computers for Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get an out of band service point
```
PS C:\>Get-CMOutOfBandServicePoint -SiteSystemServerName "cmcen-dist02.tsqa.corp.contoso.com" -SiteCode "CM1" >>\Results\Get-CMOutOfBandServicePoint_data.txt"
```

This command get an out of band service point that is associated with the site system named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM and the site code CM1.
The command directs the output to the text file Get-CMOutOfBandServicePoint_data.txt.

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

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName
Required: False
Position: 0
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

[Set-CMOutOfBandServicePoint](xref:ConfigurationManager/vlatest/Set-CMOutOfBandServicePoint.md)

[Add-CMOutOfBandServicePoint](xref:ConfigurationManager/vlatest/Add-CMOutOfBandServicePoint.md)

[Remove-CMOutOfBandServicePoint](xref:ConfigurationManager/vlatest/Remove-CMOutOfBandServicePoint.md)


