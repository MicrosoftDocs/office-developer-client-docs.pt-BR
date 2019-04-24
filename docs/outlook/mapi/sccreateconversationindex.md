---
title: ScCreateConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCreateConversationIndex
api_type:
- COM
ms.assetid: 3ccfc15d-f3c6-4c7b-b1cc-855af66036de
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 385660889c40e5f59dfc015ad92ce6a1398ab0cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351321"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="1ed64-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="1ed64-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="1ed64-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ed64-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ed64-105">Indica em que local da mensagem um segmento de mensagem pertence.</span><span class="sxs-lookup"><span data-stu-id="1ed64-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ed64-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1ed64-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ed64-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="1ed64-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1ed64-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1ed64-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1ed64-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1ed64-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1ed64-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="1ed64-110">Called by:</span></span>  <br/> |<span data-ttu-id="1ed64-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="1ed64-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="1ed64-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ed64-112">Parameters</span></span>

 <span data-ttu-id="1ed64-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="1ed64-113">_cbParent_</span></span>
  
> <span data-ttu-id="1ed64-114">no Contagem de bytes no índice de conversa pai.</span><span class="sxs-lookup"><span data-stu-id="1ed64-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="1ed64-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="1ed64-115">_lpbParent_</span></span>
  
> <span data-ttu-id="1ed64-116">no Ponteiro para bytes no índice de conversa pai.</span><span class="sxs-lookup"><span data-stu-id="1ed64-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="1ed64-117">Isso pode ser NULL se _cbParent_ for zero.</span><span class="sxs-lookup"><span data-stu-id="1ed64-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="1ed64-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="1ed64-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="1ed64-119">bota Ponteiro para a contagem de bytes no novo índice de conversa retornado pela chamada.</span><span class="sxs-lookup"><span data-stu-id="1ed64-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="1ed64-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="1ed64-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="1ed64-121">bota Ponteiro para um ponteiro para o novo índice de conversa retornado pela chamada.</span><span class="sxs-lookup"><span data-stu-id="1ed64-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1ed64-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1ed64-122">Return value</span></span>

<span data-ttu-id="1ed64-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ed64-123">S_OK</span></span> 
  
> <span data-ttu-id="1ed64-124">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="1ed64-124">The call succeeded and has returned the expected value or values.</span></span>
    

