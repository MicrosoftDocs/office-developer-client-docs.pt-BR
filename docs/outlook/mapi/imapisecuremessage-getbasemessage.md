---
title: IMAPISecureMessageGetBaseMessage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISecureMessage.GetBaseMessage
api_type:
- COM
ms.assetid: 573f40c5-e0d2-4281-8c22-10a1ae1f0dee
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 70c8bd36142d18b541ad6a2e0ded3bebcfb6dbb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767158"
---
# <a name="imapisecuremessagegetbasemessage"></a><span data-ttu-id="ec49e-103">IMAPISecureMessage::GetBaseMessage</span><span class="sxs-lookup"><span data-stu-id="ec49e-103">IMAPISecureMessage::GetBaseMessage</span></span>

  
  
<span data-ttu-id="ec49e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ec49e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ec49e-105">Recupera subjacente [IMessage: IMAPIProp](imessageimapiprop.md) que esta [IMAPISecureMessage: IUnknown](imapisecuremessageiunknown.md) é encapsular.</span><span class="sxs-lookup"><span data-stu-id="ec49e-105">Retrieves the underlying [IMessage : IMAPIProp](imessageimapiprop.md) that this [IMAPISecureMessage : IUnknown](imapisecuremessageiunknown.md) is encapsulating.</span></span> 
  
```cpp
HRESULT GetBaseMessage(
  LPMMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="ec49e-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ec49e-106">Parameters</span></span>

 <span data-ttu-id="ec49e-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="ec49e-107">_ppmsg_</span></span>
  
> <span data-ttu-id="ec49e-108">[out] Um objeto de mensagem segura.</span><span class="sxs-lookup"><span data-stu-id="ec49e-108">[out] A secure message object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ec49e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ec49e-109">Return value</span></span>

<span data-ttu-id="ec49e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ec49e-110">S_OK</span></span>
  
> <span data-ttu-id="ec49e-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="ec49e-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ec49e-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec49e-112">See also</span></span>



[<span data-ttu-id="ec49e-113">IMAPISecureMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ec49e-113">IMAPISecureMessage : IUnknown</span></span>](imapisecuremessageiunknown.md)
  
[<span data-ttu-id="ec49e-114">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ec49e-114">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

