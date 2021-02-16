---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435387"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="58c5b-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="58c5b-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="58c5b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58c5b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58c5b-105">Aloca um buffer de memória vinculado a outro buffer alocado anteriormente com a [função MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="58c5b-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="58c5b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="58c5b-106">Header file:</span></span>  <br/> |<span data-ttu-id="58c5b-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="58c5b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="58c5b-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="58c5b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="58c5b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="58c5b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="58c5b-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="58c5b-110">Called by:</span></span>  <br/> |<span data-ttu-id="58c5b-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="58c5b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="58c5b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="58c5b-112">Parameters</span></span>

 <span data-ttu-id="58c5b-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="58c5b-113">_cbSize_</span></span>
  
> <span data-ttu-id="58c5b-114">[in] Tamanho, em bytes, do novo buffer a ser alocado.</span><span class="sxs-lookup"><span data-stu-id="58c5b-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="58c5b-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="58c5b-115">_lpObject_</span></span>
  
> <span data-ttu-id="58c5b-116">[in] Ponteiro para um buffer MAPI existente alocado usando **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="58c5b-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="58c5b-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="58c5b-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="58c5b-118">[out] Ponteiro para o buffer recém-alocado retornado.</span><span class="sxs-lookup"><span data-stu-id="58c5b-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58c5b-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="58c5b-119">Return value</span></span>

<span data-ttu-id="58c5b-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="58c5b-120">S_OK</span></span> 
  
> <span data-ttu-id="58c5b-121">A chamada foi bem-sucedida e retornou um ponteiro para a memória solicitada.</span><span class="sxs-lookup"><span data-stu-id="58c5b-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58c5b-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="58c5b-122">Remarks</span></span>

<span data-ttu-id="58c5b-123">Durante o processamento de chamada **MAPIAllocateMore,** a implementação de chamada adquire um bloco de memória do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="58c5b-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="58c5b-124">O buffer de memória é alocado em um endereço de byte numerado.</span><span class="sxs-lookup"><span data-stu-id="58c5b-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="58c5b-125">Em plataformas onde o acesso inteiro longo é mais eficiente, o sistema operacional aloca o buffer em um endereço cujo tamanho em bytes é um múltiplo de quatro.</span><span class="sxs-lookup"><span data-stu-id="58c5b-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="58c5b-126">A única maneira de liberar um buffer alocado com **MAPIAllocateMore** é passar o ponteiro do buffer especificado no parâmetro _lpObject_ para a função [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="58c5b-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="58c5b-127">O link entre os buffers de memória alocados com [MAPIAllocateBuffer](mapiallocatebuffer.md) e **MAPIAllocateMore** permite que **MAPIFreeBuffer** libere ambos os buffers com uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="58c5b-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

