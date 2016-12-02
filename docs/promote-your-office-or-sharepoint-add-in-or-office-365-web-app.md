---
title: Promote your Office or SharePoint Add-in or Office 365 web app
ms.prod: MULTIPLEPRODUCTS
ms.assetid: b19e21f8-76f5-44e1-9971-bef79cad4c71
ms.locale: en-US
---


# Promote your Office or SharePoint Add-in or Office 365 web app







After you submit your app or add-in to the Seller Dashboard and it is approved for addition to the Office Store, you might want to brand it as an  Office Store app or add-in on your webpage. You can use the Office Store badges to promote your app or add-in and drive traffic from your site to the store. To do so:

1. Download the [Office Store Badge zip file](http://download.microsoft.com/download/2/4/D/24D59A35-F3C6-410D-AF29-43C9304631FE/OfficeDownload.zip).
2. Choose the badge size that best suits your needs. Badge sizeHow it looksSmallMediumLarge
3. Add the badge to your  app or add-in webpage, directly following the link. This will make it clear to your users that they can download your app or add-in from the  Office Store. 




You can also add your Office 365 web app using Azure AD to the Office 365 app launcher. For information, see [Have your add-in appear in the Office 365 add-in launcher](https://msdn.microsoft.com/en-us/office/office365/howto/connect-your-app-to-o365-app-launcher).

## Guidelines for using the Office Store badge
The following guidelines apply to using the Office Store badge on your webpage:

- Make the Office Store badge visually distinct. Do not overlap it with or incorporate it within any other icon or brand image on your page.
- Do not modify the badge.
- Do not make the badge the primary element on your webpage.
- Do not use the badge on any pages that violate laws or regulations or that contain otherwise objectionable content. This includes pages that contain or display adult content, promote gambling, promote violence, or contain hate speech.
- Make sure that when users choose the badge, the link opens your page in the Office Store, and that your app or add-in is available in the Office Store.




If you need a localized version of the badge,  [contact us](http://officespdev.uservoice.com/).



## Link to the Office Store from your site
When you link from the Office Store badge on your site to your app or add-in in the Office Store, include the following query parameters at the end of the URL:

- mktcmpid=Your marketing campaign ID, which can include up to 16 characters (any letter, number, _, and -). For example, blogpost_12.
- mktvid=Your Store Provider ID, which is included in the URL of your Store Provider page. For example, PN102957641.




The following example shows a URL that includes the two query parameters:



https://store.office.com/app.aspx?assetid=WA102957661&mktcmpid=refexample&mktvid=PN102957641



Adding these parameters to your Office Store URL will enable us to provide more information about where your customers are coming from. In the future, when you include your Store Provider ID, we can provide you counts of the number of customers who go to the Office Store from your webpage.



## Track your campaign performance and customize your add-in for targeted audiences

>**Note:**
>This currently applies to Word, Excel, and PowerPoint add-ins that are free in the Office Store.


When you link from your promotional campaigns to your free Word, Excel, or PowerPoint add-in page in the Office Store, include the following query parameters at the end of the URL: 

- mktcmpid=Your marketing campaign ID, which can include up to 16 characters (any letter, number, _ , and -). For example, blogpost_12. 
- mktvid=Your Store Provider ID, which is included in the URL of your Store Provider page. For example, PN102957641. 




The following example shows a URL that includes the two query parameters: 



https://store.office.com/app.aspx?assetid=WA102957661&mktcmpid=refexample&mktvid=PN102957641 



Adding these parameters to your campaign URL will enable us to provide more information about your campaign's user funnel.



The *mktcmpid* parameter is passed all the way to the launch document. This allows you to customize the first user experience of your free Word, Excel, or PowerPoint add-in to, for example, display a specific splash screen or welcome message to your targeted audience. 



When the document loads for the targeted user, the *mktcmpid* parameter is available in the [Settings object](https://dev.office.com/reference/add-ins/shared/settings) of the add-in as a CampaignId, in Office clients where the Settings object is supported. Use the following code to read the CampaignId from the Settings object. 

```sourcecode
if (Office.context.document.settings) { 
               return Office.context.document.settings.get("CampaignId"); 
                } 

```




The value that is sent to the document is the value of the *mktcmpid* parameter.



## Additional resources
<a name="bk_addresources"></a>

- [Submit Office and SharePoint Add-ins and Office 365 web apps to the Office Store](Submit-Office-and-SharePoint-Add-ins-and-Office-365-web-apps-to-the-Office-Store.md)
- [Office Add-ins](https://dev.office.com/docs/add-ins/overview/office-add-ins)
- [SharePoint Add-ins](cd1eda9e-8e54-4223-93a9-a6ea0d18df70.md)





