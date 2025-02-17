---
# required metadata

title: Upgrade single-voucher journals and currency revaluations
description: This topic describes how to upgrade single-voucher journals and currency revaluations.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.technology: 

# optional metadata

# ms.search.form: 
# ROBOTS: 
audience: Application User
# ms.devlang: 
ms.reviewer: sericks
# ms.tgt_pltfrm: 
ms.custom: 265364
ms.assetid: c61391e4-c4bf-4f09-bd18-8107a1bf055e
ms.search.region: Global
# ms.search.industry: 
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611

---

# Upgrade single-voucher journals and currency revaluations

[!include [banner](../includes/banner.md)]

Some organizations enter journals that contain a single voucher that has more than one customer or vendor, and they also run the Accounts receivable or Accounts payable foreign currency revaluation process. This topic describes the steps that these organizations should follow when they upgrade to Microsoft Dynamics 365 for Operations version 1611.

Follow these steps when you upgrade to Microsoft Dynamics 365 for Operations version 1611.

1.  Before you upgrade to Finance and Operations, run the foreign currency revaluation processes for Accounts receivable and Accounts payable. Set the **Method** field to **Invoice date**. A revaluation transaction is created that reverses the last foreign currency revaluation. Therefore, the open transactions are valued at their original accounting currency.
2.  Upgrade to version 1611.
3.  Run the Accounts receivable and Accounts payable foreign currency revaluation processes again. This time, set the **Method** field to **Standard**. A new revaluation transaction is created that is based on the current exchange rates. This transaction records the unrealized gain/loss and the correct summary ledger account.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]