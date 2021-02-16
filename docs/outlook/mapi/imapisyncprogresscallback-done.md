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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8d397e12b8b24c5031e6e6d89d98134d487a815b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422345"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="9c0ba-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="9c0ba-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="9c0ba-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9c0ba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="9c0ba-105">Informa ao Microsoft Outlook que a sincronização foi concluída.</span><span class="sxs-lookup"><span data-stu-id="9c0ba-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="9c0ba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9c0ba-106">Parameters</span></span>

 <span data-ttu-id="9c0ba-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="9c0ba-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="9c0ba-108">Um evento que é passado de volta para permitir que o Microsoft Outlook feche o alça.</span><span class="sxs-lookup"><span data-stu-id="9c0ba-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="9c0ba-109">Pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="9c0ba-109">It can be NULL.</span></span>
    
 <span data-ttu-id="9c0ba-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="9c0ba-110">**hResult**</span></span>
  
> <span data-ttu-id="9c0ba-111">Um HRESULT indicando o status final do progresso.</span><span class="sxs-lookup"><span data-stu-id="9c0ba-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9c0ba-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9c0ba-112">Return value</span></span>

<span data-ttu-id="9c0ba-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9c0ba-113">S_OK</span></span> 
  
> <span data-ttu-id="9c0ba-114">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="9c0ba-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9c0ba-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="9c0ba-115">See also</span></span>



[<span data-ttu-id="9c0ba-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9c0ba-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

