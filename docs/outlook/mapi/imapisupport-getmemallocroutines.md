---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577811"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="0356c-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="0356c-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="0356c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0356c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0356c-105">Recupera os endereços das MAPI memória alocação e desalocação funções ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="0356c-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="0356c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0356c-106">Parameters</span></span>

 <span data-ttu-id="0356c-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="0356c-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="0356c-108">[out] Um ponteiro para um ponteiro para a função **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="0356c-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="0356c-109">**MAPIAllocateBuffer** aloca memória.</span><span class="sxs-lookup"><span data-stu-id="0356c-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="0356c-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="0356c-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="0356c-111">[out] Um ponteiro para um ponteiro para a função **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="0356c-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="0356c-112">**MAPIAllocateMore** aloca memória adicional para memória que foi originalmente alocada usando **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="0356c-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="0356c-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="0356c-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="0356c-114">[out] Um ponteiro para um ponteiro para a função **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="0356c-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="0356c-115">**MAPIFreeBuffer** libera a memória.</span><span class="sxs-lookup"><span data-stu-id="0356c-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0356c-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0356c-116">Return value</span></span>

<span data-ttu-id="0356c-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="0356c-117">S_OK</span></span> 
  
> <span data-ttu-id="0356c-118">Os endereços de função foram retornados com êxito.</span><span class="sxs-lookup"><span data-stu-id="0356c-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0356c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="0356c-119">Remarks</span></span>

<span data-ttu-id="0356c-120">O método **IMAPISupport::GetMemAllocRoutines** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="0356c-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="0356c-121">Provedores de serviços de chamarem **GetMemAllocRoutines** para obter os endereços das funções de alocação de três memória que são passados para as suas funções de inicialização ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)ou [XPProviderInit](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="0356c-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0356c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0356c-122">See also</span></span>



[<span data-ttu-id="0356c-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0356c-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="0356c-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="0356c-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="0356c-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="0356c-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="0356c-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="0356c-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

