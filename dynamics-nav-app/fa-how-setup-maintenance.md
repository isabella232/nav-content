---
title: Set Up FA Maintenance
description: To manage fixed asset repairs and service, you specify general maintenance information, codes for the type of work, and a posting account for costs.

documentationcenter: ''
author: SorenGP

ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: repair, service
ms.date: 06/02/2017
ms.author: edupont

---
# How to: Set Up Fixed Asset Maintenance
To manage fixed asset maintenance, you must first set up some general maintenance information, a posting account for maintenance costs, and maintenance codes for types of work, such as Routine Service or Repair.

## To set up general maintenance information
If you set up the fields for maintenance, you can post maintenance expenses from the fixed asset journal.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Fixed Assets**, and then choose the related link.
2. Select the fixed asset that you to define insurance coverage for, and then choose the **Edit** action.
3. On the **Maintenance** FastTab, fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## To set up maintenance codes
When you post maintenance costs from a general journal, you fill in the **Maintenance Code** field to record what kind of maintenance has been performed, such as routine service or repair.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Maintenance**, and then choose the related link.
2. In the **Maintenance** window, set up codes for different types of maintenance work.

## To set up maintenance expense accounts
To post maintenance costs, you must first enter an account number in the **FA Posting Groups** window.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA Posting Groups**, and then choose the related link.
2. Fill in the **Maintenance Expense Account** field for each posting group.

> [!NOTE]  
>   To define that maintenance costs are allocated to departments or projects, set up an allocation keys. For more information, see [How to: Set Up General Fixed Assets Features](fa-how-setup-general.md).

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Setting Up Fixed Assets](fa-setup.md)  
[Fixed Assets](fa-manage.md)  
[Finance](finance.md)  
[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
