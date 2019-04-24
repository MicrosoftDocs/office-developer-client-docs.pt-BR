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
ms.openlocfilehash: 090a73ed908d2a647d00de27b93538a77766c258
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351258"
---
# <a name="scinitmapiutil"></a><span data-ttu-id="5053c-103">ScInitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="5053c-103">ScInitMapiUtil</span></span>

  
  
<span data-ttu-id="5053c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5053c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5053c-105">Substitui [MAPIInitialize](mapiinitialize.md) quando apenas as funções de utilitário são usadas.</span><span class="sxs-lookup"><span data-stu-id="5053c-105">Replaces [MAPIInitialize](mapiinitialize.md) when only select utility functions are being used.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5053c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5053c-106">Header file:</span></span>  <br/> |<span data-ttu-id="5053c-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="5053c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="5053c-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5053c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="5053c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="5053c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="5053c-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5053c-110">Called by:</span></span>  <br/> |<span data-ttu-id="5053c-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="5053c-111">Client applications</span></span>  <br/> |
   
```cpp
SCODE ScInitMapiUtil(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="5053c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5053c-112">Parameters</span></span>

 <span data-ttu-id="5053c-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5053c-113">_ulFlags_</span></span>
  
> <span data-ttu-id="5053c-114">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="5053c-114">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5053c-115">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5053c-115">Return value</span></span>

<span data-ttu-id="5053c-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5053c-116">S_OK</span></span> 
  
> <span data-ttu-id="5053c-117">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="5053c-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5053c-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="5053c-118">Remarks</span></span>

<span data-ttu-id="5053c-119">As funções **ScInitMapiUtil** e [DeinitMapiUtil](deinitmapiutil.md) cooperam para chamar e liberar funções do utilitário Select, em vez de [MAPIInitialize](mapiinitialize.md), que chama o núcleo, bem como funções utilitárias.</span><span class="sxs-lookup"><span data-stu-id="5053c-119">The **ScInitMapiUtil** and [DeinitMapiUtil](deinitmapiutil.md) functions cooperate to call and release select utility functions, as opposed to [MAPIInitialize](mapiinitialize.md), which calls core as well as utility functions.</span></span> <span data-ttu-id="5053c-120">Quando o **ScInitMapiUtil** chama funções de utilitário, ele também inicializa a memória necessária.</span><span class="sxs-lookup"><span data-stu-id="5053c-120">When **ScInitMapiUtil** calls utility functions, it also initializes the necessary memory.</span></span> 
  
<span data-ttu-id="5053c-121">Quando o uso das funções que o **ScInitMapiUtil** chamou estiver concluído, **DeinitMapiUtil** deverá ser explicitamente chamado para liberá-las.</span><span class="sxs-lookup"><span data-stu-id="5053c-121">When use of the functions that **ScInitMapiUtil** has called is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="5053c-122">Por outro lado, **MAPIInitialize** chama implicitamente **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="5053c-122">In contrast, **MAPIInitialize** implicitly calls **DeinitMapiUtil**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5053c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="5053c-123">See also</span></span>



[<span data-ttu-id="5053c-124">MAPIUninitialize</span><span class="sxs-lookup"><span data-stu-id="5053c-124">MAPIUninitialize</span></span>](mapiuninitialize.md)

