---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833849
schema: 2.0.0
ms.assetid: A52F6FB6-F290-40F9-AE6C-2026EF88AF06
updated_at: 12/7/2016 11:03 PM
ms.date: 12/7/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMEnrollmentPoint.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/0be8f3cf2157376220d368547d702e97388a8421/sccm-cmdlets/ConfigurationManager/vlatest/Set-CMEnrollmentPoint.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
manager: mbaldwin
open_to_public_contributors: true
ms.service: configuration-manager
---

# Set-CMEnrollmentPoint

## SYNOPSIS
Sets an enrollment point in Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMEnrollmentPoint [-UserName <String>] [-UseComputerAccount] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMEnrollmentPoint [-SiteCode <String>] [-SiteSystemServerName] <String> [-UserName <String>]
 [-UseComputerAccount] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMEnrollmentPoint** cmdlet sets an enrollment point in Microsoft System Center Configuration Manager.
An enrollment point is a site system role that uses public key infrastructure (PKI) certificates to complete mobile device enrollment and to provision Intel AMT-based computers.

## EXAMPLES

### Example 1: Set an enrollment point
```
PS C:\>Set-CMEnrollmentPoint -SiteSystemServerName "CM-Contoso.Contoso.Com" -SiteCode "CM2" -UserName "Contoso\ElisaDaugherty"
```

The command sets an enrollment point, and specifies an account name to use to connect to the Configuration Manager database.

### Example 2: Set an enrollment point with the computer account
```
PS C:\>Set-CMEnrollmentPoint -SiteSystemServerName "CM-Contoso.Contoso.Com" -SiteCode "CM2" -UseComputerAccount
```

The command sets an enrollment point by specifying the site system server and site code, and uses the computer account to connect to the Configuration Manager database.

### Example 3: Set an enrollment point by using an input object
```
PS C:\>$Ep = Get-CMEnrollmentPoint -SiteSystemServerName "CM-Contoso.Contoso.Com" -SiteCode "CM2" 
PS C:\> Set-CMEnrollmentPoint -InputObject $Ep -UserName "Contoso\ElisaDaugherty"
```

The first command uses the **Get-CMEnrollmentPoint** cmdlet to get an enrollment point, and stores the result in the $Ep variable.

The second command sets an enrollment point for a server by using the input object stored in the $Ep variable.

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
Specifies an input object.
To get an input object, use the [Get-CMEnrollmentPoint](./Get-CMEnrollmentPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: EnrollmentPoint
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseComputerAccount
Indicates that you use the computer account to connect to the Configuration Manager database.

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

### -UserName
Specifies a user account that the enrollment point uses to connect to the Configuration Manager database.

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

[Add-CMEnrollmentPoint](xref:ConfigurationManager/vlatest/Add-CMEnrollmentPoint.md)

[Get-CMEnrollmentPoint](xref:ConfigurationManager/vlatest/Get-CMEnrollmentPoint.md)

[Remove-CMEnrollmentPoint](xref:ConfigurationManager/vlatest/Remove-CMEnrollmentPoint.md)
