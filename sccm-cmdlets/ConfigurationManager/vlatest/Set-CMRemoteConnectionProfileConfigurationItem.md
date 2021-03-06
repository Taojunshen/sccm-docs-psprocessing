---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834002
schema: 2.0.0
ms.assetid: 7B4B13D3-569E-4121-8210-8E3E045DBCFF
updated_at: 12/8/2016 6:40 PM
ms.date: 12/8/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMRemoteConnectionProfileConfigurationItem.md
original_content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMRemoteConnectionProfileConfigurationItem.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0205e569abecf1b4e1b2b342947b87a3691b29a5/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMRemoteConnectionProfileConfigurationItem.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: True
ms.service: configuration-manager
---

# Set-CMRemoteConnectionProfileConfigurationItem

## SYNOPSIS
Modifies a remote connection profile.

## SYNTAX

### SetByValue (Default)
```
Set-CMRemoteConnectionProfileConfigurationItem [-InputObject] <IResultObject> [-EnableNla <Boolean>]
 [-EnablePrimaryUser <Boolean>] [-EnableTSFirewallRule <Boolean>] [-EnableTSConnection <Boolean>]
 [-Enable <Boolean>] [-RDGatewayServer <String>] [-Description <String>] [-Digest <ConfigurationItem>]
 [-DigestPath <String>] [-DigestXml <String>] [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMRemoteConnectionProfileConfigurationItem [-EnableNla <Boolean>] [-EnablePrimaryUser <Boolean>]
 [-EnableTSFirewallRule <Boolean>] [-EnableTSConnection <Boolean>] [-Enable <Boolean>]
 [-RDGatewayServer <String>] [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-Id] <Int32> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMRemoteConnectionProfileConfigurationItem [-EnableNla <Boolean>] [-EnablePrimaryUser <Boolean>]
 [-EnableTSFirewallRule <Boolean>] [-EnableTSConnection <Boolean>] [-Enable <Boolean>]
 [-RDGatewayServer <String>] [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-Name] <String> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMRemoteConnectionProfileConfigurationItem** cmdlet modifies a remote connection profile.
Client computers use remote connection profiles to remotely connect to computers from outside the domain or over the Internet.

## EXAMPLES

### Example 1: Modify a remote connection profile configuration item
```
PS C:\> Set-CMRemoteConnectionProfileConfigurationItem -ID "AAA0004D" -EnablePrimaryUsers $False -EnableTSConnection $False -EnableTSFirewallRule $False
```

This command modifies the remote connection profile configuration item with the ID AAA0004D.
In this case, the *EnablePrimaryUsers*, *EnableTSConnection*, and *EnableTSFirewallRule* properties are all set to $False.

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

### -Description
Specifies a description for a remote connection profile.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digest


```yaml
Type: ConfigurationItem
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DigestPath


```yaml
Type: String
Parameter Sets: (All)
Aliases: DesiredConfigurationDigestPath
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DigestXml


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

### -Enable


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableConnectionSettings
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNla
Indicates whether to allow connections only from computers that run Remote Desktop by using Network Level Authentication.

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

### -EnablePrimaryUser


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnablePrimaryUsers
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableTSConnection
Indicates whether to allow remote connections to client computers.
If you specify a value for this parameter, you must specify values for the *EnablePrimaryUsers* and *EnableTSFirewallRule* parameters.

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

### -EnableTSFirewallRule
Indicates whether to allow Windows Firewall exceptions for connections in Windows domains and on private networks.
If you specify a value for this parameter, you must specify values for the *EnablePrimaryUsers* and *EnableTSConnections* parameters.

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

### -Id
Specifies an array of IDs for remote connection profiles.

```yaml
Type: Int32
Parameter Sets: SetById
Aliases: CIId, CI_ID
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a remote connection profile object.
To obtain a remote connection profile, use the Get-CMRemoteConnectionProfileConfigurationItem cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of remote connection profiles.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: LocalizedDisplayName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies the new name for the remote connection profile.

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

### -RDGatewayServer
Specifies the host name and port of the Remote Desktop gateway server, for example, Boston.gateway.Contoso.com:8080.

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

[New-CMRemoteConnectionProfileConfigurationItem](xref:ConfigurationManager/vlatest/New-CMRemoteConnectionProfileConfigurationItem.md)
