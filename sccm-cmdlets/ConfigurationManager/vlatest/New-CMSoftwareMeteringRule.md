---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833755
schema: 2.0.0
ms.assetid: 13FECF2C-1A82-4A61-B717-F91AE4C9F94D
updated_at: 12/6/2016 7:33 PM
ms.date: 12/6/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/New-CMSoftwareMeteringRule.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/504fd5ae0c4dcc14877d18b3f201f0c5172688ce/sccm-cmdlets/ConfigurationManager/vlatest/New-CMSoftwareMeteringRule.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# New-CMSoftwareMeteringRule

## SYNOPSIS
Creates a Configuration Manager software metering rule.

## SYNTAX

### New (Default)
```
New-CMSoftwareMeteringRule -ProductName <String> [-FileName <String>] [-OriginalFileName <String>]
 [-FileVersion <String>] [-LanguageId <Int32>] [-Comment <String>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewFromPath
```
New-CMSoftwareMeteringRule [-ProductName <String>] [-SiteCode <String>] -Path <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSoftwareMeteringRule** cmdlet creates a Microsoft System Center Configuration Manager software metering rule.
A software metering rule specifies a piece of software, along with version information.
You can obtain necessary file information from Windows Explorer.

Software metering monitors and collects software usage data from System Center Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

For more information about software metering in System Center Configuration Manager, see [Introduction to Software Metering in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268432) on TechNet.

## EXAMPLES

### Example 1: Create a software metering rule
```
PS C:\>New-CMSoftwareMeteringRule -Path "Notepad.exe" -SiteCode "CM1" -FileVersion "6.1.7600.16385" -OriginalFileName "NOTEPAD.EXE" -ProductName "Microsoft Windows Operating System" 
ApplyToChildSites : True
Comment           : 
Enabled           : True
FileName          : Notepad.exe
FileVersion       : 6.1.7600.16385
LanguageID        : 
LastUpdateTime    : 
OriginalFileName  : NOTEPAD.EXE
ProductName       : Microsoft Windows Operating System
RuleID            : 
SecurityKey       : 
SiteCode          : CM1
SourceSite        :
```

This command creates a software metering rule for the System Center Configuration Manager site named CM1.
The command specifies the file name, version, original file name, and product name for the software product.

## PARAMETERS

### -Comment
Specifies a comment for a software metering rule.

```yaml
Type: String
Parameter Sets: New
Aliases: 
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

### -FileName


```yaml
Type: String
Parameter Sets: New
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileVersion
Specifies a version of the software that a rule meters.

```yaml
Type: String
Parameter Sets: New
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

### -LanguageId
Specifies a LocaleID of the software that a rule meters.
For more information and a list of locale identifiers, see the Locale IDs Assigned by Microsoft topic at [http://go.microsoft.com/fwlink/?LinkId=262651](http://go.microsoft.com/fwlink/?LinkId=262651).

```yaml
Type: Int32
Parameter Sets: New
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OriginalFileName
Specifies an original file name of the software that a rule meters.
This parameter can differ from the *Path* parameter if a user changed the name.

```yaml
Type: String
Parameter Sets: New
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies a file path of the software that a rule meters.

```yaml
Type: String
Parameter Sets: NewFromPath
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductName
Specifies a name for a product that a rule meters.

```yaml
Type: String
Parameter Sets: New
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NewFromPath
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

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

[Disable-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Disable-CMSoftwareMeteringRule.md)

[Enable-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Enable-CMSoftwareMeteringRule.md)

[Get-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Get-CMSoftwareMeteringRule.md)

[Remove-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Remove-CMSoftwareMeteringRule.md)

[Set-CMSoftwareMeteringRule](xref:ConfigurationManager/vlatest/Set-CMSoftwareMeteringRule.md)


