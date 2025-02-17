---
# required metadata

title: Self-service deployment FAQ
description: This topic provides answers to some frequently asked questions about self-service deployment.
author: rashmansur
manager: AnnBe
ms.date: 03/10/2021
ms.topic: article
ms.prod: 
ms.technology: 

# optional metadata

# ms.search.form:  [Operations AOT form name to tie this topic to]
audience: IT Pro
# ms.devlang: 
ms.reviewer: sericks
# ms.custom: [used by loc for topics migrated from the wiki]
ms.search.region: Global 
# ms.search.industry: 
ms.author: rashmim
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: 8.1.1

---

# Self-service deployment FAQ

[!include[banner](../includes/banner.md)]
[!include [banner](../includes/limited-availability.md)]

This topic provides answers to some frequently asked questions about [self-service deployment](infrastructure-stack.md). Refer to the [known issues](known-issues-new-deployment-experience.md) list if your scenario is not listed here.  

## Why do I see only application version 8.1.1 and Platform update 21 and above when I try to deploy my sandbox environment using self-service deployment? 

Currently, self-service deployment supports only application version 8.1.1 with Platform update 21 and above.  

## My development environment is on application version 8.1. Am I still able to move my customization to the sandbox environment? 

Yes. Application version 8.1.1 is fully backward compatible with application 8.1. 

## What is the minimum supported application and platform version when trying to use the self-service deployment? 

Application version 8.1 with Platform update 20 is the minimum supported version. 

## What do I do if deployment fails? 

1. Delete the deployment.  
2. If you want to reuse the same environment name, wait 5 minutes and try again. Otherwise, retry deploying with a new name. 
3. If deployment fails again, log a Support ticket.  

> [!Note]
> Microsoft will add automatic retry logic in an upcoming release and make logs available. 

## What if my deployment fails with an “environment already exists” error? 

You may be trying to reuse the environment name of a deployment that you just deleted. Wait 5–10 minutes before retrying the deployment. 

## I don't have Remote Desktop access to my sandbox environment. How do I perform critical actions that require Remote Desktop access today?

Although you will no longer have Microsoft Remote Desktop access, you can continue to operate your Tier 2+ sandbox environments, because Microsoft is providing self-service capabilities and tools that you can use to perform the common critical actions that are described here.

### Access the Azure SQL database
You can access the Microsoft Azure SQL database by following these steps.

1. From LCS, add a safe list of the IP address of the machine that you will use to connect to the Azure SQL database using SQL Management Studio.
2. Use LCS to request access to see the database credentials. You must provide a reason for requesting access. 

As soon as you submit the request, it's automatically approved. Within a minute or two, you will be able to see the database access credentials on the LCS environment details page. You can use the credentials to connect to the SQL database.

> [!NOTE]
> The credentials are valid for eight hours, and then they will expire. After the credentials expire, you will have to request access again. 

### Access log files
You can view and download all log files from the **Activity** tab on the LCS environment monitoring page.

### Use perfmon tools
Although you can no longer use Remote Desktop and then use perfmon.exe to diagnose performance issues, you can monitor critical health metrics for CPU and memory consumption through LCS. In addition, you can run predefined queries on demand, and you can run predefined actions to mitigate performance issues on your Tier 2+ environments. 

### Access self-service logs
All logs that are related to self-service operations that are performed on the environment through LCS are available for download from LCS. These self-service operations include deployment, servicing, and database movement. You can download the log folders from the LCS environment history page.

### Turn Maintenance mode on/off
Starting in the January 2019 release, you will be able to turn Maintenance mode in your environment on and off through a self-service action in LCS.

### Restart services
Starting in the January 2019 release, you will able to restart services through a self-service action in LCS.

### Configure the Regression suite automation tool
Microsoft is working on tooling that will let you update certificate thumbprints in the wif.config file without having to use Remote Desktop. This tooling is scheduled for release in February 2019. If you must use the Regression suite automation tool before then, log a support request.

## I must perform one of the critical actions that are listed earlier in this topic, but the self-service feature isn't yet available. How do I get help?

Log a support ticket, and Microsoft will help you perform the action on your environment.

## I don't have Remote Desktop access to my sandbox environment, and the critical action that I must perform isn't listed in this topic. How do I get help?

If your critical action isn't listed earlier in this topic, add a comment to this topic or log a documentation bug, and Microsoft will address your requirement.

## What regions are supported on self-service in North America?
We currently only support the following regions in North America.

