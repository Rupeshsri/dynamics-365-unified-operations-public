---
# required metadata

title: Cancel an executing batch job
description: This topic provides information about how to cancel an executing batch job.
author: Peakerbl
manager: AnnBe
ms.date: 02/23/2021
ms.topic: article
ms.prod: 
ms.technology: 

# optional metadata

# ms.search.form: 
# ROBOTS: 
audience: IT Pro
# ms.devlang: 
ms.reviewer: sericks
# ms.tgt_pltfrm: 
ms.custom: 62333
ms.assetid: 6135bcf7-bf8f-42ae-b2c6-458f6538e6a4
ms.search.region: Global
# ms.search.industry: 
ms.author: peakerbl
ms.search.validFrom: 2019-05-08
ms.dyn365.ops.version: Platform update 27

---

# Cancel an executing batch job
[!include [banner](../includes/banner.md)]

> [!NOTE] 
> This feature is available as of Platform update 27.

Sometimes canceling a batch job can take a long time if already executing tasks will take a long time to finish. This option provides a system administrator or batch job manager with the ability to cancel already executing tasks for jobs that are in the process of being canceled. This provides a much faster mechanism to cancel a long running job that is impacting system usage elsewhere.

>[!NOTE]
> It is important to note that this feature should be used with caution. When you cancel a running process, it is an inherently unsafe action that can lead to data corruption, resulting in either orphaned or incomplete data. This action should only be used to mitigate other issues caused by the running tasks.

Complete the following steps to immediately cancel the running task.

1. Go to **System administration** \> **Inquiries** \> **Batch jobs**.
2. Select a batch job that has a **Status** of **Canceling**.
3. On the **Batch tasks** tab, select **Abort** on the task, and then select **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
