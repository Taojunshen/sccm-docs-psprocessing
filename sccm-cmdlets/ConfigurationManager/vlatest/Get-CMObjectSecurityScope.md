---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833786
schema: 2.0.0
ms.assetid: EFE32915-8FDB-4B03-9206-5338A0F0E5A5
updated_at: 11/29/2016 3:46 PM
ms.date: 11/29/2016
content_git_url: https://github.com/Microsoft/sccm-docs-powershell/blob/master/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMObjectSecurityScope.md
gitcommit: https://github.com/Microsoft/sccm-docs-powershell/blob/be9723fe908914c0e1ed2689b3ffaa3b56f1b53b/sccm-cmdlets/ConfigurationManager/vlatest/Get-CMObjectSecurityScope.md
ms.topic: reference
author: shill-ms
ms.author: v-suhill
keywords: powershell, cmdlet
open_to_public_contributors: True
ms.service: configuration-manager
---

# Get-CMObjectSecurityScope

## SYNOPSIS
Gets the security scope associated with a Configuration Manager object.

## SYNTAX

### FilterByName (Default)
```
Get-CMObjectSecurityScope -InputObject <IResultObject> [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### FilterById
```
Get-CMObjectSecurityScope -InputObject <IResultObject> [-Id <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMObjectSecurityScope** cmdlet gets the security scopes that are associated with a Microsoft System Center Configuration Manager object.

## EXAMPLES

### Example 1: Get security scopes for an application object
```
PS C:\>Get-CMApplication -Name "Application1" | Get-CMObjectSecurityScope
```

This command gets the application object named Application1 and uses the pipeline operator to pass the object to **Get-CMObjectSecurityScope**, which gets all security scopes associated with the application object.

### Example 2: Get a security scope
```
PS C:\>Get-CMObjectSecurityScope -InputObject (Get-CMApplication -Name "Application1") -Name "Scope1"
```

This command gets the security scope named Scope1 that is associated with the application object named Application1.

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
Specifies the ID of a security scope that is associated with a Configuration Manager object.

```yaml
Type: String
Parameter Sets: FilterById
Aliases: CategoryId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a Configuration Manager object that is associated with a security scope.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a security scope that is associated with a Configuration Manager object.

```yaml
Type: String
Parameter Sets: FilterByName
Aliases: CategoryName

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

### IResultObject[]#SMS_SecuredCategory

## NOTES

## RELATED LINKS

[Add-CMObjectSecurityScope](xref:ConfigurationManager/vlatest/Add-CMObjectSecurityScope.md)

[Get-CMApplication](xref:ConfigurationManager/vlatest/Get-CMApplication.md)

[Remove-CMObjectSecurityScope](xref:ConfigurationManager/vlatest/Remove-CMObjectSecurityScope.md)

[Set-CMObjectSecurityScope](xref:ConfigurationManager/vlatest/Set-CMObjectSecurityScope.md)

