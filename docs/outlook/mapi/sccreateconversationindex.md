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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415653"
---
# <a name="sccreateconversationindex"></a><span data-ttu-id="f4c90-103">ScCreateConversationIndex</span><span class="sxs-lookup"><span data-stu-id="f4c90-103">ScCreateConversationIndex</span></span>

  
  
<span data-ttu-id="f4c90-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4c90-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4c90-105">Indica onde uma mensagem pertence em um thread de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f4c90-105">Indicates where in a message thread a message belongs.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f4c90-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f4c90-106">Header file:</span></span>  <br/> |<span data-ttu-id="f4c90-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f4c90-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f4c90-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f4c90-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f4c90-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f4c90-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f4c90-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f4c90-110">Called by:</span></span>  <br/> |<span data-ttu-id="f4c90-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="f4c90-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCreateConversationIndex(
  ULONG cbParent,
  LPBYTE lpbParent,
  ULONG FAR* lpcbIndex,
  LPBYTE FAR * lppbIndex
);
```

## <a name="parameters"></a><span data-ttu-id="f4c90-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f4c90-112">Parameters</span></span>

 <span data-ttu-id="f4c90-113">_cbParent_</span><span class="sxs-lookup"><span data-stu-id="f4c90-113">_cbParent_</span></span>
  
> <span data-ttu-id="f4c90-114">[in] Contagem de bytes no índice da conversa pai.</span><span class="sxs-lookup"><span data-stu-id="f4c90-114">[in] Count of bytes in the parent conversation index.</span></span>
    
 <span data-ttu-id="f4c90-115">_lpbParent_</span><span class="sxs-lookup"><span data-stu-id="f4c90-115">_lpbParent_</span></span>
  
> <span data-ttu-id="f4c90-116">[in] Ponteiro para bytes no índice de conversa pai.</span><span class="sxs-lookup"><span data-stu-id="f4c90-116">[in] Pointer to bytes in the parent conversation index.</span></span> <span data-ttu-id="f4c90-117">Isso poderá ser NULL se  _cbParent_ for zero.</span><span class="sxs-lookup"><span data-stu-id="f4c90-117">This may be NULL if  _cbParent_ is zero.</span></span> 
    
 <span data-ttu-id="f4c90-118">_lpcbIndex_</span><span class="sxs-lookup"><span data-stu-id="f4c90-118">_lpcbIndex_</span></span>
  
> <span data-ttu-id="f4c90-119">[out] Ponteiro para a contagem de bytes no novo índice de conversa retornado pela chamada.</span><span class="sxs-lookup"><span data-stu-id="f4c90-119">[out] Pointer to the count of bytes in the new conversation index returned by the call.</span></span> 
    
 <span data-ttu-id="f4c90-120">_lppbIndex_</span><span class="sxs-lookup"><span data-stu-id="f4c90-120">_lppbIndex_</span></span>
  
> <span data-ttu-id="f4c90-121">[out] Ponteiro para um ponteiro para o novo índice de conversa retornado pela chamada.</span><span class="sxs-lookup"><span data-stu-id="f4c90-121">[out] Pointer to a pointer to the new conversation index returned by the call.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f4c90-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f4c90-122">Return value</span></span>

<span data-ttu-id="f4c90-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f4c90-123">S_OK</span></span> 
  
> <span data-ttu-id="f4c90-124">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="f4c90-124">The call succeeded and has returned the expected value or values.</span></span>
    

