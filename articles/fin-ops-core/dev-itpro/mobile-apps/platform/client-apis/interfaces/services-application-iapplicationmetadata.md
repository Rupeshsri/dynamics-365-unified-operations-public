---
# required metadata

title: ApplicationMetadata type
description: Represents the declarative metadata of an application
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

# ApplicationMetadata type

[!include [banner](../../../../includes/banner.md)]

Represents the declarative metadata of an application

### Hierarchy

ApplicationMetadata <br>

## Index

### Properties

* [ColorName](services-application-iapplicationmetadata.md#colorname)
* [Configs](services-application-iapplicationmetadata.md#configs)
* [Description](services-application-iapplicationmetadata.md#description)
* [IconName](services-application-iapplicationmetadata.md#iconname)
* [Id](services-application-iapplicationmetadata.md#id)
* [Title](services-application-iapplicationmetadata.md#title)

## Properties

### ColorName

ColorName: string (optional) 

The theme color of the application


### Configs

Configs: [name: string]: any (optional) 

An application can have a set of named config supplied by the author or the resource provider


### Description

Description: string (optional) 

The description of the application


### IconName

IconName: string (optional) 

The representative icon of the application


### Id

Id: string

The unique identifier of the application


### Title

Title: string

The title of the application




[!INCLUDE[footer-include](../../../../../../includes/footer-banner.md)]