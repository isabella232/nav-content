---
    title: How to Activate SEPA Payments
    description: To submit vendor payments electronically in Single Euro Payments Area (SEPA) ISO 20022 payment format, you must set up prerequisites for enabling SEPA payments.

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
# How to: Activate SEPA Payments
To submit vendor payments electronically in Single Euro Payments Area (SEPA) ISO 20022 payment format, you must set up prerequisites for enabling SEPA payments.  

In the following procedures describe how to enable SEPA payment and set up vendor bank accounts.  

## To enable countries/regions for SEPA  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Countries/Regions**, and then choose the related link.  
2.  Choose the **Edit List** action.  
3.  Select the **SEPA Allowed** check box for each country or region that you want to enable for SEPA.  
4.  Choose the **OK** button.  

## To enable bank accounts for SEPA  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Bank Accounts**, and then choose the related link.  
2.  Select the bank account that you want to enable for SEPA, and then choose the **Edit** action.  
3.  On the **General** FastTab, in the **Country/Region Code** field, select the appropriate code.  

    > [!NOTE]  
    >  The specified country/region code must be enabled for SEPA as described in the previous procedure.  

4.  Enter a value in the **Min. Balance** field.  
5.  On the **Transfer** FastTab, in the **SWIFT Code** field, enter a code.  
6.  Choose the **OK** button.  

## To set up vendor bank accounts for SEPA  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Vendors**, and then choose the related link.  
2.  Select the relevant vendor, and then choose the **Bank Accounts** action.  
3.  Select the vendor bank account to set up for SEPA, and then choose the **Edit**.  
4.  On the **Transfer** FastTab, in the **IBAN** and **SWIFT Code** fields, enter the international bank identifier code of the bank where the vendor has the account.  
5.  Choose the **OK** button.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[SEPA Payments](sepa-payments.md)   
 [How to: File SEPA Payments](how-to-file-sepa-payments.md)   
 [How to: File Non-Euro SEPA Payments](how-to-file-non-euro-sepa-payments.md)   
 [How to: Set Up Export Protocols](how-to-set-up-export-protocols.md)
