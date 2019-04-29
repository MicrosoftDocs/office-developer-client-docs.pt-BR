---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408639"
---
# <a name="freepadrlist"></a><span data-ttu-id="1c458-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="1c458-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="1c458-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c458-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c458-105">Destrói uma estrutura [das ADRLIST](adrlist.md) e libera a memória associada, incluindo a memória alocada para todas as matrizes e estruturas de membros.</span><span class="sxs-lookup"><span data-stu-id="1c458-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c458-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1c458-106">Header file:</span></span>  <br/> |<span data-ttu-id="1c458-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="1c458-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1c458-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1c458-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1c458-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1c458-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1c458-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="1c458-110">Called by:</span></span>  <br/> |<span data-ttu-id="1c458-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="1c458-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="1c458-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c458-112">Parameters</span></span>

 <span data-ttu-id="1c458-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="1c458-113">_padrlist_</span></span>
  
> <span data-ttu-id="1c458-114">no Ponteiro para a estrutura **das ADRLIST** a ser destruído.</span><span class="sxs-lookup"><span data-stu-id="1c458-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1c458-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1c458-115">Return value</span></span>

<span data-ttu-id="1c458-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="1c458-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1c458-117">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1c458-117">Notes to callers</span></span>

<span data-ttu-id="1c458-118">Como parte de sua implementação do **FreePadrlist**, MAPI chama a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas as entradas da estrutura **das ADRLIST** antes de liberar a estrutura completa.</span><span class="sxs-lookup"><span data-stu-id="1c458-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="1c458-119">Portanto, todas as entradas devem ter seguido as regras de alocação para a estrutura [das ADRLIST](adrlist.md) , usando uma chamada [MAPIAllocateBuffer](mapiallocatebuffer.md) individual para cada matriz de membros e estrutura.</span><span class="sxs-lookup"><span data-stu-id="1c458-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="1c458-120">Para obter mais informações sobre a alocação de memória para as estruturas **das ADRLIST** e **SRowSet** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="1c458-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1c458-121">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1c458-121">MFCMAPI reference</span></span>

<span data-ttu-id="1c458-122">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c458-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1c458-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="1c458-123">**File**</span></span>|<span data-ttu-id="1c458-124">**Função**</span><span class="sxs-lookup"><span data-stu-id="1c458-124">**Function**</span></span>|<span data-ttu-id="1c458-125">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="1c458-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1c458-126">MAPIABFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="1c458-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1c458-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="1c458-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="1c458-128">MFCMAPI usa o método **FreePadrlist** para liberar uma estrutura das ADRLIST que foi criada para adicionar um endereço one-off a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="1c458-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c458-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c458-129">See also</span></span>



[<span data-ttu-id="1c458-130">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="1c458-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

