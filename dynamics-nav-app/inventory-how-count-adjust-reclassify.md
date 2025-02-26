---
title: Count, Adjust, and Reclassify Inventory
description: Describes how to perform physical counting, make negative or positive adjustments, and how to change information, such as location or lot number, on item ledger entries or warehouse entries.

documentationcenter: ''
author: SorenGP

ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: adjustment, negative, positive, increase, decrease
ms.date: 08/16/2017
ms.author: edupont

---
# How to: Count, Adjust, and Reclassify Inventory
At least once every fiscal year you must take a physical inventory, that is, count all the items on inventory, to see if the quantity registered in the database is the same as the actual physical quantity in the warehouses. When the actual physical quantity is known, it must be posted to the general ledger as a part of period-end valuation of inventory.

Although you count all items in inventory at least once a year, you may have decided to count some items more often, perhaps because they are more valuable, or because they are very fast movers and a large part of your business. For this purpose, you can assign special counting periods to those items. For more information, see the "To perform cycle counting" section.

If you need to adjust recorded inventory quantities, in connection with counting or for other purposes, you can use an item journal to change the inventory ledger entries directly without posting business transactions. Alternatively, you can adjust for a single item on the item card.

If you need to change attributes on item ledger entries as well as the quantities, you can use the item reclassification journal. Typical attributes to reclassify include serial/lot numbers, expiration dates, and dimensions.

> [!NOTE]
> In advanced warehouse configurations, items are registered in bins as warehouse entries, not as item ledger entries. Therefore, you perform counting, adjusting, and reclassifying in special warehouse journals that support bins. Then, you use special functions to synchronize the new or changed warehouse entries with their related item ledger entries to reflect the changes in inventory quantities and values. This is described in specific procedures below where relevant.

## To perform a physical inventory
You must take a physical inventory, that is, count the actual items on hand, to check if the quantity registered is the same as the physical quantity in stock at the end of a fiscal year, if not more often. If there are differences, you must post them to the item accounts before you do the inventory valuation.

Apart from the physical counting task, the complete process involves the following three tasks:

- Calculate the expected inventory.
- Print the report to be used when counting.
- Enter and post the actual counted inventory.

You can perform the physical inventory in either of the following ways depending on your warehouse setup. For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).  

-   If your location is not using directed put-away and pick (basic warehouse configuration), you use the **Phys. Inventory Journal** window in the **Inventory** menu, and the procedure is much the same as when you conduct a physical inventory without cycle counting.  
-   If your location is using directed put-away and pick (advanced warehouse configuration), you first use the **Whse. Phys. Invt. Journal** window, and then you use the **Item Journal** window to run the **Calculate Whse. Adjustment** function.

### To calculate the expected inventory in basic warehouse configurations
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Phys. Inventory Journals**, and then choose the related link.
2. Choose the **Calculate Inventory** action.
3. In the **Calculate Inventory** window, specify the conditions to use to create the journal lines, such as whether to include items that have zero recorded inventory.
4. Set filters if you only want to calculate inventory for certain items, bins, locations, or dimensions.
5. Choose the **OK** button.

> [!NOTE]  
>   The item entries are processed according to the information that you specified, and lines are created in the physical inventory journal. Notice that the **Qty. (Phys. Inventory)** field is automatically filled in with the same quantity as the **Qty. (Calculated)** field. With this feature, it is not necessary for you to enter the counted inventory on hand for items that are the same as the calculated quantity. However, if the quantity counted differs from what is entered in the **Qty. (Calculated)** field, you must overwrite it with the quantity actually counted.

### To calculate the expected inventory in advanced warehouse configurations
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Journal**, and choose the related link.  
2.  Choose the **Calculate Whse. Adjustment** action.  
3.  Fill in the batch job request window with the numbers of the items you want to count and with your location.
4. Choose the **OK** button, and post the adjustments if any.

    If you do not do this before you perform the warehouse physical inventory, the results you post to the physical inventory journal and item ledger in the second part of the process will be the physical inventory results combined with other warehouse adjustments for the items that were counted.  
