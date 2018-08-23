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
ms.openlocfilehash: 5ae0c9f123ade599ca9bc1d3bdea3e9c89cfbc16
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594143"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="018f9-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="018f9-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="018f9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="018f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="018f9-105">Indica onde em um segmento de mensagem uma mensagem pertence.</span><span class="sxs-lookup"><span data-stu-id="018f9-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="018f9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="018f9-106">Header file:</span></span>  <br/> |<span data-ttu-id="018f9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="018f9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="018f9-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="018f9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="018f9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="018f9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="018f9-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="018f9-110">Called by:</span></span>  <br/> |<span data-ttu-id="018f9-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="018f9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="018f9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="018f9-112">Parameters</span></span>

 <span data-ttu-id="018f9-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="018f9-113">_cbParent_</span></span>
  
> <span data-ttu-id="018f9-114">[in] Contagem de bytes no índice de conversa pai.</span><span class="sxs-lookup"><span data-stu-id="018f9-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="018f9-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="018f9-115">_lpbParent_</span></span>
  
> <span data-ttu-id="018f9-116">[in] Ponteiro para bytes no índice de conversa pai.</span><span class="sxs-lookup"><span data-stu-id="018f9-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="018f9-117">Isso pode ser NULL se _cbParent_ for zero.</span><span class="sxs-lookup"><span data-stu-id="018f9-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="018f9-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="018f9-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="018f9-119">[out] Ponteiro para a contagem de bytes no índice da nova conversa retornado pela chamada.</span><span class="sxs-lookup"><span data-stu-id="018f9-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="018f9-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="018f9-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="018f9-121">[out] Ponteiro para um ponteiro para o novo índice de conversação retornado pela chamada.</span><span class="sxs-lookup"><span data-stu-id="018f9-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="018f9-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="018f9-122">Return value</span></span>

<span data-ttu-id="018f9-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="018f9-123">S_OK</span></span> 
  
> <span data-ttu-id="018f9-124">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="018f9-124">The call succeeded and has returned the expected value or values.</span></span>
    

