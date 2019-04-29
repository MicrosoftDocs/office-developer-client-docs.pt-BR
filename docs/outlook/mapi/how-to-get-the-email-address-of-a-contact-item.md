---
title: Obter o endereço de email de um item de contato
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 032f7242-5500-1e21-06d3-b2d947eb1043
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: fab09d0c594bac1374973f523abe6ff0b9c09dd0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429590"
---
# <a name="get-the-email-address-of-a-contact-item"></a>Obter o endereço de email de um item de contato

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Este tópico mostra como obter o valor de uma propriedade nomeada que representa o endereço de email de um item de contato do Microsoft Outlook 2010 ou do Microsoft Outlook 2013.
  
Você pode associar até três endereços de email com um item de contato no Outlook 2010 e no Outlook 2013. Cada endereço de email corresponde a uma propriedade do objeto **ContactItem** do Outlook 2010 ou do Outlook 2013 nos modelos de objeto do Outlook 2010 e Outlook 2013. Interno para o Outlook 2010 e o Outlook 2013, o endereço de email também corresponde a uma propriedade nomeada MAPI. Por exemplo, o primeiro endereço de email de um contato corresponde à propriedade **Email1Address** do **ContactItem** nos modelos de objeto do outlook 2010 e Outlook 2013, e o Outlook 2010 e o Outlook 2013 interno nomeado [ Propriedade canônica PidLidEmail1EmailAddress](pidlidemail1emailaddress-canonical-property.md).
  
Para obter o valor de um endereço de email de um item de contato, você pode usar o objeto **PropertyAccessor** do modelo de objeto do Outlook 2010 ou do Outlook 2013, ou primeiro usar o [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obter a marca de propriedade da propriedade nomeada e, em seguida, Especifique essa marca de propriedade em [IMAPIProp::](imapiprop-getprops.md) GetProps para obter o valor. Ao chamar **IMAPIProp:: GetIDsFromNames**, especifique os valores apropriados para a estrutura [MAPINAMEID](mapinameid.md) indicada pelo parâmetro de entrada _lppPropNames_. O exemplo de código a seguir mostra como obter o primeiro endereço de email de um contato `lpContact`especificado, usando **GetIDsFromNames** e GetProps. **** 
  
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