5.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Whse. Phys. Invt. Journal**, and choose the related link.  
6. Choose the **Calculate Inventory** action. The **Whse. Calculate Inventory** batch job request window opens.  
7.  Set the filters to limit the items that will be counted in the journal, and then choose the **OK** button.

    The program creates a line for each bin that fulfills the filter requirements. You can at this point still delete some of the lines, but if you want to post the results as a physical inventory, you must count the item in all the bins that contain it.  

     If you only have time to count the item in some bins and not others, you can discover discrepancies, register them, and later post them in the item journal using the **Calculate Whse. Adjustment** function.  
8.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Whse. Phys. Inventory List**, and choose the related link.  
9.  Open the  report request page and print the lists on which you want employees to record the quantity of items that they count in each bin.  
10. When the counting is done, enter the counted quantities in the **Qty. (Phys. Inventory)** field in the warehouse physical inventory journal.  

    > [!NOTE]  
    >  In the warehouse physical inventory journal, **Qty. (Calculated)** field is filled in automatically on the basis of warehouse bin records and copies these quantities are copied to the **Qty. (Physical)** field on each line. If the quantity counted by the warehouse employee differs from what the program has entered in the Qty. (Physical) field, you must enter the quantity actually counted.  

11. When you have entered all the counted quantities, choose the **Register** action.  

    When you register the journal, the program creates two warehouse entries in the warehouse register for every line that was counted and registered:  

    -   If the calculated and the physical quantities differ, a negative or positive quantity is registered for the bin, and a balancing quantity is posted to the adjustment bin of the location.  
    -   If the quantity calculated is equal to the physical quantity, the program registers an entry of 0 for both the bin and the adjustment bin. The entries are the record that on the registering date, a warehouse physical inventory was performed, and there was no discrepancy in inventory for the item.  

When you register the warehouse physical inventory, you are not posting to the item ledger, the physical inventory ledger, or the value ledger, but the records are there for immediate reconciliation whenever necessary. If you like to keep precise records of what is happening in the warehouse, however, and you counted all of the bins where the items were registered, you should immediately post the warehouse results as an inventory physical inventory. For more information, see the "To enter and post the actual counted inventory in advanced warehouse configurations" section.

### To print the report to be used when counting
1. In the **Phys. Inventory Journal** window containing the calculated expected inventory, Choose the **Print** action.
2. In the **Phys. Inventory List** window, specify if the report should show the calculated quantity and if the report should list inventory items by serial/lot numbers.
3. Set filters if you only want to print the report for certain items, bins, locations, or dimensions.
4. Choose the **Print** button.

Employees can now proceed to count inventory and record any discrepancies on the printed report.

### To enter and post the actual counted inventory in basic warehouse configurations
1. On each line in the **Phys. Inventory Journal** window where the actual inventory on hand, as determined by the physical count, differs from the calculated quantity, enter the actual inventory on hand in the **Qty. (Phys. Inventory)** field.

    The related fields are updated accordingly.

    > [!NOTE]  
   >   If the physical count reveals differences that are caused by items posted with incorrect location codes, do not enter the differences in the physical inventory journal. Instead, use the reclassification journal or a transfer order to redirect the items to the correct locations. For more information, see Item Reclass. Journal or How to: Create Transfer Orders.

2. To adjust the calculated quantities to the actual counted quantities, choose the **Post** action.

    Both item ledger entries and physical inventory ledger entries are created. Open the item card to view the resulting physical inventory ledger entries.

3. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.
4. To verify the inventory counting, open the item card in question, and then, choose the **Phys. Inventory ledger Entries** action.

