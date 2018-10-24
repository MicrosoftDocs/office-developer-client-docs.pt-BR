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
ms.openlocfilehash: cdd3db3f3779c2078b90352e19f8da6b29cffb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573200"
---
# <a name="imapisyncprogresscallbackdone"></a><span data-ttu-id="8d8aa-103">IMAPISyncProgressCallback::Done</span><span class="sxs-lookup"><span data-stu-id="8d8aa-103">IMAPISyncProgressCallback::Done</span></span>

  
  
<span data-ttu-id="8d8aa-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8d8aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8d8aa-105">Informa o Microsoft Outlook que a sincronização estiver concluída.</span><span class="sxs-lookup"><span data-stu-id="8d8aa-105">Informs Microsoft Outlook that synchronization is complete.</span></span> 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a><span data-ttu-id="8d8aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8d8aa-106">Parameters</span></span>

 <span data-ttu-id="8d8aa-107">**hThreadDoneEvent**</span><span class="sxs-lookup"><span data-stu-id="8d8aa-107">**hThreadDoneEvent**</span></span>
  
> <span data-ttu-id="8d8aa-108">Um evento que é passado voltar para permitir que o Microsoft Outlook fechar o identificador.</span><span class="sxs-lookup"><span data-stu-id="8d8aa-108">An event that is passed back to allow Microsoft Outlook to close the handle.</span></span> <span data-ttu-id="8d8aa-109">Pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="8d8aa-109">It can be NULL.</span></span>
    
 <span data-ttu-id="8d8aa-110">**hResult**</span><span class="sxs-lookup"><span data-stu-id="8d8aa-110">**hResult**</span></span>
  
> <span data-ttu-id="8d8aa-111">Um HRESULT indicando o status final do andamento.</span><span class="sxs-lookup"><span data-stu-id="8d8aa-111">An HRESULT indicating final status of the progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8d8aa-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8d8aa-112">Return value</span></span>

<span data-ttu-id="8d8aa-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8d8aa-113">S_OK</span></span> 
  
> <span data-ttu-id="8d8aa-114">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="8d8aa-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8d8aa-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d8aa-115">See also</span></span>



[<span data-ttu-id="8d8aa-116">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d8aa-116">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

