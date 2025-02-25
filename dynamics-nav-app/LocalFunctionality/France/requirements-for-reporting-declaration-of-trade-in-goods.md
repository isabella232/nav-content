---
    title: Requirements for Reporting Declaration of Trade in Goods
    description: This topic shows a list of required fields that are needed for reporting Declaration of Trade in Goods (DEB) based on the DTI+ format. For more information, see Export DEB DTI.

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
# Requirements for Reporting Declaration of Trade in Goods
This topic shows a list of required fields that are needed for reporting Declaration of Trade in Goods (DEB) based on the DTI+ format. For more information, see Export DEB DTI.  

The following fields are required for reporting DEB:  

- **CISD** from the **Company Information** table.  
- **Registration No.** from the **Company Information** table.  
- **VAT Registration No.** from the **Company Information** table.  
- **Name** from the **Company Information** table.  
- **Date** for the statistics period from the **Intrastat Jnl. Line** table.  
- **Transaction Specification** from the **Intrastat Jnl. Line** table.  
- **Quantity** from the **Intrastat Jnl. Line** table must be greater than 0.  
- **Statistical Value** from the **Intrastat Jnl. Line** table must be greater than 0.  

> [!NOTE]  
>  The **Export DEB DTI** report exports shipments and receipts in one batch. If you want to report only shipments or receipts, then you must set a filter to remove the lines that are not needed in the **Intrastat Journal** table.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[France Local Functionality](france-local-functionality.md)
