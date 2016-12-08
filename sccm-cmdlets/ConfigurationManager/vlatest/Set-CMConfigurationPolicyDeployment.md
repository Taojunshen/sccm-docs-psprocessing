---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833771
schema: 2.0.0
ms.assetid: F8D992C0-0F8C-40B7-944A-7BA571735859
updated_at: 12/8/2016 3:33 AM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMConfigurationPolicyDeployment.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/3f2e54f6163618b87e89b0d1fa27e9897f65a1e2/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMConfigurationPolicyDeployment.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMConfigurationPolicyDeployment

## SYNOPSIS
Creates a configuration policy deployment.

## SYNTAX

### SetFWPolicyDeploymentByValueMandatory (Default)
```
Set-CMConfigurationPolicyDeployment -FirewallPolicy <IResultObject> -CollectionName <String>
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetUSMPolicyDeploymentByNameMandatory
```
Set-CMConfigurationPolicyDeployment -UserDataAndProfileName <String> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetUSMPolicyDeploymentByIdMandatory
```
Set-CMConfigurationPolicyDeployment -UserDataAndProfileId <String> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetUSMPolicyDeploymentByValueMandatory
```
Set-CMConfigurationPolicyDeployment -UserDataAndProfile <IResultObject> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetFWPolicyDeploymentByNameMandatory
```
Set-CMConfigurationPolicyDeployment -FirewallPolicyName <String> -CollectionName <String>
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetFWPolicyDeploymentByIdMandatory
```
Set-CMConfigurationPolicyDeployment -FirewallPolicyId <String> -CollectionName <String>
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMConfigurationPolicyDeployment** cmdlet creates a configuration policy deployment in Microsoft System Center Configuration Manager.
You can deploy firewall policies or user session management policies.
Use the [Start-CMConfigurationPolicyDeployment](./Start-CMConfigurationPolicyDeployment.md) cmdlet to deploy specified policies for a System Center Configuration Manager collection.

## EXAMPLES

### Example 1: Create a configuration policy deployment
```
PS C:\>Set-CMConfigurationPolicyDeployment -CollectionName "Regional Remote Users" -FirewallPolicyName "Remote Firewall Policy"
```

This command creates a configuration policy deployment named Remote Firewall Policy and deploys it to the collection named Regional Remote Users.

## PARAMETERS

### -CollectionName
Specifies the name of a collection.
The deployment applies to this collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
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

### -EnableEnforcement
Indicates whether to enable enforcement for the deployment.
During enforcement, a client reports compliance information about a deployment.

```yaml
Type: Boolean
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory, SetUSMPolicyDeploymentByIdMandatory, SetUSMPolicyDeploymentByValueMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicy
Specifies a Windows Firewall Policy object.
To obtain a **CMWindowsFirewallPolicy** object, use the [Get-CMWindowsFirewallPolicy](./Get-CMWindowsFirewallPolicy.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetFWPolicyDeploymentByValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyId
Specifies the ID of a Windows Firewall policy.

```yaml
Type: String
Parameter Sets: SetFWPolicyDeploymentByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyName
Specifies the name of a Windows Firewall policy.

```yaml
Type: String
Parameter Sets: SetFWPolicyDeploymentByNameMandatory
Aliases: 
Required: True
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

### -GenerateAlert
Indicates whether Configuration Manager generates alerts during the deployment.

```yaml
Type: Boolean
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory, SetUSMPolicyDeploymentByIdMandatory, SetUSMPolicyDeploymentByValueMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitoredByScom
Indicates whether System Center 2016 - Operations Manager monitoring criteria applies during the deployment.

```yaml
Type: Boolean
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory, SetUSMPolicyDeploymentByIdMandatory, SetUSMPolicyDeploymentByValueMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideServiceWindow
Indicates whether to override the service window while deploying policies.
Service windows are periods of time allocated for maintenance.

```yaml
Type: Boolean
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory, SetUSMPolicyDeploymentByIdMandatory, SetUSMPolicyDeploymentByValueMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParameterValue
Specifies the values of administrator-defined parameters, such as thresholds.
Configuration Manager stores the values in XML format.

```yaml
Type: Int32
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory, SetUSMPolicyDeploymentByIdMandatory, SetUSMPolicyDeploymentByValueMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -PostponeDate
Specifies a date, as a **DateTime** object, for the deployment if it is postponed.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.
For more information, type `Get-Help Get-Date`.

```yaml
Type: DateTime
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory, SetUSMPolicyDeploymentByIdMandatory, SetUSMPolicyDeploymentByValueMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PostponeTime
Specifies a time, as a **DateTime** object, for the deployment if it is postponed.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.

```yaml
Type: DateTime
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory, SetUSMPolicyDeploymentByIdMandatory, SetUSMPolicyDeploymentByValueMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a schedule object.
This is the schedule for deploying the configuration policy.
You can use the [New-CMSchedule](./New-CMSchedule.md) cmdlet to create a schedule token.

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

### -UserDataAndProfile
Specifies a user data and profiles configuration item object.
To obtain a **CMUserDataAndProfileConfigurationItem** object, use the [Get-CMUserDataAndProfileConfigurationItem](./Get-CMUserDataAndProfileConfigurationItem.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetUSMPolicyDeploymentByValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -UserDataAndProfileId
Specifies an ID of a user data and profile configuration item.

```yaml
Type: String
Parameter Sets: SetUSMPolicyDeploymentByIdMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDataAndProfileName
Specifies a name of a user data and profile configuration item.

```yaml
Type: String
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory
Aliases: 
Required: True
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

[Get-CMUserDataAndProfileConfigurationItem](xref:ConfigurationManager/vlatest/Get-CMUserDataAndProfileConfigurationItem.md)

[Get-CMWindowsFirewallPolicy](xref:ConfigurationManager/vlatest/Get-CMWindowsFirewallPolicy.md)
 
[New-CMSchedule](xref:ConfigurationManager/vlatest/New-CMSchedule.md)

[Start-CMConfigurationPolicyDeployment](xref:ConfigurationManager/vlatest/Start-CMConfigurationPolicyDeployment.md)
