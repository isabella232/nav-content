---
title: Manage Fixed Assets
description: Learn about the fixed assets functionality in Dynamics NAV and get an overview of how to work with fixed assets.

documentationcenter: ''
author: SorenGP

ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: machinery, buildings
ms.date: 06/02/2017
ms.author: edupont

---
# Fixed Assets
The Fixed Assets functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)] provides an overview of your fixed assets and ensures correct periodic depreciation. It also enables you to keep track of your maintenance costs, manage insurance policies, post fixed asset transactions, and generate various reports and statistics.

For each fixed asset, you must set up a card containing information about the asset. You can set up buildings or production equipment as a main asset with a component list, and you can group them in various ways, such as by class, department, or location. Then you can begin to acquire, maintain, and sell the fixed assets. You can also set up budgeted assets. This makes it possible to include any anticipated acquisitions and sales in reports.

To keep track of fixed asset depreciations as well as other financial transactions related to fixed assets, you set up one or more depreciation books for each fixed asset in your company. Depreciation is done by running a report to calculate periodic depreciation and fill in a journal with the resulting entries, ready to be posted. [!INCLUDE[d365fin](includes/d365fin_md.md)] supports several depreciation methods. For more information, see [Depreciation Methods](fa-depreciation-methods.md). You can set up multiple depreciation books per fixed asset for different purposes, such as one for tax reporting and another for internal reporting.

For each asset, you can record maintenance costs and the next service date. Keeping track of maintenance expenses can be important for budgeting purposes and for making decisions about whether to replace a fixed asset.

Each fixed asset can be attached to one or more insurance policies. You can therefore easily verify that insurance policy amounts are in accordance with the value of the assets that are linked to the policy. This also makes it easy to monitor annual insurance premiums.

> [!NOTE]  
>   You can record fixed asset transactions in the **Fixed Asset G/L Journal** window or in the **Fixed Asset Journal** window, depending on whether the transactions are for financial reporting or for internal management. Help for Fixed Assets only describes how to use the **Fixed Asset G/L Journal** window. For more information, see [How to: Set Up Fixed Asset Depreciation](fa-how-setup-depreciation.md).

Before you can begin to manage fixed assets, you must set up default values, fixed asset accounting, posting groups, allocation keys, journals, and posting types. For more information, see [Setting Up Fixed Assets](fa-setup.md).

The following table describes a sequence of tasks, with links to the topics that describe them.

| To | See |
| --- | --- |
| Create fixed assets, assign depreciation methods, post acquisitions, salvage values, and print fixed asset lists. |[How to: Acquire Fixed Assets](fa-how-acquire.md) |
| Record service visits, post maintenance costs, and monitor maintenance costs. |[How to: Maintain Fixed Assets](fa-how-maintain.md) |
| Update insurance information, post acquisition costs to insurance policies, modify insurance coverage, view insurance statistics, and list insurance policies. |[How to: Insure Fixed Assets](fa-how-insure.md) |
| Reclassify fixed assets, transfer fixed assets to different locations, split up or combine assets. |[How to: Transfer, Split, or Combine Fixed Assets](fa-how-trans-split-combine.md) |
| Adjust values of fixed assets, post appreciation, and post write-down transactions. |[How to: Revalue Fixed Assets](fa-how-revalue.md) |
| Calculate depreciation, post depreciation, and  analyze depreciation in fixed assets reports. |[How to: Depreciate or Amortize Fixed Assets](fa-how-depreciate-amortize.md) |
| Post disposal transactions, view disposal ledger entries, and post partial disposals. |[How to: Dispose of or Retire Fixed Assets](fa-how-dispose-retire.md) |
| Manage fixed asset budgets, budget acquisition costs, budget disposals of fixed assets, and budget depreciation. |[How to: Manage Budgets for Fixed Assets](fa-how-manage-budgets.md) |

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Setting Up Fixed Assets](fa-setup.md)  
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-customizing-overview.md)  
[Finance](finance.md)  
[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
