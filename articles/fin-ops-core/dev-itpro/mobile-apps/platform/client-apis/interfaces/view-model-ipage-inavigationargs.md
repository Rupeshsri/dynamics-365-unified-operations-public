---
# required metadata
title: NavigationArgs type
description: NavigationArgs type
author: robinarh
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.technology: 
# optional metadata
# ms.search.form:
audience: Developer
# ms.devlang: 
ms.reviewer: rhaertle
# ms.tgt_pltfrm: 
# ms.custom:
ms.search.region: Global
# ms.search.industry: 
ms.author: rhaertle
ms.search.validFrom:
ms.dyn365.ops.version:
---

# NavigationArgs type

[!include [banner](../../../../includes/banner.md)]

### Hierarchy

[PageTarget](view-model-ipage-ipagetarget.md) <br>&nbsp;&nbsp;&nbsp;└─ NavigationArgs <br>

## Index

### Properties

* [label](view-model-ipage-inavigationargs.md#label)
* [options](view-model-ipage-inavigationargs.md#options)
* [params](view-model-ipage-inavigationargs.md#params)
* [replace](view-model-ipage-inavigationargs.md#replace)
* [to](view-model-ipage-inavigationargs.md#to)
* [url](view-model-ipage-inavigationargs.md#url)

## Properties

### label

label: string (optional) 




### options

options: any (optional) 




### params

params: [PageOptions](view-model-ipage-ipageoptions.md) (optional) 



> Inherited from [PageTarget](view-model-ipage-ipagetarget.md).[params](view-model-ipage-ipagetarget.md#params)


### replace

replace: boolean (optional) 

If set to true, removes current view firing navigation from navigation history stack.


### to

to: string (optional) 



> Inherited from [PageTarget](view-model-ipage-ipagetarget.md).[to](view-model-ipage-ipagetarget.md#to)


### url

url: string (optional) 

If provided, this link is directly opened.




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]