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
ms.openlocfilehash: 39a184f00ccf54d4fa4477bbdf3086f3e44bddb0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576544"
---
# <a name="freepadrlist"></a><span data-ttu-id="9fa18-103">FreePadrlist</span><span class="sxs-lookup"><span data-stu-id="9fa18-103">FreePadrlist</span></span>

  
  
<span data-ttu-id="9fa18-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9fa18-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9fa18-105">Destruir uma estrutura [ADRLIST](adrlist.md) e libera a memória associada, incluindo a memória alocada para todos os conjuntos de membro e estruturas.</span><span class="sxs-lookup"><span data-stu-id="9fa18-105">Destroys an [ADRLIST](adrlist.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fa18-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9fa18-106">Header file:</span></span>  <br/> |<span data-ttu-id="9fa18-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9fa18-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9fa18-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="9fa18-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9fa18-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9fa18-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9fa18-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="9fa18-110">Called by:</span></span>  <br/> |<span data-ttu-id="9fa18-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="9fa18-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a><span data-ttu-id="9fa18-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fa18-112">Parameters</span></span>

 <span data-ttu-id="9fa18-113">_padrlist_</span><span class="sxs-lookup"><span data-stu-id="9fa18-113">_padrlist_</span></span>
  
> <span data-ttu-id="9fa18-114">[in] Ponteiro para a estrutura **ADRLIST** para destruídos.</span><span class="sxs-lookup"><span data-stu-id="9fa18-114">[in] Pointer to the **ADRLIST** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9fa18-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9fa18-115">Return value</span></span>

<span data-ttu-id="9fa18-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="9fa18-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="9fa18-117">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="9fa18-117">Notes to callers</span></span>

<span data-ttu-id="9fa18-118">Como parte da sua implementação do **FreePadrlist**, MAPI chama a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas as entradas na estrutura de **ADRLIST** antes de liberar a estrutura completa.</span><span class="sxs-lookup"><span data-stu-id="9fa18-118">As part of its implementation of **FreePadrlist**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **ADRLIST** structure before freeing the complete structure.</span></span> <span data-ttu-id="9fa18-119">Portanto, todas as entradas de tais devem ter seguido as regras de alocação para a estrutura [ADRLIST](adrlist.md) , usando um indivíduo [MAPIAllocateBuffer](mapiallocatebuffer.md) chamadas para cada matriz de membro e estrutura.</span><span class="sxs-lookup"><span data-stu-id="9fa18-119">Therefore all such entries must have followed the allocation rules for the [ADRLIST](adrlist.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="9fa18-120">Para obter mais informações sobre a alocação de memória para as estruturas **ADRLIST** e **SRowSet** , consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="9fa18-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9fa18-121">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9fa18-121">MFCMAPI reference</span></span>

<span data-ttu-id="9fa18-122">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="9fa18-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9fa18-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="9fa18-123">**File**</span></span>|<span data-ttu-id="9fa18-124">**Function**</span><span class="sxs-lookup"><span data-stu-id="9fa18-124">**Function**</span></span>|<span data-ttu-id="9fa18-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="9fa18-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9fa18-126">MAPIABFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="9fa18-126">MAPIABFunctions.cpp</span></span>  <br/> |<span data-ttu-id="9fa18-127">AddOneOffAddress</span><span class="sxs-lookup"><span data-stu-id="9fa18-127">AddOneOffAddress</span></span>  <br/> |<span data-ttu-id="9fa18-128">MFCMAPI usa o método **FreePadrlist** para liberar uma estrutura ADRLIST que tenha sido criada para adicionar um endereço único a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="9fa18-128">MFCMAPI uses the **FreePadrlist** method to free an ADRLIST structure that was built to add a one-off address to a message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9fa18-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fa18-129">See also</span></span>



[<span data-ttu-id="9fa18-130">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="9fa18-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

