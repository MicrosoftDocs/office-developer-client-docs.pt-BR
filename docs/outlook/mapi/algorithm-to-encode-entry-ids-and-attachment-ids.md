---
title: Algoritmo para codificar IDs de entrada e IDs de anexo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: b9ae6679-99b7-6509-74d4-12aa13d54928
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4d3ca89ea7d3d72f625d38e37494e253b05b1569
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577916"
---
# <a name="algorithm-to-encode-entry-ids-and-attachment-ids"></a><span data-ttu-id="eab71-103">Algoritmo para codificar IDs de entrada e IDs de anexo</span><span class="sxs-lookup"><span data-stu-id="eab71-103">Algorithm to Encode Entry IDs and Attachment IDs</span></span>

  
  
<span data-ttu-id="eab71-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eab71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eab71-105">Um provedor de armazenamento pode enviar como parte de um MAPI Uniform Resource Locator (URL) uma identificação de entrada e uma ID de anexo para o manipulador de protocolo MAPI para identificar um objeto que está pronto para indexação.</span><span class="sxs-lookup"><span data-stu-id="eab71-105">A store provider can send as part of a MAPI Uniform Resource Locator (URL) an entry ID and an attachment ID to the MAPI Protocol Handler to identify an object that is ready for indexing.</span></span> <span data-ttu-id="eab71-106">O provedor de armazenamento codifica a entrada ID e a ID do anexo como cadeias de caracteres Unicode.</span><span class="sxs-lookup"><span data-stu-id="eab71-106">The store provider encodes the entry ID and attachment ID as Unicode strings.</span></span> <span data-ttu-id="eab71-107">Este tópico mostra um algoritmo que gera uma representação compact da identificação de entrada ou ID de anexo.</span><span class="sxs-lookup"><span data-stu-id="eab71-107">This topic shows an algorithm that generates a compact representation of the entry ID or attachment ID.</span></span>
  
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

## <a name="see-also"></a><span data-ttu-id="eab71-108">Confira também</span><span class="sxs-lookup"><span data-stu-id="eab71-108">See also</span></span>



[<span data-ttu-id="eab71-109">Sobre a indexação de repositórios baseados em notificação</span><span class="sxs-lookup"><span data-stu-id="eab71-109">About Notification-Based Store Indexing</span></span>](about-notification-based-store-indexing.md)
  
[<span data-ttu-id="eab71-110">Sobre URLs MAPI para indexação baseada em notificação</span><span class="sxs-lookup"><span data-stu-id="eab71-110">About MAPI URLs for Notification-Based Indexing</span></span>](about-mapi-urls-for-notification-based-indexing.md)

