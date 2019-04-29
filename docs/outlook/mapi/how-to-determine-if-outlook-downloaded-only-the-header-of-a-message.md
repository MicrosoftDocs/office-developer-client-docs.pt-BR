---
title: Determinar se o Outlook baixou somente o cabeçalho de uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: acc96bb9-1592-c480-53ee-1325f65297e1
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 9671126c0d83064d926f4211468cdfa6ebf43270
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428148"
---
# <a name="determine-if-outlook-downloaded-only-the-header-of-a-message"></a><span data-ttu-id="22873-103">Determinar se o Outlook baixou somente o cabeçalho de uma mensagem</span><span class="sxs-lookup"><span data-stu-id="22873-103">Determine if Outlook downloaded only the header of a message</span></span>

<span data-ttu-id="22873-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22873-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22873-105">Este tópico mostra um exemplo de código no Visual C++ que usa a [propriedade nomeada PidLidHeaderItem canônica](pidlidheaderitem-canonical-property.md) para determinar se o Microsoft Outlook 2013 baixou apenas o cabeçalho de uma mensagem ou o cabeçalho e o corpo de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="22873-105">This topic shows a code sample in Visual C++ that uses the named [PidLidHeaderItem Canonical Property](pidlidheaderitem-canonical-property.md) to determine whether Microsoft Outlook 2013 has downloaded only the header of a message or the header and the body of a message.</span></span> 
  
```cpp
BOOL bIsHeader(LPMESSAGE lpMessage) 
{ 
    HRESULT         hRes = S_OK; 
    BOOL            bRet = false; 
    ULONG    ulVal = 0; 
    LPSPropValue    lpPropVal = NULL; 
    LPSPropTagArray lpNamedPropTag = NULL; 
    MAPINAMEID      NamedID = {0}; 
    LPMAPINAMEID    lpNamedID = NULL; 
 
    NamedID.lpguid = (LPGUID) &PSETID_Common; 
    NamedID.ulKind = MNID_ID; 
    NamedID.Kind.lID = dispidHeaderItem; 
    lpNamedID = &NamedID; 
    hRes = lpMessage->GetIDsFromNames(1, &lpNamedID, NULL, &lpNamedPropTag); 
 
    if (lpNamedPropTag && 1 == lpNamedPropTag->cValues) 
    { 
lpNamedPropTag->aulPropTag[0] = CHANGE_PROP_TYPE(lpNamedPropTag->aulPropTag[0], PT_LONG); 
 
//Get the value of the property. 
hRes = lpMessage->GetProps(lpNamedPropTag, 0, &ulVal, &lpPropVal); 
if (lpPropVal && 1 == ulVal && PT_LONG == PROP_TYPE(lpPropVal->ulPropTag) && lpPropVal->Value.ul) 
{ 
    bRet = true; 
} 
    } 
 
    MAPIFreeBuffer(lpPropVal); 
    MAPIFreeBuffer(lpNamedPropTag); 
    return bRet; 
}

```


