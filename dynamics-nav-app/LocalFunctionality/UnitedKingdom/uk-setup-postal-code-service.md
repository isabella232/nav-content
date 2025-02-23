---
title: 'How to: Set Up the GetAddress.io UK Postcodes Extension'
description: Describes the general functionality you use to interact with data in Dynamics NAV, such as entering values, sorting data, and changing views.
author: bholtorf
ms.prod: "dynamics-nav-2018"
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: getaddress.io, postcodes, extension
ms.date: 07/17/2017
ms.author: bholtorf

---
# How to: Set Up the GetAddress.io UK Postcodes Extension
This extension makes it easy to enter addresses in the UK for entities like customers, contacts, employees, vendors, bank accounts, and so on.

The GetAddress.io UK Postcodes extension uses the getAddress API to find addresses in postcodes in the UK. To use the extension, you need to get a plan and an API Key for the getAddress API. That's easy, and we help you do that when you set up the GetAddress.io UK Postcodes extension. Plans are based on use, or what's sometimes referred to as calls. A call, in this case, is when [!INCLUDE[navnow](../../includes/navnow_md.md)] displays a list of addresses in a postcode. Depending on how often you add addresses, choose the plan that is best for you. If you just choose **Get API Key** in the page, you'll use the **Free** plan, which lets you add 20 addresses per day, and is valid for 30 days.

## To set up the GetAddress.io UK Postcodes extension
1. Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Connections**, and then choose the related link.  
2. In the **Service Connections** window, choose **UK Postcode Service**.
3. In the **Postcode provider configuration** page, choose **Disabled**.
4. In the **Postal code service selection** window, choose **GetAddress.io**.
5. In the **GetAddress.io Config** window, choose **Get API Key** to open the **Plans** page on the website for the getAddress API.  

    > [!NOTE]  
   >   You might need to allow pop-ups in your browser.

6. Purchase a plan, or just choose **Get API Key**, and then provide your email address.
7. Open the email from getAddress.io, and copy the API key. The key is under the **Your API Key** heading.
8. In the **GetAddress.io Config** window, paste the API key in the **API Key** field, and then Choose the **OK** button.
9. In the **Service Connections** page, verify that the **Address Provider** field shows **GetAddress.io**. If it does, the service is enabled.

## See Also
[Dynamics 365 Business Central](https://docs.microsoft.com/dynamics365/business-central/)  
[United Kingdom Local Functionality](united-kingdom-local-functionality.md)  
[GetAddress.io UK Postcodes](../../ui-extensions-getaddressio.md)
[Customizing [!INCLUDE[navnow](../../includes/navnow_md.md)] Using Extensions](../../ui-extensions.md)  
[Working with [!INCLUDE[navnow](../../includes/navnow_md.md)]](../../ui-work-product.md)
