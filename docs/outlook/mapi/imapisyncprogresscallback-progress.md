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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9b44337a4bc9615558ac6337e99ea206ba063b1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429107"
---
# <a name="imapisyncprogresscallbackprogress"></a><span data-ttu-id="17d92-103">IMAPISyncProgressCallback::Progress</span><span class="sxs-lookup"><span data-stu-id="17d92-103">IMAPISyncProgressCallback::Progress</span></span>

  
  
<span data-ttu-id="17d92-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17d92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17d92-105">Atualiza o status na caixa de diálogo enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="17d92-105">Updates the status in the Send/Receive dialog.</span></span> <span data-ttu-id="17d92-106">O provedor de repositórios chama periodicamente essa função.</span><span class="sxs-lookup"><span data-stu-id="17d92-106">The store provider periodically calls this function.</span></span>
  
```cpp
HRESULT Progress(
  const WCHAR *pwcszProgress, 
  ULONG ulIndex, 
  ULONG ulIndexMax
);
```

## <a name="parameters"></a><span data-ttu-id="17d92-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17d92-107">Parameters</span></span>

 <span data-ttu-id="17d92-108">**pwczsProgress**</span><span class="sxs-lookup"><span data-stu-id="17d92-108">**pwczsProgress**</span></span>
  
> <span data-ttu-id="17d92-109">Um ponteiro para uma cadeia de caracteres que exibe a etapa de progresso atual.</span><span class="sxs-lookup"><span data-stu-id="17d92-109">A pointer to a string that displays the current progress step.</span></span> <span data-ttu-id="17d92-110">Pode ser nulo para atualizar o andamento.</span><span class="sxs-lookup"><span data-stu-id="17d92-110">It can be NULL to update progress.</span></span>
    
 <span data-ttu-id="17d92-111">**ulIndex**</span><span class="sxs-lookup"><span data-stu-id="17d92-111">**ulIndex**</span></span>
  
> <span data-ttu-id="17d92-112">A posição atual em andamento.</span><span class="sxs-lookup"><span data-stu-id="17d92-112">The current position in progress.</span></span>
    
 <span data-ttu-id="17d92-113">**ulIndexMax**</span><span class="sxs-lookup"><span data-stu-id="17d92-113">**ulIndexMax**</span></span>
  
> <span data-ttu-id="17d92-114">O índice que indica o progresso completo.</span><span class="sxs-lookup"><span data-stu-id="17d92-114">The index indicating complete progress.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="17d92-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="17d92-115">Return value</span></span>

<span data-ttu-id="17d92-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="17d92-116">S_OK</span></span> 
  
> <span data-ttu-id="17d92-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="17d92-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="17d92-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="17d92-118">See also</span></span>



[<span data-ttu-id="17d92-119">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="17d92-119">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)

