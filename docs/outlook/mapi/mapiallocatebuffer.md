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
ms.openlocfilehash: 0520b219c87207a54555ba74050761f6ecc4854a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579596"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="c2978-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c2978-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="c2978-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2978-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2978-105">Aloca um buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="c2978-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2978-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c2978-106">Header file:</span></span>  <br/> |<span data-ttu-id="c2978-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="c2978-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c2978-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="c2978-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c2978-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c2978-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c2978-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="c2978-110">Called by:</span></span>  <br/> |<span data-ttu-id="c2978-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="c2978-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="c2978-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2978-112">Parameters</span></span>

 <span data-ttu-id="c2978-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="c2978-113">_cbSize_</span></span>
  
> <span data-ttu-id="c2978-114">[in] Tamanho, em bytes, do buffer a ser alocado.</span><span class="sxs-lookup"><span data-stu-id="c2978-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="c2978-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="c2978-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="c2978-116">[out] Ponteiro para o buffer alocado retornado.</span><span class="sxs-lookup"><span data-stu-id="c2978-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c2978-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c2978-117">Return value</span></span>

<span data-ttu-id="c2978-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2978-118">S_OK</span></span> 
  
> <span data-ttu-id="c2978-119">A chamada foi bem-sucedida e retornou o buffer de memória solicitada.</span><span class="sxs-lookup"><span data-stu-id="c2978-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2978-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2978-120">Remarks</span></span>

<span data-ttu-id="c2978-121">Processamento de chamadas durante **MAPIAllocateBuffer** , a implementação chamando adquire um bloco de memória do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="c2978-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="c2978-122">O buffer de memória é alocado em um endereço de pares de byte.</span><span class="sxs-lookup"><span data-stu-id="c2978-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="c2978-123">Em plataformas onde o acesso de inteiro longo é mais eficiente, o sistema operacional aloca o buffer de um endereço cujo tamanho em bytes é um múltiplo de quatro.</span><span class="sxs-lookup"><span data-stu-id="c2978-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="c2978-124">Chamar as versões de função [MAPIFreeBuffer](mapifreebuffer.md) o buffer de memória alocado por **MAPIAllocateBuffer**, chamando-se a função [MAPIAllocateMore](mapiallocatemore.md) e qualquer buffers vinculadas a ela, quando a memória não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="c2978-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2978-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2978-125">See also</span></span>



[<span data-ttu-id="c2978-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="c2978-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