- East US
- West US
- Central US

For more information about region availability, see [International availability of Dynamics 365](https://www.microsoft.com/trustcenter/privacy/dynamics365-operations-location).

### My environments are currently in the regions that are no longer supported. How will this change affect me?
Projects that have been onboarded on or after August 1, 2020 are no longer supported in the following regions:

-	East US2
-	West US2
-	West Central US
-	North Central US
-	South Central US

> [!NOTE]
> This will not affect any environments that have their data stored in the deprecated regions before August 2020. There is a transition plan to move customers in the deprecated regions into other regions. For a list of the latest supported regions, see [International availability of Dynamics 365](https://www.microsoft.com/trustcenter/privacy/dynamics365-operations-location).

- With all self-service migrations, we are changing the outbound IP addresses in regions where your environments are hosted. New outbound IP addresses are available, so you must add them before your upcoming self-service migrations. For more information about IP addresses, see [For my Microsoft-managed environments, I have external components that have dependencies on an explicit outbound IP safe list. How can I ensure my service is not impacted after the move to self-service deployment?](deploymentFAQ.md#for-my-microsoft-managed-environments-i-have-external-components-that-have-dependencies-on-an-explicit-outbound-ip-safe-list-how-can-i-ensure-my-service-is-not-impacted-after-the-move-to-self-service-deployment).
- If you have any integrations or other dependencies that are latency-driven and have questions regarding how the change in regions will impact that, please contact [Microsoft Support](../lifecycle-services/lcs-support.md).
- If you are planning to leverage dual-write, virtual entities, or any Finance and Operations add-ins that have dependences on Dataverse, keep in mind that **Dataverse is not supported in Central US**. We recommend that you choose East US or West US for continued functionality for features on self-service. Contact [Microsoft Support](../lifecycle-services/lcs-support.md) if you want to move to East US or West US instead of Central US, as part of your move to self-service.
-	Please review all the Azure resources in your current region and assess if they need to be co-located to the new region in preparation for the upcoming changes as part of migrations.
- If you have questions about data movement related to cross-region migrations, see [The source and target are on different infrastructure (Microsoft-managed vs. self-Service)](../database/database-pitr-prod-sandbox.md#the-source-and-target-are-on-different-infrastructure-microsoft-managed-vs-self-service).

## For my Microsoft-managed environments, I have external components that have dependencies on an explicit outbound IP safe list. How can I ensure my service is not impacted after the move to self-service deployment?
With self-service migrations, we are changing the outbound IP addresses in regions where your environments are hosted. New outbound IP addresses are available so you can add them in preparation for the upcoming self-service migrations or post migrations.

* If none of your external components have dependencies on an explicit inclusion list of IPs or special handling of outbound IP addresses for routing or firewall, no action is required.
* If any of your external components have special handling for the outbound IP addresses to communicate to the AOS, add the new outbound IP addresses where the existing ones appear. Don’t replace the existing IP addresses. You can find the new outbound IP addresses in the following list. For example, an outbound IP address may be explicitly included in a firewall outside your AOS, or an external service may have an allowed list that contains the outbound IP address for your AOS.

The inbound IP address to the AOS is dynamic. This can, and will, change over time as infrastructure changes occur.

> [!NOTE]
> The outbound IP address from the AOS will remain static for the duration of an individual AOS session, which is currently listed to end in June 2021. 

| Region | IP prefix
|---------------------|-------------|
| West US | 52.250.195.128/26
| East US | 52.255.218.64/26
| Central US | 13.86.98.128/26
| West EUR | 51.105.159.192/26
| West EUR-2 | 20.61.88.128/26
| North EUR | 52.155.160.192/26
| UK West | 51.137.139.0/26
| UK South | 51.11.26.192/26
| Australia East | 20.40.190.0/26
| Australia SouthEast | 20.40.165.192/26
| Canada Central | 20.151.60.0/26
| Canada East | 52.155.27.128/26
| Brazil South | 191.234.130.0/26
| East Asia | 52.229.231.64/26
| South East Asia | 20.44.247.0/26
| Japan East | 20.48.77.192/26
| Japan West | 20.39.179.192/26
| India South | 20.40.5.0/26
| India Cental | 20.193.248.192/26

## Is there a potential impact on the environment's certificates?

Yes, if you are migrating from the previous non self-service deployment, your environment’s certificate may be renewed due to infrastructure differences. Determine if there is any dependence on the certificates in your solution/integration and perform the needed actions after the migration.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
