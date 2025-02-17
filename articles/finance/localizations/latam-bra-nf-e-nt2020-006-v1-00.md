---
# required metadata

title: NT2020.006 – Intermediary sales digital platform for NF-e
description: This topic explains how to tag intermediary digital sales for NF-e.
author: gionoder
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 

# optional metadata

# ms.search.form: 
audience: Application User
# ms.devlang: 
ms.reviewer: kfend
# ms.tgt_pltfrm: 
# ms.custom: 
# ms.assetid: 
ms.search.region: Brazil
# ms.search.industry: 
ms.author: sndray
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: 8.0

---

# NT2020.006 – Intermediary sales digital platform for NF-e

[!include [banner](../includes/banner.md)]

A sale can occur even when the customer isn't physically present. Instead, a digital platform or marketplace can serve as an intermediary for the transaction. In these scenarios, the XML of the electronic fiscal document model 55 (NF-e) that is issued from the sale must contain a new tag to indicate that an intermediary participated in the operation.

This feature supports scenarios when a digital platform or marketplace is owned or licensed by the fiscal document issuer.

## Enable the technical note in Dynamics 365 Finance and Dynamics 365 Supply Chain Management

1. Sign in to your instance of Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.
2. Go to **Organization administration** \> **Organizations** \> **Fiscal establishments** \> **Fiscal establishments**.
3. Select the fiscal establishment, and then select **Edit**.
4. On the **NF-e and NFC-e federal** FastTab, in the **NF-e technical notes** field group, select **Enable NF-e technical note**.
5. In the **NF-e technical notes** field, select **2020.006 v1.10 technical note** for version 1.10 of the technical note.

## Enable the technical note in Dynamics AX 2012 R3

- Apply KB 4611321 to enable version 1.10 of the technical note in Dynamics AX 2012 R3.
- Apply KB 4598546 to enable version 1.00 of the technical note in Dynamics AX 2012 R3.

## Sales that are intermediated by the taxpayer's own sales digital platform

When a digital platform that the taxpayer owns serves as the intermediary for a sale, if the presence type is set to one of the following values on the header of the sales order that is created for the sale, the **&lt;indintermed&gt;** tag is added to the XML of the NF-e. The value is set to **0** (zero).

- In person
- Internet
- Telesales
- Others

## Out of scope for the feature

- This feature doesn't support NF-e that are issued from free text invoices that are generated from sales where the customer isn't physically present and a sales digital platform serves as an intermediary.
- This feature doesn't support NF-e that are issued from returns, transfer orders, or complementary and tax credit scenarios.
