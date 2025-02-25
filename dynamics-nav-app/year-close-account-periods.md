---
title: Close Accounting Periods for a Fiscal Year 
description: Describes how to close the accounting periods that make up the fiscal year.

documentationcenter: ''
author: jswymer

ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: year closing, close accounting period, close fiscal year, bank account detailed trial balance
ms.date: 06/02/2017
ms.author: jswymer

---
# How to: Close Accounting Periods
When a fiscal year is over, you must close the periods that comprise it.

## To close accounting periods
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Accounting Periods**, and then choose the related link.
2. In the **Accounting Periods** window, choose the **Close Year** action.

    If more than one fiscal year is open, the earliest one is automatically selected to be closed. A message displays identifying the year that will close and the consequences of closing the year.
3. To close the year, choose the **Yes** button.

The fiscal year is closed, and the **Closed** and **Date Locked** fields for all the periods in the year are selected. The fiscal year cannot be opened again and you cannot remove the check mark from the **Closed** or **Date Locked** fields.

> [!NOTE]  
>   You cannot close a fiscal year before you create a new one. Notice that when a fiscal year has been closed, you cannot change the starting date of the following fiscal year.

Even though a fiscal year has been closed, you can still post general ledger entries to it. When you do this, the entries will be marked as posted to a closed fiscal year and the **Prior-Year Entry** field will be selected.

After a fiscal year is closed, you must close the income statement accounts and transfer the year's results to an account in the balance sheet. You can repeat this every time that you post to the closed fiscal year.

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Closing Books](year-close-books.md)  
[How to: Post the Year-End Closing Entry](year-how-post-year-end-close-entry.md)  
[How to: Open a New Fiscal Year](finance-how-open-new-fiscal-year.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
