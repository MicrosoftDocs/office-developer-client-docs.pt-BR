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
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410550"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="6b787-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="6b787-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="6b787-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b787-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b787-105">Libera um buffer de memória alocado com uma chamada para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [a função MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="6b787-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b787-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6b787-106">Header file:</span></span>  <br/> |<span data-ttu-id="6b787-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="6b787-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="6b787-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6b787-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6b787-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6b787-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6b787-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6b787-110">Called by:</span></span>  <br/> |<span data-ttu-id="6b787-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6b787-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="6b787-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b787-112">Parameters</span></span>

 <span data-ttu-id="6b787-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="6b787-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="6b787-114">[in] Ponteiro para um buffer de memória alocado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6b787-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="6b787-115">Se NULL for passado no  _parâmetro lpBuffer,_ **MAPIFreeBuffer** não faz nada.</span><span class="sxs-lookup"><span data-stu-id="6b787-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6b787-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6b787-116">Return value</span></span>

<span data-ttu-id="6b787-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b787-117">S_OK</span></span> 
  
> <span data-ttu-id="6b787-118">A chamada foi bem-sucedida e liberou a memória solicitada.</span><span class="sxs-lookup"><span data-stu-id="6b787-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="6b787-119">**MAPIFreeBuffer** também pode retornar S_OK locais já liberados ou se o bloco de memória não estiver alocado com **MAPIAllocateBuffer** e **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="6b787-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b787-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b787-120">Remarks</span></span>

<span data-ttu-id="6b787-121">Normalmente, quando um aplicativo cliente ou provedor de serviços chama [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), o sistema operacional constrói em um buffer de memória contíguo uma ou mais estruturas complexas com vários níveis de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="6b787-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="6b787-122">Quando uma função ou método MAPI cria um buffer com esse conteúdo, um cliente pode liberar posteriormente todas as estruturas contidas no buffer passando para **MAPIFreeBuffer** o ponteiro para o buffer retornado pela função MAPI que criou o buffer.</span><span class="sxs-lookup"><span data-stu-id="6b787-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="6b787-123">Para um provedor de serviços liberar um buffer de memória usando **MAPIFreeBuffer**, ele deve passar o ponteiro para esse buffer retornado com o objeto de suporte do provedor.</span><span class="sxs-lookup"><span data-stu-id="6b787-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="6b787-124">A chamada para **MAPIFreeBuffer** para liberar um buffer específico deve ser feita assim que um cliente ou provedor terminar de usar esse buffer.</span><span class="sxs-lookup"><span data-stu-id="6b787-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="6b787-125">Simplesmente chamar o [método IMAPISession::Logoff](imapisession-logoff.md) no final de uma sessão MAPI não libera automaticamente buffers de memória.</span><span class="sxs-lookup"><span data-stu-id="6b787-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="6b787-126">Um cliente ou provedor de serviços deve operar na suposição de que o ponteiro passado  _em lpBuffer_ é inválido após um retorno bem-sucedido de **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="6b787-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="6b787-127">Se o ponteiro indicar um bloco de memória não alocado pelo sistema de mensagens por meio de **MAPIAllocateBuffer** ou **MAPIAllocateMore** ou um bloco de memória livre, o comportamento de **MAPIFreeBuffer** será indefinido.</span><span class="sxs-lookup"><span data-stu-id="6b787-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6b787-128">Passar um ponteiro nulo para **MAPIFreeBuffer** torna o código de limpeza do aplicativo mais simples e menor porque **MAPIFreeBuffer** pode inicializar ponteiros para NULL e, em seguida, libera-los no código de limpeza sem precisar testá-los primeiro.</span><span class="sxs-lookup"><span data-stu-id="6b787-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6b787-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b787-129">See also</span></span>



[<span data-ttu-id="6b787-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="6b787-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

