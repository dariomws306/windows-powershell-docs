---
author: brianlic-msft
description: 
external help file: Microsoft.UpdateServices.Commands.dll-Help.xml
keywords: powershell, cmdlet
manager: alanth
ms.date: 2016-12-20
ms.prod: powershell
ms.technology: powershell
ms.topic: reference
online version: 
schema: 2.0.0
title: Set-WsusClassification
ms.assetid: 6207A305-EFCA-40EE-B997-2A939DD9BE7A
---

# Set-WsusClassification

## SYNOPSIS
Sets whether the classifications of updates that WSUS synchronizes are enabled.

## SYNTAX

```
Set-WsusClassification -Classification <WsusClassification> [-Disable] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-WsusClassification** cmdlet enables or disables the category of updates, for example, security or critical, to be synchronized.

To use this cmdlet without filtering results, the [Get-WsusClassification](./Get-WsusClassification.md) cmdlet must be run, then the results are passed it into this cmdlet.

To use this cmdlet with filtered results, the **Get-WsusClassification** cmdlet must be run, then results are filtered using the [Where-Object](http://go.microsoft.com/fwlink/?LinkID=113423) cmdlet and passed into this cmdlet.

## EXAMPLES

### Example 1: Disable driver updates
```
PS C:\> Get-WsusClassification | Where-Object -FilterScript {$_.Classification.Title -Eq "Drivers"} | Set-WsusClassification -Disable
```

This command specifies that you do not want driver updates.

## PARAMETERS

### -Classification
Specifies the classification of updates that are to be synchronized.
If the **Disable** parameter is used, then this parameter specifies the classification of updates that are not to be synchronized.
This parameter value is passed from the **Get-WsusClassification** cmdlet.

```yaml
Type: WsusClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -Disable
Specifies that updates are not to be synchronized for the specified classification.

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

### None

## OUTPUTS

### None

## NOTES

## RELATED LINKS

[Where-Object](http://go.microsoft.com/fwlink/p/?LinkID=289623)

[Get-WsusClassification](./Get-WsusClassification.md)