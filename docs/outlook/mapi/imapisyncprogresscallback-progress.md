---
title: IMAPISyncProgressCallbackProgress
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Progress
api_type:
- COM
ms.assetid: 6797cd1c-8a0b-4f42-ba56-6162d8e7b058
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 12624ef6212f9113041bf5cf3a82e2b7df6eca9e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767297"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="5fc67-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="5fc67-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="5fc67-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5fc67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5fc67-105">Atualiza o status na caixa de diálogo Enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="5fc67-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="5fc67-106">O provedor de armazenamento periodicamente chama essa função.</span><span class="sxs-lookup"><span data-stu-id="5fc67-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="5fc67-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5fc67-107">Parameters</span></span>

 <span data-ttu-id="5fc67-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="5fc67-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="5fc67-109">Um ponteiro para uma cadeia de caracteres que exibe a etapa de andamento atual.</span><span class="sxs-lookup"><span data-stu-id="5fc67-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="5fc67-110">Pode ser NULL para atualizar progresso.</span><span class="sxs-lookup"><span data-stu-id="5fc67-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="5fc67-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="5fc67-111">**ulIndex**</span></span>
  
> <span data-ttu-id="5fc67-112">A posição atual em andamento.</span><span class="sxs-lookup"><span data-stu-id="5fc67-112">The current position in progress.</span></span>
    
 <span data-ttu-id="5fc67-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="5fc67-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="5fc67-114">O índice que indica o progresso completo.</span><span class="sxs-lookup"><span data-stu-id="5fc67-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5fc67-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="5fc67-115">Return value</span></span>

<span data-ttu-id="5fc67-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5fc67-116">S_OK</span></span> 
  
> <span data-ttu-id="5fc67-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="5fc67-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5fc67-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fc67-118">See also</span></span>



[<span data-ttu-id="5fc67-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5fc67-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

