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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346659"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="eb46d-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="eb46d-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="eb46d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb46d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb46d-105">Libera um buffer de memória alocado com uma chamada para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) ou a função [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="eb46d-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb46d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="eb46d-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb46d-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="eb46d-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="eb46d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="eb46d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eb46d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eb46d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eb46d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="eb46d-110">Called by:</span></span>  <br/> |<span data-ttu-id="eb46d-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="eb46d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="eb46d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb46d-112">Parameters</span></span>

 <span data-ttu-id="eb46d-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="eb46d-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="eb46d-114">no Ponteiro para um buffer de memória alocado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="eb46d-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="eb46d-115">Se NULL for passado no parâmetro _lpBuffer_ , **MAPIFreeBuffer** não fará nada.</span><span class="sxs-lookup"><span data-stu-id="eb46d-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb46d-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="eb46d-116">Return value</span></span>

<span data-ttu-id="eb46d-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb46d-117">S_OK</span></span> 
  
> <span data-ttu-id="eb46d-118">A chamada teve êxito e liberou a memória solicitada.</span><span class="sxs-lookup"><span data-stu-id="eb46d-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="eb46d-119">**MAPIFreeBuffer** também pode retornar S_OK em locais já liberados ou se o bloco de memória não estiver alocado com **MAPIAllocateBuffer** e **MAPIAllocateMore**.</span><span class="sxs-lookup"><span data-stu-id="eb46d-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb46d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb46d-120">Remarks</span></span>

<span data-ttu-id="eb46d-121">Normalmente, quando um aplicativo cliente ou provedor de serviços chama [MAPIAllocateBuffer](mapiallocatebuffer.md) ou [MAPIAllocateMore](mapiallocatemore.md), o sistema operacional constrói um buffer de memória contíguo uma ou mais estruturas complexas com vários níveis de ponteiros.</span><span class="sxs-lookup"><span data-stu-id="eb46d-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="eb46d-122">Quando um método ou função MAPI cria um buffer com esse conteúdo, um cliente pode liberar mais tarde todas as estruturas contidas no buffer passando para **MAPIFreeBuffer** o ponteiro para o buffer retornado pela função MAPI que criou o buffer.</span><span class="sxs-lookup"><span data-stu-id="eb46d-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="eb46d-123">Para que um provedor de serviços Libere um buffer de memória usando o **MAPIFreeBuffer**, ele deve passar o ponteiro para o buffer retornado com o objeto support do provedor.</span><span class="sxs-lookup"><span data-stu-id="eb46d-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="eb46d-124">A chamada para **MAPIFreeBuffer** para liberar um buffer específico deve ser feita assim que um cliente ou provedor terminar de usar esse buffer.</span><span class="sxs-lookup"><span data-stu-id="eb46d-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="eb46d-125">Simplesmente chamar o método [IMAPISession:: logoff](imapisession-logoff.md) no final de uma sessão MAPI não libera buffers de memória automaticamente.</span><span class="sxs-lookup"><span data-stu-id="eb46d-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="eb46d-126">Um cliente ou provedor de serviços deve operar na pressuposição de que o ponteiro passado no _lpBuffer_ seja inválido após um retorno bem-sucedido de **MAPIFreeBuffer**.</span><span class="sxs-lookup"><span data-stu-id="eb46d-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="eb46d-127">Se o ponteiro indicar um bloco de memória não alocado pelo sistema de mensagens por meio do **MAPIAllocateBuffer** ou do **MAPIAllocateMore** ou de um bloco de memória livre, o comportamento de **MAPIFreeBuffer** é indefinido.</span><span class="sxs-lookup"><span data-stu-id="eb46d-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="eb46d-128">Passar um ponteiro nulo para o **MAPIFreeBuffer** torna o código de limpeza de aplicativos mais simples e menor porque o **MAPIFreeBuffer** pode inicializar ponteiros como nulo e, em seguida, liberá-los no código de limpeza sem precisar testá-los primeiro.</span><span class="sxs-lookup"><span data-stu-id="eb46d-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eb46d-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb46d-129">See also</span></span>



[<span data-ttu-id="eb46d-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="eb46d-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

