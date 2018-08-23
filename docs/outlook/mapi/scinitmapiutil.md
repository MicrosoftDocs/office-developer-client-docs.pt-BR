---
title: ScInitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ScInitMapiUtil
api_type:
- HeaderDef
ms.assetid: d83b8ea8-a3b8-4038-a226-de1869c5d722
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3176280de33bda01bfd09ebaafc31d326d455a3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575032"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="72551-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="72551-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="72551-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="72551-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="72551-105">Substitui [MAPIInitialize](mapiinitialize.md) quando somente o utilitário selecionar funções estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="72551-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72551-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="72551-106">Header file:</span></span>  <br/> |<span data-ttu-id="72551-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="72551-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="72551-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="72551-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="72551-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="72551-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="72551-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="72551-110">Called by:</span></span>  <br/> |<span data-ttu-id="72551-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="72551-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="72551-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72551-112">Parameters</span></span>

 <span data-ttu-id="72551-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="72551-113">_ulFlags_</span></span>
  
> <span data-ttu-id="72551-114">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="72551-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72551-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="72551-115">Return value</span></span>

<span data-ttu-id="72551-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="72551-116">S_OK</span></span> 
  
> <span data-ttu-id="72551-117">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="72551-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72551-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="72551-118">Remarks</span></span>

<span data-ttu-id="72551-119">As funções **ScInitMapiUtil** e [DeinitMapiUtil](deinitmapiutil.md) cooperam visando chamada e funções de funções, em vez de [MAPIInitialize](mapiinitialize.md), que chama o núcleo bem como utilitário do utilitário select de lançamento.</span><span class="sxs-lookup"><span data-stu-id="72551-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="72551-120">Quando **ScInitMapiUtil** chama as funções do utilitário, ele também inicializa a memória necessária.</span><span class="sxs-lookup"><span data-stu-id="72551-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="72551-121">Quando o uso das funções que **ScInitMapiUtil** chamou estiver concluído, **DeinitMapiUtil** deve ser chamado explicitamente para liberá-los.</span><span class="sxs-lookup"><span data-stu-id="72551-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="72551-122">Por outro lado, **MAPIInitialize** implicitamente chama **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="72551-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="72551-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="72551-123">See also</span></span>



[<span data-ttu-id="72551-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="72551-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

