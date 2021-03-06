﻿---
title: Get-CMTaskSequenceDeployment
titleSuffix: Configuration Manager
description: Gets a task sequence deployment in Configuration Manager.
ms.date: 12/03/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Get-CMTaskSequenceDeployment

## SYNOPSIS

Gets a task sequence deployment in Configuration Manager.

## SYNTAX

### SearchByName (Default)

```powershell
Get-CMTaskSequenceDeployment [-Name <String>] [-Summary] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById

```powershell
Get-CMTaskSequenceDeployment [-TaskSequenceId <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId

```powershell
Get-CMTaskSequenceDeployment [-DeploymentId <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue

```powershell
Get-CMTaskSequenceDeployment [-InputObject <IResultObject>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMTaskSequenceDeployment** cmdlet gets a task sequence deployment.
A task sequence deployment assigns a task sequence to a collection of computers.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1

```powershell
PS XYZ:\> Get-CMTaskSequenceDeployment -Name "Task Sequence 1333" 
```

This command gets a task sequence deployment by name.

## PARAMETERS

### -Collection

Specifies a collection object.

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

Specifies a collection ID.

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

Specifies a name of a collection designated to receive a task sequence deployment.
A collection is a group of client computers.

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

### -DeploymentId

Specifies a deployment ID.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AdvertisementID, TaskSequenceDeploymentID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

Specifies a task sequence deployment object.
To obtain a task sequence object, use the [Get-CMTaskSequenceDeployment](Get-CMTaskSequenceDeployment.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: TaskSequence

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies the name of a task sequence.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: TaskSequenceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Summary

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

### -TaskSequenceId

Specifies the ID of a task sequence

```yaml
Type: String
Parameter Sets: SearchById
Aliases: SmsObjectId, TaskSequencePackageID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_DeploymentSummary

- IResultObject#SMS_DeploymentSummary
- IResultObject[]#SMS_Advertisement
- IResultObject#SMS_Advertisement

## RELATED LINKS

[New-CMTaskSequenceDeployment](./New-CMTaskSequenceDeployment.md)
[Set-CMTaskSequenceDeployment](./Set-CMTaskSequenceDeployment.md)
[Start-CMTaskSequenceDeployment](./Start-CMTaskSequenceDeployment.md)
[Remove-CMTaskSequenceDeployment](./Remove-CMTaskSequenceDeployment.md)
