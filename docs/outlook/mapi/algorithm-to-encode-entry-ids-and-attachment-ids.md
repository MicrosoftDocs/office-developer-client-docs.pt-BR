---
title: Algoritmo para codificar identificações de entrada e anexo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 710ba5173dcce6e948e1f49c7d82e46bc83b8200
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766169"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a>Algoritmo para codificar identificações de entrada e anexo

  
  
**Aplica-se a**: Outlook 
  
Um provedor de armazenamento pode enviar como parte de um MAPI Uniform Resource Locator (URL) uma identificação de entrada e uma ID de anexo para o manipulador de protocolo MAPI para identificar um objeto que está pronto para indexação. O provedor de armazenamento codifica a entrada ID e a ID do anexo como cadeias de caracteres Unicode. Este tópico mostra um algoritmo que gera uma representação compact da identificação de entrada ou ID de anexo.
  
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



[Sobre a indexação do repositório baseada em notificação](about-notification-based-store-indexing.md)
  
[Sobre URLs MAPI para indexação baseada em notificação](about-mapi-urls-for-notification-based-indexing.md)

