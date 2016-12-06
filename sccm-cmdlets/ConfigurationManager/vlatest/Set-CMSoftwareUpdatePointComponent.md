---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834096
schema: 2.0.0
ms.assetid: 06300983-C58D-4402-A33C-E37968FF9FD2
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMSoftwareUpdatePointComponent.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMSoftwareUpdatePointComponent.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMSoftwareUpdatePointComponent

## SYNOPSIS
Modifies a software update point.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Set-CMSoftwareUpdatePointComponent [-SiteCode <String>] [-DefaultWsusServer <String>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>]
 [-ReportingEvent <ReportingEventType>] [-RemoveUpdateClassification <String[]>]
 [-AddUpdateClassification <String[]>] [-AddCompany <String[]>] [-RemoveCompany <String[]>]
 [-AddProductFamily <String[]>] [-RemoveProductFamily <String[]>] [-AddProduct <String[]>]
 [-RemoveProduct <String[]>] [-EnableSynchronization <Boolean>] [-Schedule <IResultObject>]
 [-EnableSyncFailureAlert <Boolean>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-WaitMonth <Int32>] [-AddLanguageUpdateFile <String[]>]
 [-RemoveLanguageUpdateFile <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-RemoveLanguageSummaryDetail <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMSoftwareUpdatePointComponent -Name <String> [-DefaultWsusServer <String>]
 [-SynchronizeAction <SynchronizeActionType>] [-UpstreamSourceLocation <String>]
 [-ReportingEvent <ReportingEventType>] [-RemoveUpdateClassification <String[]>]
 [-AddUpdateClassification <String[]>] [-AddCompany <String[]>] [-RemoveCompany <String[]>]
 [-AddProductFamily <String[]>] [-RemoveProductFamily <String[]>] [-AddProduct <String[]>]
 [-RemoveProduct <String[]>] [-EnableSynchronization <Boolean>] [-Schedule <IResultObject>]
 [-EnableSyncFailureAlert <Boolean>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-WaitMonth <Int32>] [-AddLanguageUpdateFile <String[]>]
 [-RemoveLanguageUpdateFile <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-RemoveLanguageSummaryDetail <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMSoftwareUpdatePointComponent [-DefaultWsusServer <String>] [-SynchronizeAction <SynchronizeActionType>]
 [-UpstreamSourceLocation <String>] [-ReportingEvent <ReportingEventType>]
 [-RemoveUpdateClassification <String[]>] [-AddUpdateClassification <String[]>] [-AddCompany <String[]>]
 [-RemoveCompany <String[]>] [-AddProductFamily <String[]>] [-RemoveProductFamily <String[]>]
 [-AddProduct <String[]>] [-RemoveProduct <String[]>] [-EnableSynchronization <Boolean>]
 [-Schedule <IResultObject>] [-EnableSyncFailureAlert <Boolean>] [-ImmediatelyExpireSupersedence <Boolean>]
 [-EnableCallWsusCleanupWizard <Boolean>] [-WaitMonth <Int32>] [-AddLanguageUpdateFile <String[]>]
 [-RemoveLanguageUpdateFile <String[]>] [-AddLanguageSummaryDetail <String[]>]
 [-RemoveLanguageSummaryDetail <String[]>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdatePointComponent** cmdlet modifies a software update point.
A software update point component interacts with a Windows Server Update Services (WSUS) server to configure update settings, request synchronization to the upstream update source, and synchronize updates from the WSUS database to the site server database on the central site.

You can specify a software update point to modify by name, by site code, or by using the Get-CMSoftwareUpdatePointComponent cmdlet.

## EXAMPLES

### Example 1: Modify a software update point
```
PS C:\>$CIObj = Get-CMSoftwareUpdatePointComponent -SiteSystemServerName "Contoso-SiteSysSrv.Western.Contoso.com"
PS C:\> Set-CMSoftwareUpdatePointComponent -InputObject $CIObj
```

The first command retrieves a software update point component object on the server named Contoso-SiteSysSrv.TSQA.Contoso.com.
The command stores the object in the **$CIObj** variable.

The second command modifies the software update point component in **$CIObj**.

## PARAMETERS

### -AddCompany


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddCompanies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguageSummaryDetail


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddLanguageSummaryDetails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddLanguageUpdateFile
Specifies an array of languages, as strings.
The cmdlet adds these languages to the languages supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddProduct


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddProducts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddProductFamily


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddProductFamilies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddUpdateClassification
Specifies an array of software update classifications, as strings.
This cmdlet adds these classifications to the classifications supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Critical Updates, Definition Updates, Feature Packs, Security Updates, Service Packs, Tools, Update Rollups, Updates, Upgrades

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

### -DefaultWsusServer


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

### -EnableCallWsusCleanupWizard


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSyncFailureAlert
Indicates whether Configuration Manager creates an alert when synchronization fails on a site.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSynchronization
Indicates whether this site automatically synchronizes updates according to a schedule.
Specify a schedule by using the *Schedule* parameter.

```yaml
Type: Boolean
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

### -ImmediatelyExpireSupersedence
Indicates whether a software update expires immediately after another update supersedes it or after a specified period of time.
If you specify a value of $False for this parameter, specify the number of months to wait for expiration by using the *WaitMonth* parameter.

System Center 2016 Endpoint Protection definition updates and software updates that Service Packs supersede never expire.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software update point component object.
To obtain a software update point component object, use the **Get-CMSoftwareUpdatePointComponent** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Site, SiteComponent

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name of a site system server in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveCompany


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveCompanies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLanguageSummaryDetail


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveLanguageSummaryDetails

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveLanguageUpdateFile
Specifies an array of languages, as strings.
The cmdlet removes these languages from the languages supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveProduct


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveProducts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveProductFamily


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveProductFamilies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveUpdateClassification
Specifies an array of software update classifications, as strings.
This cmdlet removes these classifications from the classifications supported for software updates at this site.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Critical Updates, Definition Updates, Feature Packs, Security Updates, Service Packs, Tools, Update Rollups, Updates, Upgrades

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportingEvent
Specifies whether to create event messages for WSUS reporting for status reporting events or for all reporting events.
The acceptable values for this parameter are:

- CreateAllWsusReportingEvents
- CreateOnlyWsusStatusReportingEvents
- DoNotCreateWsusReportingEvents

```yaml
Type: ReportingEventType
Parameter Sets: (All)
Aliases: 
Accepted values: DoNotCreateWsusReportingEvents, CreateOnlyWsusStatusReportingEvents, CreateAllWsusReportingEvents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a **Schedule** object.
Configuration Manager can synchronize updates according this schedule if you specify a value of $True for the *EnableSynchronization* parameter.
To obtain a **Schedule** object, use the New-CMSchedule cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SynchronizeAction
Specifies a source for synchronization for this software update point.
The acceptable values for this parameter are:

- DoNotSynchronizeFromMicrosoftUpdateOrUpstreamDataSource
- SynchronizeFromAnUpstreamDataSourceLocation
---SynchronizeFromMicrosoftUpdate

If you select a value of SynchronizeFromAnUpstreamDataSourceLocation, specify the data source location by using the **UpstreamSourceLocation** parameter.

```yaml
Type: SynchronizeActionType
Parameter Sets: (All)
Aliases: 
Accepted values: SynchronizeFromMicrosoftUpdate, SynchronizeFromAnUpstreamDataSourceLocation, DoNotSynchronizeFromMicrosoftUpdateOrUpstreamDataSource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpstreamSourceLocation
Specifies an upstream data location as a URL.
To use this location, specify a value of SynchronizeFromAnUpstreamDataSourceLocation for the *SynchronizeAction* parameter.

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

### -WaitMonth
Specifies how long, in months, to wait before a software update expires after another update supersedes it.
Specify a value of $True for the *ImmediatelyExpireSupersedence* parameter for software updates to expire immediately.

Endpoint Protection definition updates and software updates that Service Packs supersede never expire.

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

[Get-CMSoftwareUpdatePointComponent](xref:ConfigurationManager/vlatest/Get-CMSoftwareUpdatePointComponent.md)

[New-CMSchedule](xref:ConfigurationManager/vlatest/New-CMSchedule.md)

[Set-CMCollectionMembershipEvaluationComponent](xref:ConfigurationManager/vlatest/Set-CMCollectionMembershipEvaluationComponent.md)

[Set-CMEmailNotificationComponent](xref:ConfigurationManager/vlatest/Set-CMEmailNotificationComponent.md)

[Set-CMManagementPointComponent](xref:ConfigurationManager/vlatest/Set-CMManagementPointComponent.md)

[Set-CMOutOfBandManagementComponent](xref:ConfigurationManager/vlatest/Set-CMOutOfBandManagementComponent.md)

[Set-CMStatusReportingComponent](xref:ConfigurationManager/vlatest/Set-CMStatusReportingComponent.md)

[Set-CMSystemHealthValidatorPointComponent](xref:ConfigurationManager/vlatest/Set-CMSystemHealthValidatorPointComponent.md)


