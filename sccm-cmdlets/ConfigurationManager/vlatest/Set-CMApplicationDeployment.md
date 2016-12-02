---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833636
schema: 2.0.0
ms.assetid: B77A46FA-BA17-4E39-AC41-267AB0D3A353
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMApplicationDeployment.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMApplicationDeployment.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMApplicationDeployment

## SYNOPSIS
Modifies properties for an application deployment in Configuration Manager.

## SYNTAX

### SetApplicationDeploymentByValueMandatory (Default)
```
Set-CMApplicationDeployment -InputObject <IResultObject> [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-Comment <String>] [-RequireApproval <Boolean>] [-PreDeploy <Boolean>]
 [-SendWakeUpPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-TimeBaseOn <TimeType>]
 [-AvailableDate <DateTime>] [-AvailableTime <DateTime>] [-DeadlineDate <DateTime>] [-DeadlineTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-OverrideServiceWindow <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-CreateAlertBaseOnPercentSuccess <Boolean>] [-SuccessParameterValue <Int32>] [-PostponeDate <DateTime>]
 [-PostponeTime <DateTime>] [-CreateAlertBaseOnPercentFailure <Boolean>] [-FailParameterValue <Int32>]
 [-EnableMomAlert <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetApplicationDeploymentByNameMandatory
```
Set-CMApplicationDeployment -ApplicationName <String> [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-Comment <String>] [-RequireApproval <Boolean>] [-PreDeploy <Boolean>]
 [-SendWakeUpPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-TimeBaseOn <TimeType>]
 [-AvailableDate <DateTime>] [-AvailableTime <DateTime>] [-DeadlineDate <DateTime>] [-DeadlineTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-OverrideServiceWindow <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-CreateAlertBaseOnPercentSuccess <Boolean>] [-SuccessParameterValue <Int32>] [-PostponeDate <DateTime>]
 [-PostponeTime <DateTime>] [-CreateAlertBaseOnPercentFailure <Boolean>] [-FailParameterValue <Int32>]
 [-EnableMomAlert <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetApplicationDeploymentByIdMandatory
```
Set-CMApplicationDeployment -ApplicationId <String> [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-Comment <String>] [-RequireApproval <Boolean>] [-PreDeploy <Boolean>]
 [-SendWakeUpPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-TimeBaseOn <TimeType>]
 [-AvailableDate <DateTime>] [-AvailableTime <DateTime>] [-DeadlineDate <DateTime>] [-DeadlineTime <DateTime>]
 [-UserNotification <UserNotificationType>] [-OverrideServiceWindow <Boolean>]
 [-RebootOutsideServiceWindow <Boolean>] [-PersistOnWriteFilterDevice <Boolean>]
 [-CreateAlertBaseOnPercentSuccess <Boolean>] [-SuccessParameterValue <Int32>] [-PostponeDate <DateTime>]
 [-PostponeTime <DateTime>] [-CreateAlertBaseOnPercentFailure <Boolean>] [-FailParameterValue <Int32>]
 [-EnableMomAlert <Boolean>] [-RaiseMomAlertsOnFailure <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMApplicationDeployment** cmdlet modifies properties for an application deployment in Microsoft System Center Configuration Manager.
An application deployment installs an application according to schedule for a several computers.
Application deployments can also allow users to install at a time they choose.

To specify an application deployment to modify, specify the collection name and the application.
You can specify an application by name or ID, or you can use the Get-CMApplication cmdlet to get an application to modify.

## EXAMPLES

### Example 1: Modify availability and deadline for an application deployment
```
PS C:\>Set-CMApplicationDeployment -ApplicationName "Track System 2011" -CollectionName "All Users" -AvaliableDate 2012/10/21 -AvaliableTime 17:25 -DeadlineDate 2013/01/01 -DeadlineTime 13:10
```

This command modifies an application deployment for an application named Track System 2011 for a collection named All Users.
The command specifies the date and time when the application becomes available and the date and time of a deadline for deployment.

## PARAMETERS

### -ApplicationId
Specifies the ID of an application.

```yaml
Type: String
Parameter Sets: SetApplicationDeploymentByIdMandatory
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
Parameter Sets: SetApplicationDeploymentByNameMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableDate


```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: AvaliableDate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableTime


```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: AvaliableTime

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection


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

### -CollectionId


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

### -CollectionName
Specifies the name of device collection or user collection.

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

### -Comment
Specifies a comment for the deployment.

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

### -CreateAlertBaseOnPercentFailure
Indicates whether to create an alert for a percentage of the applications that fail to deploy.
Enter the percentage value by using the *FailParameterValue* parameter.

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

### -CreateAlertBaseOnPercentSuccess
Indicates whether to create an alert for a percentage of the applications that deploy successfully.
Enter the percentage value by using the *SuccessParameterValue* parameter.

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

### -DeadlineDate
Specifies a date as a **DateTime** object.
To obtain a **DateTime** object, use the Get-Date cmdlet.
This is the deadline for deployment of the application.
If the application has not deployed to a client by this date, Configuration Manager forces deployment.
If you specify a value for the *DeadlineTime* parameter in addition to this parameter, the cmdlet uses that value.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeadlineTime
Specifies a time as a **DateTime** object.
To obtain a **DateTime** object, use the Get-Date cmdlet.
This is the deadline for deployment of the application.
If the application has not deployed to a client by this time, Configuration Manager forces deployment.

```yaml
Type: DateTime
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

### -EnableMomAlert
Indicates whether alerts from this cmdlet appear in System Center 2016 - Operations Manager.

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

### -FailParameterValue
Specifies the percentage of failed application installation that causes an alert.
Specify an integer from 1 through 100.
You must also specify the *CreatAlertBaseOnPercentFailure* parameter as $True.

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
Parameter Sets: SetApplicationDeploymentByValueMandatory
Aliases: Application

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OverrideServiceWindow
Indicates whether the deployment takes place even if scheduled outside of a service window.
A service window is a specified period of time used for computer maintenance and updates.
If this value is $True, Configuration Manager deploys the application even the scheduled time falls outside the service window.
If this value is $False, Configuration Manager does not deploy the application outside the service window, but Configuration Manager waits until it can deploy in a service window.

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

### -PassThru


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

### -PersistOnWriteFilterDevice
Indicates whether to enable write filters for embedded devices.
For a value of $True, the device commits changes during a maintenance window.
This action requires a restart.
For a value of $False, the device saves changes in an overlay and commits them later.

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

### -PostponeDate
Specifies a date as a **DateTime** object.
To obtain a **DateTime** object, use the Get-Date cmdlet.
Configuration Manager generates a deployment alert after this length of time.
If you specify a value for the *PostponeTime* parameter in addition to this parameter, the cmdlet uses that value.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PostponeTime
Specifies a time as a **DateTime** object.
To obtain a **DateTime** object, use the Get-Date cmdlet.
Configuration Manager generates a deployment alert after this length of time.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreDeploy
Indicates whether to pre-deploy the application to the primary device of the user.

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

### -RaiseMomAlertsOnFailure
Indicates whether to create an Operations Manager alert if a client fails to install the application.

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

### -RebootOutsideServiceWindow
Indicates whether a computer restarts outside a service window.
A service window is a specified period of time used for computer maintenance and updates.
If this value is $True, any required restart takes place without regard to service windows.
If this value is $False, the computer does not restart outside a service window.

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

### -RequireApproval


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AppRequiresApproval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendWakeUpPacket
Indicates whether to send a wake-up packet to computers before the deployment begins.
If this value is $True, Configuration Manager wakes a computer from sleep.
If this value is $False, it does not wake computers from sleep.
For computers to wake, you must first configure Wake On LAN.

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

### -SuccessParameterValue
Specifies the percentage of successful application installation that causes an alert.
Specify an integer from 0 through 99.
You must also specify the *CreatAlertBaseOnPercentSuccess* parameter as $True.

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

### -TimeBaseOn
Specifies which time zone to use.
The acceptable values for this parameter are:

- LocalTime.
Use local time. 
- UTC.
Use Coordinated Universal Time (UTC), also known as Greenwich Mean Time.

```yaml
Type: TimeType
Parameter Sets: (All)
Aliases: 
Accepted values: LocalTime, Utc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseMeteredNetwork
Indicates whether to allow clients to download content over a metered Internet connection after the deadline, which may incur additional expense.

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

### -UserNotification
Specifies the type of notification for a client.
Valid values are: 

- DisplayAll
- DisplaySoftwareCenterOnly
- HideAll

```yaml
Type: UserNotificationType
Parameter Sets: (All)
Aliases: 
Accepted values: DisplayAll, DisplaySoftwareCenterOnly, HideAll

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

[Get-CMApplication](xref:ConfigurationManager/vlatest/Get-CMApplication.md)

[Start-CMApplicationDeployment](xref:ConfigurationManager/vlatest/Start-CMApplicationDeployment.md)

[Start-CMApplicationDeploymentSimulation](xref:ConfigurationManager/vlatest/Start-CMApplicationDeploymentSimulation.md)


