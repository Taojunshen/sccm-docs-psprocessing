---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833947
schema: 2.0.0
ms.assetid: B0A665E8-148A-4848-9923-7F80EAB27A4F
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMMulticastServicePoint.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMMulticastServicePoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMMulticastServicePoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMMulticastServicePoint

## SYNOPSIS
Sets a multicast service point.

## SYNTAX

### ByValue (Default)
```
Set-CMMulticastServicePoint [-ClientTransferRate <NetworkProfile>] [-EndIPAddress <String>]
 [-EndUdpPort <Int32>] [-InputObject] <IResultObject> [-EnableScheduledMulticast <Boolean>]
 [-MinimumClientCount <Int32>] [-MaximumClientCount <Int32>] [-PassThru] [-SessionStartDelayMins <Int32>]
 [-StartIPAddress <String>] [-StartUdpPort <Int32>] [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMMulticastServicePoint [-ClientTransferRate <NetworkProfile>] [-EndIPAddress <String>]
 [-EndUdpPort <Int32>] [-EnableScheduledMulticast <Boolean>] [-MinimumClientCount <Int32>]
 [-MaximumClientCount <Int32>] [-PassThru] [-SessionStartDelayMins <Int32>] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-StartIPAddress <String>] [-StartUdpPort <Int32>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMMulticastServicePoint** cmdlet updates the configuration of multicast settings for a distribution point.

## EXAMPLES

### Example 1: Modify a multicast service point by using the pipeline
```
PS C:\> Get-CMMulticastServicePoint -SiteSystemServerName "server01.contoso.com" | Set-CMMulticastServicePoint -UserName $null -StartIPAddress 224.0.1.0 -EndIPAddress 239.255.255.255 -StartUdpPort 64001 -EndUdpPort 65000 -ClientTransferRate Profile100Mbps -MaximumClientCount 100 -EnableScheduledMulticast $true -SessionStartDelayMins 15 -MinimumClientCount 20
```

This command gets the multicast service point object with the site system server name server1.contoso.com and uses the pipeline operator to pass the object to **Set-CMMulticastServicePoint**.
**Set-CMMulticastServicePoint** updates the multicast settings on the distribution point object by creating an IP address range of 224.0.1.0 to 239.255.255.255, and a UDP port range of 64001 to 65000.
The command also sets the minimum and maximum client count, and sets a start delay of 15 minutes.

### Example 2: Modify a multicast service point
```
PS C:\> Set-CMMulticastServicePoint -SiteSystemServerName "server02.contoso.com" -UserName "contoso\administrator" -StartIPAddress 224.0.1.0 -EndIPAddress 239.255.255.255 -StartUdpPort 64001 -EndUdpPort 65000 -ClientTransferRate "Profile100Mbps" -MaximumClientCount 100 -EnableScheduledMulticast $true -SessionStartDelayMins 15 -MinimumClientCount 20
```

This command updates the multicast service point settings for the site system server named server1.contoso.com using the administrator account.
The command creates an IP address range of 224.0.1.0 to 239.255.255.255, and a UDP port range of 64001 to 65000.
The command also sets the minimum and maximum client count, and sets a start delay of 15 minutes.

## PARAMETERS

### -ClientTransferRate
No longer used.
Transfer speed is dynamic.

Specifies the client transfer rate.
Valid values are: 

- None
- Profile100Mbps
- Profile10Mbps
- Profile1Gbps 
- ProfileCustom

```yaml
Type: NetworkProfile
Parameter Sets: (All)
Aliases: 
Accepted values: None, ProfileCustom, Profile10Mbps, Profile100Mbps, Profile1Gbps
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

### -EnableScheduledMulticast
Indicates whether you can schedule when Configuration Manager deploys the operating system image from the distribution point.

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

### -EndIPAddress
Specifies the ending IP address in the range of IP addresses that Configuration Manager uses to send data to the destination computers.

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

### -EndUdpPort
Specifies the ending port in the range of user datagram protocol (UDP) ports that Configuration Manager uses to send data to the destination computers.

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
Specifies a multicast service point object.
To obtain a multicast service point object, use the [Get-CMMulticastServicePoint](./Get-CMMulticastServicePoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: MulticastServicePoint
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumClientCount
Specifies the maximum number of destination computers that can download the operating system from this distribution point.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MulticastMaximumClientCount
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumClientCount
Specifies the minimum number of requests that must be received before Configuration Manager starts to deploy the operating system.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinimumSessionSize
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object that represents the multicast service point.
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

### -SessionStartDelayMins
Specifies the number of minutes that Configuration Manager waits before it responds to the first deployment request.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SessionStartDelayMinutes
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for the Configuration Manager site that hosts the site system role.

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

### -SiteSystemServerName
Specifies the name of the server that hosts a site system role.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name, ServerName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartIPAddress
Specifies the starting IP address in the range of IP addresses that Configuration Manager uses to send data to the destination computers.

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

### -StartUdpPort
Specifies the starting port in the range of UDP ports that Configuration Manager uses to send data to the destination computers.

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

### -UserName
Specifies the name of the user that the distribution site system components use to connect to the primary site database.
If the *UserName* parameter is not specified, the cmdlet uses the computer account of the distribution point to the primary site database.

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

[Add-CMMulticastServicePoint](xref:ConfigurationManager/vlatest/Add-CMMulticastServicePoint.md)

[Get-CMMulticastServicePoint](xref:ConfigurationManager/vlatest/Get-CMMulticastServicePoint.md)

[Remove-CMMulticastServicePoint](xref:ConfigurationManager/vlatest/Remove-CMMulticastServicePoint.md)
