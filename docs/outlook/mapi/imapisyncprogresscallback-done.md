---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e0a34e1cc0b1da1b5e2127d0697cce472c8530c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767300"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="db27b-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="db27b-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="db27b-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db27b-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="db27b-105">Informa o Microsoft Outlook que a sincronização estiver concluída.</span><span class="sxs-lookup"><span data-stu-id="db27b-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="db27b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="db27b-106">Parameters</span></span>

 <span data-ttu-id="db27b-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="db27b-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="db27b-108">Um evento que é passado voltar para permitir que o Microsoft Outlook fechar o identificador.</span><span class="sxs-lookup"><span data-stu-id="db27b-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="db27b-109">Pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="db27b-109">It can be NULL.</span></span>
    
 <span data-ttu-id="db27b-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="db27b-110">**hResult**</span></span>
  
> <span data-ttu-id="db27b-111">Um HRESULT indicando o status final do andamento.</span><span class="sxs-lookup"><span data-stu-id="db27b-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="db27b-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="db27b-112">Return value</span></span>

<span data-ttu-id="db27b-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="db27b-113">S_OK</span></span> 
  
> <span data-ttu-id="db27b-114">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="db27b-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="db27b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="db27b-115">See also</span></span>



[<span data-ttu-id="db27b-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="db27b-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

