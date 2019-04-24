---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357306"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="dfc0d-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="dfc0d-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="dfc0d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dfc0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dfc0d-105">Aloca um buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfc0d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="dfc0d-106">Header file:</span></span>  <br/> |<span data-ttu-id="dfc0d-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="dfc0d-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="dfc0d-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="dfc0d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="dfc0d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="dfc0d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="dfc0d-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="dfc0d-110">Called by:</span></span>  <br/> |<span data-ttu-id="dfc0d-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="dfc0d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="dfc0d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfc0d-112">Parameters</span></span>

 <span data-ttu-id="dfc0d-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="dfc0d-113">_cbSize_</span></span>
  
> <span data-ttu-id="dfc0d-114">no Tamanho, em bytes, do buffer a ser alocado.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="dfc0d-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="dfc0d-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="dfc0d-116">bota Ponteiro para o buffer alocado retornado.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dfc0d-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="dfc0d-117">Return value</span></span>

<span data-ttu-id="dfc0d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfc0d-118">S_OK</span></span> 
  
> <span data-ttu-id="dfc0d-119">A chamada teve êxito e retornou o buffer de memória solicitado.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dfc0d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfc0d-120">Remarks</span></span>

<span data-ttu-id="dfc0d-121">Durante o processamento de chamada **MAPIAllocateBuffer** , a implementação de chamada adquire um bloco de memória do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="dfc0d-122">O buffer de memória é alocado em um endereço de byte par numerado.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="dfc0d-123">Nas plataformas nas quais o acesso inteiro longo é mais eficiente, o sistema operacional aloca o buffer em um endereço cujo tamanho em bytes é um múltiplo de quatro.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="dfc0d-124">Chamar a função [MAPIFreeBuffer](mapifreebuffer.md) libera o buffer de memória alocado por **MAPIAllocateBuffer**, chamando a função [MAPIAllocateMore](mapiallocatemore.md) e todos os buffers vinculados a ele, quando a memória não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="dfc0d-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfc0d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfc0d-125">See also</span></span>



[<span data-ttu-id="dfc0d-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="dfc0d-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

