---
title: Obter o endereço de email de um item de contato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344685"
---
# <a name="get-the-email-address-of-a-contact-item"></a><span data-ttu-id="c77f3-103">Obter o endereço de email de um item de contato</span><span class="sxs-lookup"><span data-stu-id="c77f3-103">Get the email address of a Contact item</span></span>

<span data-ttu-id="c77f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c77f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c77f3-105">Este tópico mostra como obter o valor de uma propriedade nomeada que representa o endereço de email de um item de contato do Microsoft Outlook 2010 ou do Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="c77f3-105">This topic shows how to obtain the value of a named property that represents the email address of an Microsoft Outlook 2010 or Microsoft Outlook 2013 Contact item.</span></span>
  
<span data-ttu-id="c77f3-106">Você pode associar até três endereços de email com um item de contato no Outlook 2010 e no Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="c77f3-106">You can associate up to three email addresses with a Contact item in Outlook 2010 and Outlook 2013.</span></span> <span data-ttu-id="c77f3-107">Cada endereço de email corresponde a uma propriedade do objeto **ContactItem** do Outlook 2010 ou do Outlook 2013 nos modelos de objeto do Outlook 2010 e Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="c77f3-107">Each email address corresponds to a property of the Outlook 2010 or Outlook 2013 **ContactItem** object in the Outlook 2010 and Outlook 2013 object models.</span></span> <span data-ttu-id="c77f3-108">Interno para o Outlook 2010 e o Outlook 2013, o endereço de email também corresponde a uma propriedade nomeada MAPI.</span><span class="sxs-lookup"><span data-stu-id="c77f3-108">Internal to Outlook 2010 and Outlook 2013, the email address also corresponds to a MAPI named property.</span></span> <span data-ttu-id="c77f3-109">Por exemplo, o primeiro endereço de email de um contato corresponde à propriedade **Email1Address** do **ContactItem** nos modelos de objeto do outlook 2010 e Outlook 2013, e o Outlook 2010 e o Outlook 2013 interno nomeado [ Propriedade canônica PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).</span><span class="sxs-lookup"><span data-stu-id="c77f3-109">For example, the first email address of a contact corresponds to the **Email1Address** property of the **ContactItem** in the Outlook 2010 and Outlook 2013 object models, and the Outlook 2010 and Outlook 2013 internal named [PidLidEmail1EmailAddress Canonical Property](pidlidemail1emailaddress-canonical-property.md).</span></span>
  
<span data-ttu-id="c77f3-110">Para obter o valor de um endereço de email de um item de contato, você pode usar o objeto **PropertyAccessor** do modelo de objeto do Outlook 2010 ou do Outlook 2013, ou primeiro usar o [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade da propriedade nomeada e, em seguida, Especifique essa marca de propriedade em [IMAPIProp::](imapiprop-getprops.md) GetProps para obter o valor.</span><span class="sxs-lookup"><span data-stu-id="c77f3-110">To obtain the value of an email address of a contact item, you can use the **PropertyAccessor** object of the Outlook 2010 or Outlook 2013 object model, or first use [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) to obtain the property tag of the named property, and then specify this property tag in [IMAPIProp::GetProps](imapiprop-getprops.md) to get the value.</span></span> <span data-ttu-id="c77f3-111">Ao chamar **IMAPIProp:: GetIDsFromNames**, especifique os valores apropriados para a estrutura [MAPINAMEID](mapinameid.md) indicada pelo parâmetro de entrada _lppPropNames_.</span><span class="sxs-lookup"><span data-stu-id="c77f3-111">When calling **IMAPIProp::GetIDsFromNames**, specify the appropriate values for the [MAPINAMEID](mapinameid.md) structure pointed at by the input parameter  _lppPropNames_.</span></span> <span data-ttu-id="c77f3-112">O exemplo de código a seguir mostra como obter o primeiro endereço de email de um contato `lpContact`especificado, usando **GetIDsFromNames** e GetProps. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c77f3-112">The following code sample shows how to obtain the first email address of a specified contact,  `lpContact`, using **GetIDsFromNames** and **GetProps**.</span></span> 
  
```cpp
HRESULT HrGetEmail1(LPMESSAGE lpContact) 
{ 
    HRESULT hRes = S_OK; 
    LPSPropTagArray lpNamedPropTags = NULL; 
    MAPINAMEID NamedID = {0}; 
    LPMAPINAMEID lpNamedID = &NamedID; 
    NamedID.lpguid = (LPGUID)&PSETID_Address; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidEmailEmailAddress; 
 
    hRes = lpContact->GetIDsFromNames( 
           1,  
           &lpNamedID,  
           NULL,  
           &lpNamedPropTags); 
 
    if (SUCCEEDED(hRes) && lpNamedPropTags) 
    { 
        SPropTagArray sPropTagArray; 
 
        sPropTagArray.cValues = 1; 
        sPropTagArray.aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTags->aulPropTag[0],PT_STRING8); 
        LPSPropValue lpProps = NULL; 
        ULONG cProps = 0; 
 
        hRes = lpContact->GetProps( 
               &sPropTagArray, 
               NULL, 
               &cProps, 
               &lpProps); 
        if (SUCCEEDED(hRes) &&  
            1 == cProps &&  
            lpProps &&  
            PT_STRING8 == PROP_TYPE(lpProps[0].ulPropTag) && 
            lpProps[0].Value.lpszA) 
        { 
            printf("Email address 1 = \"%s\"\n",lpProps[0].Value.lpszA); 
        } 
        MAPIFreeBuffer(lpProps); 
        MAPIFreeBuffer(lpNamedPropTags); 
     } 
     return hRes; 
}
```


