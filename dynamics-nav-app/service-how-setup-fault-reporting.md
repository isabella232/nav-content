---
    title: Set Up Fault Reporting in Service Management 
    description: Learn how to set up fault reporting processes.
    
    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 08/22/2017
    ms.author: edupont

---

# How to: Set Up Fault Reporting
Fault reporting lets you establish standards for recording fault information for service items. For example, you can specify what the problem is, the symptoms you see, the reason for the problem, and how to resolve it.  

Fault codes describe the typical service item faults or the actions taken on service items. Depending on the level of fault reporting in your company, you might need to set up fault area codes and symptom codes before you set up fault codes. Fault areas descrive areas of service item faults. Fault reason codes describe the reason for service item faults and, if needed, whether to exclude warranty and contract discounts. For example, you might want to exclude warranty and contract discounts if the customer was somehow responsible for the fault in the service item. You assign fault reason codes to service orders. For more information, see [How to: Work on Service Tasks](service-how-to-work-on-service-tasks.md).  

## To specify the overall level of fault reporting to use
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link. 
2. In the **Fault Reporting Level** field, choose one of the options described in the following table.  
  
    |**Fault Level**|**Description**|  
    |------------|-------------|  
    |None | No reporting codes are used.|  
    |Fault | Codes are listed in the **Fault Codes** table. These codes identify service item faults or actions to take on service items. You can cluster related codes into **Fault Area Code** groupings.|  
    |Fault + Symptom | You provide a combination of codes in the **Fault Codes** and **Symptom Codes** tables. Typical symptom codes include indicators that a customer might use to describe a problem, such as a noise or a quality.|  
    |Fault + Symptom + Area | You use fault, symptom, and fault area codes as an implementation of the International Repair Coding System (IRIS).|  
  
To complete the setup of fault reporting, you can also specify what repairs or resolutions are associated with a fault or defect. You set that up on the **Fault/Resolution Code Relationships** page, where you set up combinations of codes for the service item group of the service item from which you accessed the witndow and the number of occurrences for each one.

## To create fault and resolution code relationships
<!--this needs to go in a working with topic-->
To be able to see the most common methods of repair for particular item faults when you are servicing the items, you need to build up information on fault/resolution codes relationships. Use the **Insert Fault/Resol. Codes Relationships** batch job to find all the combination of fault and resolution codes in posted service orders and record them on the **Fault/Resol. Codes Relationships** page. 
  
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Insert Fault/Resol. Codes Relationships**, and then choose the related link.  
2. Enter dates to define the period you want to include in the batch job.  
3. To group the relationships by service item group, choose the **Relation Based on Service Item Group** check box.  
4. To retain the records that you have already inserted manually in the **Fault/Resol. Codes Relationships** page, choose the **Retain Manually Inserted Rec.** check box.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Setting Up Service Management](service-setup-service.md)  
[Service Management](service-service.md)  
