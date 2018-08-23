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
ms.openlocfilehash: 0e6226dd0fc9c04070ed3d1dda1770f77fbc585c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583005"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="272e6-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="272e6-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="272e6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="272e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="272e6-105">Aloca um buffer de memória que é vinculado a outro buffer anteriormente alocado com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="272e6-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="272e6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="272e6-106">Header file:</span></span>  <br/> |<span data-ttu-id="272e6-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="272e6-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="272e6-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="272e6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="272e6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="272e6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="272e6-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="272e6-110">Called by:</span></span>  <br/> |<span data-ttu-id="272e6-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="272e6-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="272e6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="272e6-112">Parameters</span></span>

 <span data-ttu-id="272e6-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="272e6-113">_cbSize_</span></span>
  
> <span data-ttu-id="272e6-114">[in] Tamanho, em bytes, do buffer de novo a ser alocado.</span><span class="sxs-lookup"><span data-stu-id="272e6-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="272e6-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="272e6-115">_lpObject_</span></span>
  
> <span data-ttu-id="272e6-116">[in] Ponteiro para um buffer MAPI existente alocado usando **MAPIAllocateBuffer**.</span><span class="sxs-lookup"><span data-stu-id="272e6-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="272e6-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="272e6-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="272e6-118">[out] Ponteiro para o retornados recentemente alocado buffer.</span><span class="sxs-lookup"><span data-stu-id="272e6-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="272e6-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="272e6-119">Return value</span></span>

<span data-ttu-id="272e6-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="272e6-120">S_OK</span></span> 
  
> <span data-ttu-id="272e6-121">A chamada foi bem-sucedida e retornou um ponteiro para a memória solicitada.</span><span class="sxs-lookup"><span data-stu-id="272e6-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="272e6-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="272e6-122">Remarks</span></span>

<span data-ttu-id="272e6-123">Processamento de chamadas durante **MAPIAllocateMore** , a implementação chamando adquire um bloco de memória do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="272e6-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="272e6-124">O buffer de memória é alocado em um endereço de pares de byte.</span><span class="sxs-lookup"><span data-stu-id="272e6-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="272e6-125">Em plataformas onde o acesso de inteiro longo é mais eficiente, o sistema operacional aloca o buffer de um endereço cujo tamanho em bytes é um múltiplo de quatro.</span><span class="sxs-lookup"><span data-stu-id="272e6-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="272e6-126">Passe o ponteiro de buffer especificado no parâmetro _lpObject_ para a função [MAPIFreeBuffer](mapifreebuffer.md) é a única maneira de liberar um buffer alocado com **MAPIAllocateMore** .</span><span class="sxs-lookup"><span data-stu-id="272e6-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="272e6-127">O vínculo entre os buffers de memória alocada com [MAPIAllocateBuffer](mapiallocatebuffer.md) e **MAPIAllocateMore** permite **MAPIFreeBuffer** ao lançamento de ambos os buffers com uma única chamada.</span><span class="sxs-lookup"><span data-stu-id="272e6-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

