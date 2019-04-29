---
title: Algoritmo para codificar IDs de entrada e IDs de anexo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6c39fe513be122f265fdc316629a3e64a156fdc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420133"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algoritmo para codificar IDs de entrada e IDs de anexo

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de repositório pode enviar como parte de uma URL de MAPI (Uniform Resource Locator) de MAPI uma ID de entrada e uma ID de anexo para o manipulador de protocolo MAPI para identificar um objeto que está pronto para indexação. O provedor de repositório codifica a ID de entrada e a ID de anexo como cadeias de caracteres Unicode. Este tópico mostra um algoritmo que gera uma representação compacta da ID de entrada ou ID de anexo.
  
```cpp
const WORD kwBaseOffset = 0xAC00;  // Hangul char range (AC00-D7AF) 
LPWSTR EncodeID(ULONG cbEID, LPENTRYID rgbID) 
{ 
    ULONG   i = 0; 
    LPWSTR  pwzDst = NULL; 
    LPBYTE  pbSrc = NULL; 
    LPWSTR  pwzIDEncoded = NULL; 
 
    // rgbID is the item Entry ID or the attachment ID 
    // cbID is the size in bytes of rgbID 
 
    // Allocate memory for pwzIDEncoded 
    pwzIDEncoded = new WCHAR[cbEID]; 
    if (!pwzIDEncoded) return NULL; 
 
    for (i = 0, pbSrc = (LPBYTE)rgbID, pwzDst = pwzIDEncoded; 
        i < cbEID; 
        i++, pbSrc++, pwzDst++) 
    { 
        *pwzDst = (WCHAR) (*pbSrc + kwBaseOffset); 
    } 
 
    // Ensure NULL terminated 
    *pwzDst = L'\0'; 
 
    // pwzIDEncoded now contains the entry ID encoded. 
    return pwzIDEncoded; 
}
```

## <a name="see-also"></a>Confira também



[Sobre a indexação de repositórios baseados em notificação](about-notification-based-store-indexing.md)
  
[Sobre URLs MAPI para indexação baseada em notificação](about-mapi-urls-for-notification-based-indexing.md)

