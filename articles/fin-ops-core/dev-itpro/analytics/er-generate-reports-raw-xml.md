---
# required metadata

title: Generate reports by adding content as raw XML
description: You can design Electronic reporting (ER) formats that generate outgoing documents in XML format.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.technology: 

# optional metadata

# ms.search.form: EROperationDesigner
# ROBOTS: 
audience: Application User, Developer, IT Pro
# ms.devlang: 
ms.reviewer: kfend
# ms.tgt_pltfrm: 
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
# ms.search.industry: 
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0

---

# Generate reports by adding content as raw XML

[!include[banner](../includes/banner.md)]

You can use the new **RAW XML** format element to design Electronic reporting (ER) formats that generate outgoing documents in XML format. In some cases, you might prefer to add raw XML data to these reports for one or more of the following reasons:

- It's more convenient to use raw XML for the original design and ongoing maintenance of a report, because the XML structure can be automatically generated by executing a runtime expression. Therefore, multiple bindings don't have to be determined for multiple format elements at design time. It is possible when the data sources that you're using contain information that can be used to make XML elements while the report is generated.
- No other method can be used to fill the report with XML content that was previously received and stored in the system. For example, the XML response that is generated might have to contain the content of an XML request that was sent earlier.
- No other method can be used to insert characters into the generated document based on their numeric codes. For some languages and characters, codes of this type don't exist. Examples include the Greek letter rho (ρ) and HTML entity codes such as \&eacute; for an *e* that has an acute accent (é).

> [!NOTE]
> Be aware that the framework doesn't control whether the XML content that is placed to the generated document by using the **RAW XML** format element is correct.

To learn more about this feature, play the **ER Use raw XML data to generate XML reports (Part 1: Design data model)** and **ER Use raw XML data to generate XML reports (Part 2: Design and run report)** task guides, which are part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process, and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684). These task guides walk you through the process of configuring an ER format to insert raw XML data into generated files.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]