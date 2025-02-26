---
title: Revalue Fixed Assets
description: Learn how to adjust the value of fixed assets, recording new amounts as a write-down or appreciation, and post additional acquisition costs.

documentationcenter: ''
author: SorenGP

ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 06/02/2017
ms.author: edupont

---
# How to: Revalue Fixed Assets
Revaluation of fixed assets can consist of appreciations, write-downs, or general value adjustments.

When the value of a fixed asset has increased, you post a journal line with a higher amount, an appreciation, to the depreciation book. The new amount is recorded as an appreciation according to the fixed asset posting setup.

When the value of a fixed asset has decreased, you post a journal line with a lower amount, a write-down, to the depreciation book. The new amount is recorded as a write-down according to the fixed asset posting setup.

Indexation is used to adjust multiple fixed asset values, for example per general price changes. The **Index Fixed Assets** batch job can be used to change various amounts, such as write-down and appreciation amounts.

## To post an appreciation from the fixed asset G/L journal
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.  
2. Create an initial journal line and fill in the fields as necessary.
3. In the **FA Posting Type** field, select **Revaluation**.
4. Choose the **Insert FA Bal. Account** action. A second journal line is created for the balancing account that is set up for appreciation posting.

    > [!NOTE]  
   >   Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Appreciation Account** field contains the general ledger debit account and the **Appreciation Bal. Account** field contains the general ledger account to which you want to post balancing entries for appreciation. For more information, see the "To set up fixed asset posting groups" section in [How to: Set Up General Fixed Asset Information](fa-how-setup-general.md).  
5. Choose the **Post** action.

## To post a write-down from the fixed asset G/L journal
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.  
2. Create an initial journal line, and fill in the fields as necessary.
3. In the **FA Posting Type** field, select **Write-Down**.
4. Choose the **Insert FA Bal. Account** action. A second journal line is created for the balancing account that is set up for write-down posting.

    > [!NOTE]  
   >   Step 4 only works if you have set up the following: In the **FA Posting Group Card** window for the posting group of the fixed asset, the **Write-Down Account** field contains the general ledger credit account and the **Write-Down Expense Account** field contains the general ledger debit account to which you want to post balancing entries for write-downs. For more information, see the "To set up fixed asset posting groups" section in [How to: Set Up General Fixed Asset Information](fa-how-setup-general.md).
5. Choose the **Post** action.

## To perform general revaluation of fixed assets
Indexation is used to adjust multiple fixed asset values, for example per general price changes. The **Index Fixed Assets** batch job can be used to change various amounts, such as write-down and appreciation amounts. The **Allow Indexation** check box in the **Depreciation Book** window must be selected.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Index Fixed Assets**, and then choose the related link.  
2. Fill in the fields as necessary.
3. Choose the **OK** button.

    Revaluation lines are created per your settings in step 2. The lines are created in either the fixed asset journal or the fixed asset G/L journal, depending on your template and batch setup in the **FA Journal Setup** window. For more information, see [How to: Set Up General Fixed Asset Information](fa-how-setup-general.md).
4. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **FA G/L Journals**, and then choose the related link.  
5. Select the journal with the fixed assets that you want to revalue, and then choose the **Ledger Entries** action.  
6. Check the created entries, and then choose the **Post** action to post the journal.

    > [!TIP]  
   >   If the index figures are for simulation purposes only, you can create a special depreciation book to store them in. Then these entries will not affect any of the other depreciation books.

   ## To post additional acquisition costs
   You post additional acquisition cost for a fixed asset in the same way as you post the original acquisition cost: from a purchase invoice or from a fixed asset journal. For more information, see [How to: Acquire Fixed Assets](fa-how-acquire.md).  

If depreciation has already been calculated for the fixed asset, select the **Depr. Acquisition Cost** check box to have the additional acquisition cost less the salvage value depreciated in proportion to the amount by which the previously acquired fixed asset has already been depreciated. This ensures that the depreciation period is not changed.  

The depreciation percentage is calculated as:  

*P = (total depreciation x 100) / depreciable basis*

*Depreciation amount = (P/100) x (extra acquisition cost - salvage value)*  

Remember to select the **Depr. until FA Posting Date** check box on the invoice, the fixed asset G/L journal, or the fixed asset journal lines to ensure that depreciation is calculated from the last fixed asset posting date to the posting date of the additional acquisition cost.

### Example - Posting Additional Acquisition Costs
A machine is purchased on August 1, 2000. The acquisition cost is 4,800. The depreciation method is straight-line over four years.

On August 31, 2000, the **Calculate Depreciation** batch job is run. Depreciation is calculated as:

*book value x number of depreciation days / total number of depreciation days = 4800 x 30 / 1440 = 100*  

On September 15, 2000, an invoice is posted for painting the machine. The invoice amount is 480.

If you selected the **Depr. until FA Posting Date** check box on the invoice before posting, the following calculation is made:  

15 days of depreciation (from 09/01/00 to 09/15/00) is calculated as:

*book value x number of depreciation days / remaining number of depreciation days = (4800 - 100) x 15 / 1410 = 50*

If you selected the **Depr. Acquisition Cost** check box on the invoice before posting, the following calculation is made:  

*The additional acquisition cost is depreciated by ((150 x 100) / 4800) / 100 x 480 = 15*

The depreciable basis is now *5280 = (4800 + 480)*, and the accumulated depreciation is *165 = (100 + 50 + 15)*, corresponding to 45 days of depreciation of the total acquisition cost. This means that the asset will be totally depreciated within the estimated lifetime of four years.  

When the **Calculate Depreciation** batch job is run on 09/30/00, the following calculation is made:  

*Remaining depreciable life is 3 years, 10 months and 15 days = 1395 days*  

*Book value is (5280 - 165) = 5115*  

*Depreciation amount for September 2000: 5115 x 15 / 1395 = 55.00*  

*Total of depreciation = 165 + 55 = 220*  

If you did not select the **Depr. until FA Posting Date** check box, the asset would lose 15 days of depreciation because the **Calculate Depreciation** batch job run on 09/30/00 would calculate depreciation from 09/15/00 to 09/30/00. This means that when the **Calculate Depreciation** batch job is run on 09/30/00, the calculation is as follows:  

*Remaining life time is 3 years, 10 months and 15 days = 1395 days*  

*Book value is (4800 + 480 - 100 - 15) = 5165*

*Depreciation amount for September 2000: 5165 x 15 / 1395 = 55.54*  

*Total of depreciation = 100 + 15 + 55.54 = 170.54*

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Fixed Assets](fa-manage.md)  
[Setting Up Fixed Assets](fa-setup.md)  
[Finance](finance.md)  
[Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