### To enter and post the actual counted inventory in advanced warehouse configurations

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Journal**, and choose the related link.  
2.  Choose the **Calculate Whse. Adjustment** action.  
3.  Select the same items that you counted in the cycle counting physical inventory you just performed, and any other items that require adjustment, and then choose the **OK** button.  

     The **Inventory Journal** window opens and lines are created for these items. Note that the net quantities that you just counted and registered bin by bin are now ready to be consolidated and synchronized as item ledger entries.  

4.  Post the journal without changing any quantities.  

The quantities in the item ledger (item entries) and the quantities in the warehouse (warehouse entries) are now once again the same for these items, and the program has updated the last counting date of the item or stockkeeping unit.  

## To perform cycle counting
Although you count all items in inventory at least once a year, you may have decided to count some items more often, perhaps because they are more valuable, or because they are very fast movers and a large part of your business. For this purpose, you can assign special counting periods to those items.

You can perform the cycle counting in either of the following ways depending on your warehouse setup. For more information, see [Setting Up Warehouse Management](warehouse-setup-warehouse.md).  

-   If your location is not using directed put-away and pick (basic warehouse configuration), you use the **Phys. Inventory Journal** window in the **Inventory** menu, and the procedure is much the same as when you conduct a physical inventory without cycle counting.  
-   If your location is using directed put-away and pick (advanced warehouse configuration), you first use the **Whse. Phys. Invt. Journal** window, and then you use the **Item Journal** window to run the **Calculate Whse. Adjustment** function.  

### To set up counting periods
A physical inventory is typically taken at some recurring interval, for example monthly, quarterly, or annually. You can set up whatever inventory counting periods necessary.

You set up the inventory counting periods that you want to use and then assign one to each item. When you perform a physical inventory and use the **Calculate Counting Period** in the physical inventory journal, lines for the items are created automatically.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Phys. Invt. Counting Periods**, and then choose the related link.  
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

### To assign a counting period to an item  
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.  
2. Select the item to which you want to assign a counting period.  
3. In the **Phys Invt Counting Period Code** field, select the appropriate counting period.  
4. Choose the **Yes** button to change the code and calculate the first counting period for the item. The next time you choose to calculate a counting period in the physical inventory journal, the item appears as a line in the **Phys. Invt. Item Selection** window. You can then begin to count the item on a periodic basis.

### To initiate a count based on counting periods in basic warehouse configurations
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Phys. Inventory Journal**, and then choose the related link.
2. Choose the **Calculate Counting Period** action.

    The **Phys. Invt. Item Selection** window opens showing the items that have counting periods assigned and need to be counted according to their counting periods.
3. Perform the physical inventory. For more information, see the "To perform a physical inventory" section.

### To initiate a count based on counting periods in advanced warehouse configurations
1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Whse. Phys. Invt. Journal**, and choose the related link.  
2. Choose the **Calculate Counting Period** action.

    The **Phys. Invt. Item Selection** window opens showing the items that have counting periods assigned and need to be counted according to their counting periods.
3. Perform the physical inventory. For more information, see the "To perform a physical inventory" section.  

    > [!NOTE]  
    >  You must count the item in all the bins that contain the particular item. If you delete some of the bin lines that the program has retrieved for counting in the **Whse. Phys. Inventory** window, then you will not be counting all the items in the warehouse. If you later post such incomplete results in the Phys. Inventory Journal, the amounts posted will be incorrect.  

## To adjust the inventory of one item
After you have made a physical count of an item in your inventory area, you can use the **Adjust Inventory** function to record the actual inventory quantity.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items**, and then choose the related link.
2. Select the item for which you want to adjust inventory, and then choose the **Adjust Inventory** action.
3. In the **New Inventory** field, enter the inventory quantity that you want to record for the item.
4. Choose the **OK** button.

The item’s inventory is now adjusted. The new quantity is shown in the **Current Inventory** field in the **Adjust Inventory** window and in the **Inventory** field in the **Item Card** window.

You can also use the **Adjust Inventory** function as a simple way to place purchased items on inventory if you do not use purchase invoices or orders to record your purchases. For more information, [How to: Record Purchases](purchasing-how-record-purchases.md).

