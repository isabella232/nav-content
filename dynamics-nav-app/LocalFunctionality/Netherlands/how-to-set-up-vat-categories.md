---
    title: How to Set Up VAT Categories
    description: To use the electronic VAT declaration, you must set up a VAT category code for all XML elements in the electronic VAT declaration.

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
# How to: Set Up VAT Categories
To use the electronic VAT declaration, you must set up a VAT category code for all XML elements in the electronic VAT declaration.  

You must set up all of the possible category and subcategory combinations that represent an XML element in the electronic VAT declaration. Then, you can map the VAT statement data directly to an XML element.  

## To set up a VAT category  

1.  Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Elec. Tax. Decl. VAT Categories**, and then choose the related link.  
2.  In the **Elec. Tax. Decl. VAT Categories** window, choose the **New** action.  
3.  Fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Code**|The unique code for each category and subcategory combination. You can enter a maximum of 10 alphanumeric characters.|  
    |**Category**|Specify the main category option for the VAT statement.|  
    |**By Us (Domestic)**|The subcategory for the VAT Statement.<br /><br /> Select a subcategory here if the **Category** field displays **By Us (Domestic)**.|  
    |**To Us (Domestic)**|The subcategory for the VAT Statement.<br /><br /> Select a subcategory here if the **Category** field displays **To Us (Domestic)**.|  
    |**By Us (Foreign)**|The subcategory for the VAT Statement.<br /><br /> Select a subcategory here if the **Category** field displays **By Us (Foreign)**.|  
    |**To Us (Foreign)**|The subcategory for the VAT Statement.<br /><br /> Select a subcategory here if the **Category** field displays **To Us (Foreign)**.|  
    |**Calculation**|The subcategory for the VAT Statement.<br /><br /> Select a subcategory here if the **Category** field displays **Calculation**.|  
    |**Optional**|Select to indicate that the XML element that is represented by the category code is not required in the electronic VAT declaration.|  

4.  Choose the **OK** button.  

You can now map the VAT statement data directly to an XML element.  

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[Electronic VAT and ICP Declarations](electronic-vat-and-icp-declarations.md)   
 [How to: Create Electronic VAT and ICP Declarations](how-to-create-electronic-vat-and-icp-declarations.md)
