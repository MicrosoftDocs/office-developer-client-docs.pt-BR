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
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="7cc60-103">Algoritmo para codificar IDs de entrada e IDs de anexo</span><span class="sxs-lookup"><span data-stu-id="7cc60-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="7cc60-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cc60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cc60-105">Um provedor de armazenamento pode enviar como parte de uma URL (Uniform Resource Locator) de MAPI uma ID de entrada e uma ID de anexo para o Manipulador de Protocolo MAPI para identificar um objeto que está pronto para indexação.</span><span class="sxs-lookup"><span data-stu-id="7cc60-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="7cc60-106">O provedor do armazenamento codifica a ID de entrada e a ID do anexo como cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="7cc60-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="7cc60-107">Este tópico mostra um algoritmo que gera uma representação compacta da ID de entrada ou da ID do anexo.</span><span class="sxs-lookup"><span data-stu-id="7cc60-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="7cc60-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cc60-108">See also</span></span>



[<span data-ttu-id="7cc60-109">Sobre Notification-Based Store Indexação</span><span class="sxs-lookup"><span data-stu-id="7cc60-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="7cc60-110">Sobre URLs MAPI para Notification-Based indexação</span><span class="sxs-lookup"><span data-stu-id="7cc60-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

