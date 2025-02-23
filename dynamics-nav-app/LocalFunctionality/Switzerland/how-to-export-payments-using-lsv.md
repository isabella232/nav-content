---
    title: How to Export Payments Using LSV
    description: You can export or write Lastschrift Verfahren (LSV+) files that contain payments information after closing the LSV collection. You can send the generated files to the bank on a disk, or use an electronic file transfer such as your online banking software or an Internet portal.

    documentationcenter: ''
    author: SorenGP

    ms.prod: "dynamics-nav-2018"
    ms.topic: article
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 07/01/2017
    ms.author: edupont

---
# How to: Export Payments Using LSV
You can export or write Lastschrift Verfahren (LSV+) files that contain payments information after closing the LSV collection. You can send the generated files to the bank on a disk, or use an electronic file transfer such as your online banking software or an Internet portal.  

## To export payments using LSV  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **LSV Journal List**, and then choose the related link.  
2.  In the **LSV Journal List** window, select the required LSV journal.  
3.  Choose the **Write LSV File** action.  
4.  In the **Write LSV File** window, on the **Options** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**No.**|Specify the LSV journal number that you want to export.|  
    |**Test**|Specify if you are sending test deliveries to your bank. The bank does not process test files.|  

5.  All related lines are transferred to the LSV journal. The LSV file is generated in the predetermined folder.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Swiss Electronic Payments Using LSV+](swiss-electronic-payments-using-lsv-.md)   
 [How to: Process an LSV Collection](how-to-process-an-lsv-collection.md)   
 [How to: Close an LSV Collection](how-to-close-an-lsv-collection.md)   
 [How to: Post LSV+ Payments](how-to-post-lsv-payments.md)