> [!NOTE]  
>   After you have adjusted inventory, you must update it with the current, calculated value. For more information, see [How to: Revalue Inventory](inventory-how-revalue-inventory.md).

### To adjust the inventory quantity of multiple items in basic warehouse configurations
In the **Item Journal** window, you can post item transaction directly to adjust inventory in connection with purchases, sales, and positive or negative adjustments without using documents.

If you often use the item journal to post the same or similar journal lines, for example, in connection with material consumption, you can use the **Standard Item Journal** window to make this recurring work easier. For more information, see the "Standard Journals" section in [Working with General Journals](ui-work-general-journals.md).

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Journals**, and then choose the related link.
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Choose the **Post** action to make the inventory adjustments.

> [!NOTE]  
>   After you have adjusted inventory, you must update it with the current, calculated value. For more information, see [How to: Revalue Inventory](inventory-how-revalue-inventory.md).

### To adjust bin quantities in advanced warehouse configurations  
If your location uses directed put-away and pick, use the **Whse. Item Journal** to post, outside the context of the physical inventory, all positive and negative adjustments in item quantity that you know are real gains, such as items previously posted as missing that show up unexpectedly, or real losses, such as breakage.  

Unlike posting adjustments in the inventory item journal, using the warehouse item journal gives you an additional level of adjustment that makes your quantity records even more precise at all times. The warehouse thus always has a complete record of how many items are on hand and where they are stored, but each adjustment registration is not posted immediately to the item ledger. In the registering process, credits or debits are made to the real bin with the quantity adjustment and a counterbalancing entry is made in an adjustment bin, a virtual bin with no real items. This bin is defined in the **Invt. Adjustment Bin Code** on the location card.

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Whse. Item Journal**, and then choose the related link.  
2.  Fill in the header information.  
3.  Fill in the **Item No.** field on the line.  
4.  Enter the bin in which you are putting the extra items or where you have found items to be missing.  
5.  Fill in the quantity that you observe as a discrepancy in the **Quantity** field. If you have found extra items, enter a positive quantity. If items are missing, enter a negative quantity.  
6.  Choose the **Register** action.

## To synchronize the adjusted warehouse entries with the related item ledger entries
At appropriate intervals as defined by company policy, you must post the warehouse adjustment bin records in the item ledger. Some companies find it appropriate to post adjustments to the item ledger every day, while others may find it adequate to reconcile less frequently.

1.  Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Journal**, and then choose the related link.  
2.  Fill in the fields on each journal line.  
3.  Choose the **Calculate Whse. Adjustment** action, and fill in the filters as appropriate in the batch job request window. The adjustments are calculated only for the entries in the adjustment bin that meet filter requirements.  
4.  On the **Options** FastTab, fill in the **Document No.** field with a number that you enter manually. Because no number series has been set up for this batch job, use the number scheme set up by the warehouse, or enter the date followed by your initials.  
5.  Choose the **OK** button. The positive and negative adjustments are totaled for each item and lines are created in the item journal for any items where the sum is a positive or negative quantity.  
6.  Post the journal lines to enter the quantity differences in the item ledger. The inventory in the warehouse bins now corresponds precisely to the inventory in the item ledger.  

## To reclassify an item's lot number
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Reclass. Journals**, and then choose the related link.
2. In the **Item Reclass. Journal** window, fill in the fields as necessary.
3. To In the **Lot No.** field, enter the items current lot number.
4. In the **New Lot No.** field, enter the item's new lot number.
5. Choose the **Post** action.

Special steps apply when you want to reclassify serial or lot numbers. For more information, see [How to: Work with Serial and Lot Numbers](inventory-how-work-item-tracking.md).

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Inventory](inventory-manage-inventory.md)
[Warehouse Management](warehouse-manage-warehouse.md)    
[Sales](sales-manage-sales.md)  
[Purchasing](purchasing-manage-purchasing.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
