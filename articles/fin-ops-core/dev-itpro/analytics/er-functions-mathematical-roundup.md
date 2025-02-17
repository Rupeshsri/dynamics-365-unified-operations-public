---
# required metadata

title: ROUNDUP ER function
description: This topic provides information about how the ROUNDUP Electronic reporting (ER) function is used.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: 
ms.technology: 

# optional metadata

ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
# ROBOTS: 
audience: Application User, IT Pro
# ms.devlang: 
ms.reviewer: kfend
# ms.tgt_pltfrm: 
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
# ms.search.industry: 
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0

---

# ROUNDUP ER function

[!include [banner](../includes/banner.md)]

The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.

## Syntax

```vb
ROUNDDOWN (number, decimals)
```

## Arguments

`number`: *Real*

A numeric value that must be rounded up.

`decimals`: *Integer*

A numeric value that represents the number of decimal places.

## Return values

*Real*

The resulting numeric value.

## Usage notes

This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).

## Example 1

`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.

## Example 2

`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.

## Additional resources

[Mathematical functions](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]