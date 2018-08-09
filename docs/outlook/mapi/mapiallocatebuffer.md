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
ms.openlocfilehash: 8ba00ecc1d9ff1c0b7db63d3e6d667b374245742
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767976"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="1bfe9-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1bfe9-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="1bfe9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1bfe9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1bfe9-105">Aloca um buffer de memória.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bfe9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1bfe9-106">Header file:</span></span>  <br/> |<span data-ttu-id="1bfe9-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="1bfe9-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="1bfe9-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="1bfe9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1bfe9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1bfe9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1bfe9-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="1bfe9-110">Called by:</span></span>  <br/> |<span data-ttu-id="1bfe9-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="1bfe9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="1bfe9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1bfe9-112">Parameters</span></span>

 <span data-ttu-id="1bfe9-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="1bfe9-113">_cbSize_</span></span>
  
> <span data-ttu-id="1bfe9-114">[in] Tamanho, em bytes, do buffer a ser alocado.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="1bfe9-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="1bfe9-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="1bfe9-116">[out] Ponteiro para o buffer alocado retornado.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1bfe9-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1bfe9-117">Return value</span></span>

<span data-ttu-id="1bfe9-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="1bfe9-118">S_OK</span></span> 
  
> <span data-ttu-id="1bfe9-119">A chamada foi bem-sucedida e retornou o buffer de memória solicitada.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1bfe9-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bfe9-120">Remarks</span></span>

<span data-ttu-id="1bfe9-121">Processamento de chamadas durante **MAPIAllocateBuffer** , a implementação chamando adquire um bloco de memória do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="1bfe9-122">O buffer de memória é alocado em um endereço de pares de byte.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="1bfe9-123">Em plataformas onde o acesso de inteiro longo é mais eficiente, o sistema operacional aloca o buffer de um endereço cujo tamanho em bytes é um múltiplo de quatro.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="1bfe9-124">Chamar as versões de função [MAPIFreeBuffer](mapifreebuffer.md) o buffer de memória alocado por **MAPIAllocateBuffer**, chamando-se a função [MAPIAllocateMore](mapiallocatemore.md) e qualquer buffers vinculadas a ela, quando a memória não é mais necessária.</span><span class="sxs-lookup"><span data-stu-id="1bfe9-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1bfe9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="1bfe9-125">See also</span></span>



[<span data-ttu-id="1bfe9-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="1bfe9-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

