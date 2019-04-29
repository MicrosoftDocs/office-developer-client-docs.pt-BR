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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415534"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="82de4-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="82de4-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="82de4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82de4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82de4-105">Recupera os endereços das funções de alocação e desalocação de memória MAPI ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="82de4-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="82de4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="82de4-106">Parameters</span></span>

 <span data-ttu-id="82de4-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="82de4-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="82de4-108">bota Um ponteiro para um ponteiro para a função **MAPIAllocateBuffer** .</span><span class="sxs-lookup"><span data-stu-id="82de4-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="82de4-109">**MAPIAllocateBuffer** aloca memória.</span><span class="sxs-lookup"><span data-stu-id="82de4-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="82de4-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="82de4-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="82de4-111">bota Um ponteiro para um ponteiro para a função **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="82de4-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="82de4-112">**MAPIAllocateMore** aloca memória adicional para a memória que foi originalmente alocada usando o **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="82de4-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="82de4-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="82de4-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="82de4-114">bota Um ponteiro para um ponteiro para a função **MAPIFreeBuffer** .</span><span class="sxs-lookup"><span data-stu-id="82de4-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="82de4-115">**MAPIFreeBuffer** libera memória.</span><span class="sxs-lookup"><span data-stu-id="82de4-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="82de4-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="82de4-116">Return value</span></span>

<span data-ttu-id="82de4-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="82de4-117">S_OK</span></span> 
  
> <span data-ttu-id="82de4-118">Os endereços da função foram retornados com êxito.</span><span class="sxs-lookup"><span data-stu-id="82de4-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82de4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="82de4-119">Remarks</span></span>

<span data-ttu-id="82de4-120">O método **IMAPISupport:: GetMemAllocRoutines** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="82de4-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="82de4-121">Os provedores de serviços chamam o **GetMemAllocRoutines** para obter os endereços das três funções de alocação de memória que são passadas para a função de inicialização ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)ou [XPProviderInit](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="82de4-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82de4-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="82de4-122">See also</span></span>



[<span data-ttu-id="82de4-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="82de4-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="82de4-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="82de4-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="82de4-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="82de4-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="82de4-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="82de4-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

