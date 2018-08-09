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
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767989"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="a8427-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="a8427-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="a8427-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8427-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a8427-105">Aloca um buffer de memória que é vinculado a outro buffer anteriormente alocado com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a8427-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8427-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a8427-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8427-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="a8427-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="a8427-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a8427-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8427-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8427-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8427-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a8427-110">Called by:</span></span>  <br/> |<span data-ttu-id="a8427-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="a8427-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="a8427-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8427-112">Parameters</span></span>

 <span data-ttu-id="a8427-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="a8427-113">_cbSize_</span></span>
  
> <span data-ttu-id="a8427-114">[in] Tamanho, em bytes, do buffer de novo a ser alocado.</span><span class="sxs-lookup"><span data-stu-id="a8427-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="a8427-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="a8427-115">_lpObject_</span></span>
  
> <span data-ttu-id="a8427-116">[in] Ponteiro para um buffer MAPI existente alocado usando **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="a8427-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="a8427-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="a8427-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="a8427-118">[out] Ponteiro para o retornados recentemente alocado buffer.</span><span class="sxs-lookup"><span data-stu-id="a8427-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8427-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a8427-119">Return value</span></span>

<span data-ttu-id="a8427-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="a8427-120">S_OK</span></span> 
  
> <span data-ttu-id="a8427-121">A chamada foi bem-sucedida e retornou um ponteiro para a memória solicitada.</span><span class="sxs-lookup"><span data-stu-id="a8427-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a8427-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8427-122">Remarks</span></span>

<span data-ttu-id="a8427-123">Processamento de chamadas durante **MAPIAllocateMore** , a implementação chamando adquire um bloco de memória do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="a8427-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="a8427-124">O buffer de memória é alocado em um endereço de pares de byte.</span><span class="sxs-lookup"><span data-stu-id="a8427-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="a8427-125">Em plataformas onde o acesso de inteiro longo é mais eficiente, o sistema operacional aloca o buffer de um endereço cujo tamanho em bytes é um múltiplo de quatro.</span><span class="sxs-lookup"><span data-stu-id="a8427-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="a8427-126">Passe o ponteiro de buffer especificado no parâmetro _lpObject_ para a função [MAPIFreeBuffer](mapifreebuffer.md) é a única maneira de liberar um buffer alocado com **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="a8427-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="a8427-127">O vínculo entre os buffers de memória alocada com [MAPIAllocateBuffer](mapiallocatebuffer.md) e **MAPIAllocateMore** permite **MAPIFreeBuffer** ao lançamento de ambos os buffers com uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="a8427-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

