---
    title: Supply Planning 
    description: Prepare a detailed executable plan and the final-assembly production schedule for sales and production demand.
    
    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 09/14/2017
    ms.author: edupont

---
# Planning
The production operations required to transform inputs into finished goods must be planned daily or weekly depending on the volume and nature of the products. [!INCLUDE[d365fin](includes/d365fin_md.md)] offers features to supply for anticipated and actual demand from sale, assembly, and production as well as features for distribution planning using stockkeeping units and location transfers.

> [!NOTE]
> This topic mainly describes planning for companies involved in manufacturing or assembly management where the resulting supply orders can be either production, assembly, transfer, or purchase orders. The main interface for this planning work is the **Planning Worksheet** window.
> 
> [!INCLUDE[d365fin](includes/d365fin_md.md)] also supports supply planning for wholesale companies where the resulting supply orders can only be transfer and purchase orders. The main interface for this planning work is the **Requisition Worksheet** window, which is described indirectly in this topic as most planning functionality applies to both worksheets.

Before you can plan and execute production orders, you must configure production capacities, such as creating shop calendars, routings, production BOMs, and machine centers. For more information, see [Setting Up Manufacturing](production-configure-production-processes.md).

Planning can be seen as the preparation required supply orders in the assembly or manufacturing departments to fulfill demand. For more information, see [Assembly Management](assembly-assemble-items.md) and [Manufacturing](production-manage-manufacturing.md).

The following table describes a sequence of tasks, with links to the topics that describe them.   

|**To**|**See**|  
|------------|-------------|  
|Get a brief introduction to how the planning system can be used to detect and prioritize demand and suggest a balanced supply plan.|[About Planning Functionality](production-about-planning-functionality.md)|
|Understand how all aspects of the planning system works and how to adjust the algorithms to meet planning requirements in different environments.|[Design Details: Supply Planning](design-details-supply-planning.md)|
|Learn how the planning logic differentiates between demand at locations according to the SKU setup and demand without location codes.|[Planning With or Without Locations](production-planning-with-without-locations.md)|
|Forecast production demand presented by expected sales and production orders.|[How to: Create a Production Forecast](production-how-to-create-a-forecast.md)|  
|Create one-to-one production orders automatically from a sales order to cover the exact demand of that sales order line.|[How to: Create Production Orders from Sales Orders](production-how-to-create-production-orders-from-sales-orders.md)|
|Create a project production order directly from a multiline sales order representing a production project.|[How to: Plan Project Orders](production-how-to-plan-project-orders.md)|
|Use the **Order Planning** window to manually plan for sales or production demand one production BOM level at a time.|[How to: Plan for New Demand Order by Order](production-how-to-plan-for-new-demand.md)|
|Use the **Planning Worksheet** window to run both the MPS and MRP options to automatically create either a high-level or detailed supply plan at all item levels.|[How to: Run Full Planning, MPS or MRP](production-how-to-run-mps-and-mrp.md)|
|Run the requisition worksheet to automatically create a detailed supply plan to cover demand for items that are replenished by purchase or transfer only.|**Requisition Worksheet** page|  
|Initiate or update a production order as rough-scheduled operations in the master production schedule.|[How to: Replan or Refresh Production Orders Directly](production-how-to-replan-refresh-production-orders.md)|
|Recalculate work or machine center calendars due to planning changes.|"To calculate a work center calendar" section in [How to: Set Up Shop Calendars](production-how-to-create-work-center-calendars.md)|
|Track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.|[How to: Track Relations Between Demand and Supply](production-how-track-demand-supply.md)|
|View an item's projected available inventory by different views and see which gross requirements, planned order receipts, and other events influence it over time.|[How to: View the Availability of Items](inventory-how-availability-overview.md)|  
|Perform selected planning activities, such as changing or adding planning worksheet lines, in a graphical view of the supply plan.|[How to: Modify Planning Suggestions in a Graphical View](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Setting Up Manufacturing](production-configure-production-processes.md)  
[Manufacturing](production-manage-manufacturing.md)    
[Inventory](inventory-manage-inventory.md)  
[Purchasing](purchasing-manage-purchasing.md)  
[Design Details: Supply Planning](design-details-supply-planning.md)   
[Setup Best Practices: Supply Planning](setup-best-practices-supply-planning.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
