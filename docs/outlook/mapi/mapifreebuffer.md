---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ad3d9d12e1073610747b0ab078c6d65c09f8c7c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569138"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="394be-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="394be-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="394be-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="394be-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="394be-105">Libera um buffer de memória alocado com uma chamada para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) ou a função [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="394be-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="394be-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="394be-106">Header file:</span></span>  <br/> |<span data-ttu-id="394be-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="394be-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="394be-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="394be-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="394be-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="394be-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="394be-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="394be-110">Called by:</span></span>  <br/> |<span data-ttu-id="394be-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="394be-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="394be-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="394be-112">Parameters</span></span>

 <span data-ttu-id="394be-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="394be-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="394be-114">[in] Ponteiro para um buffer de memória alocada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="394be-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="394be-115">Se NULL é passada no parâmetro _lpBuffer_ , **MAPIFreeBuffer** não fará nada.</span><span class="sxs-lookup"><span data-stu-id="394be-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="394be-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="394be-116">Return value</span></span>

<span data-ttu-id="394be-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="394be-117">S_OK</span></span> 
  
> <span data-ttu-id="394be-118">A chamada foi bem-sucedida e a memória solicitada liberada.</span><span class="sxs-lookup"><span data-stu-id="394be-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="394be-119">**MAPIFreeBuffer** também pode retornar S_OK em locais de liberação já ou se o bloco de memória não alocado com **MAPIAllocateBuffer** e **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="394be-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="394be-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="394be-120">Remarks</span></span>

<span data-ttu-id="394be-121">Normalmente, quando um aplicativo cliente ou um provedor de serviços chama [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), as construções de sistema operacional no buffer de memória contíguos um uma ou mais estruturas complexas com vários níveis de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="394be-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="394be-122">Quando uma função MAPI ou o método cria um buffer com tal conteúdo, um cliente posteriormente pode liberar todas as estruturas contidas no buffer, passando para **MAPIFreeBuffer** o ponteiro para o buffer retornado pela função MAPI que criou o buffer.</span><span class="sxs-lookup"><span data-stu-id="394be-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="394be-123">Para um provedor de serviço liberar um buffer de memória usando **MAPIFreeBuffer**, ele deve passar o ponteiro para esse buffer retornado com o objeto de suporte do provedor.</span><span class="sxs-lookup"><span data-stu-id="394be-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="394be-124">A chamada para **MAPIFreeBuffer** para liberar um buffer específico deve ser feita assim que um cliente ou provedor for concluído usando esse buffer.</span><span class="sxs-lookup"><span data-stu-id="394be-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="394be-125">Basta chamar o método de [IMAPISession::Logoff](imapisession-logoff.md) no final de uma sessão MAPI não libera automaticamente buffers de memória.</span><span class="sxs-lookup"><span data-stu-id="394be-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="394be-126">Um provedor de cliente ou serviço deve operar no pressuposto de que o ponteiro transmitido _lpBuffer_ é inválido após um retorno bem-sucedido de **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="394be-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="394be-127">Se o ponteiro indica um bloco de memória não alocado pelo sistema de mensagens por meio de **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou um bloco de memória disponível, o comportamento do **MAPIFreeBuffer** é indefinido.</span><span class="sxs-lookup"><span data-stu-id="394be-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="394be-128">Passar um ponteiro nulo para **MAPIFreeBuffer** torna o código de limpeza do aplicativo simples e menor porque **MAPIFreeBuffer** pode inicializar ponteiros para NULL e livre no código limpeza sem precisar testá-las pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="394be-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="394be-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="394be-129">See also</span></span>



[<span data-ttu-id="394be-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="394be-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

