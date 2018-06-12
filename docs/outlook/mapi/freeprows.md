---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 93659a28969efd0d04e9fc44f8926e89586f7773
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766617"
---
# <a name="freeprows"></a><span data-ttu-id="e4b0f-103">FreeProws</span><span class="sxs-lookup"><span data-stu-id="e4b0f-103">FreeProws</span></span>

  
  
<span data-ttu-id="e4b0f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e4b0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e4b0f-105">Destruir uma estrutura [SRowSet](srowset.md) e libera a memória associada, incluindo a memória alocada para todos os conjuntos de membro e estruturas.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-105">Destroys an [SRowSet](srowset.md) structure and frees associated memory, including memory allocated for all member arrays and structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4b0f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e4b0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="e4b0f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="e4b0f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="e4b0f-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="e4b0f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e4b0f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e4b0f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e4b0f-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="e4b0f-110">Called by:</span></span>  <br/> |<span data-ttu-id="e4b0f-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="e4b0f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a><span data-ttu-id="e4b0f-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="e4b0f-112">Parameters</span></span>

 <span data-ttu-id="e4b0f-113">_prows_</span><span class="sxs-lookup"><span data-stu-id="e4b0f-113">_prows_</span></span>
  
> <span data-ttu-id="e4b0f-114">[in] Ponteiro para a estrutura de **SRowSet** para destruídos.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-114">[in] Pointer to the **SRowSet** structure to be destroyed.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e4b0f-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e4b0f-115">Return value</span></span>

<span data-ttu-id="e4b0f-116">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-116">None.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e4b0f-117">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="e4b0f-117">Notes to callers</span></span>

<span data-ttu-id="e4b0f-118">Como parte da sua implementação do **FreeProws**, MAPI chama a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas as entradas na estrutura de **SRowSet** antes de liberar a estrutura completa.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-118">As part of its implementation of **FreeProws**, MAPI calls the [MAPIFreeBuffer](mapifreebuffer.md) function to free every entry in the **SRowSet** structure before freeing the complete structure.</span></span> <span data-ttu-id="e4b0f-119">Portanto, todas as entradas de tais devem ter seguido as regras de alocação para a estrutura [SRowSet](srowset.md) , usando um indivíduo [MAPIAllocateBuffer](mapiallocatebuffer.md) chamadas para cada matriz de membro e estrutura.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-119">Therefore all such entries must have followed the allocation rules for the [SRowSet](srowset.md) structure, using an individual [MAPIAllocateBuffer](mapiallocatebuffer.md) call for each member array and structure.</span></span> 
  
<span data-ttu-id="e4b0f-120">Para obter mais informações sobre a alocação de memória para as estruturas **ADRLIST** e **SRowSet** , consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md).</span><span class="sxs-lookup"><span data-stu-id="e4b0f-120">For more information about allocating memory for **ADRLIST** and **SRowSet** structures, see [Managing Memory for ADRLIST and SRowSet Structures](managing-memory-for-adrlist-and-srowset-structures.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e4b0f-121">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e4b0f-121">MFCMAPI reference</span></span>

<span data-ttu-id="e4b0f-122">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e4b0f-123">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="e4b0f-123">**File**</span></span>|<span data-ttu-id="e4b0f-124">**Function**</span><span class="sxs-lookup"><span data-stu-id="e4b0f-124">**Function**</span></span>|<span data-ttu-id="e4b0f-125">**Comment**</span><span class="sxs-lookup"><span data-stu-id="e4b0f-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4b0f-126">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="e4b0f-126">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="e4b0f-127">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="e4b0f-127">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="e4b0f-128">MFCMAPI usa o método **FreeProws** para liberar uma estrutura SRowSet contendo as linhas da tabela que estão sendo processadas.</span><span class="sxs-lookup"><span data-stu-id="e4b0f-128">MFCMAPI uses the **FreeProws** method to free an SRowSet structure containing rows of the table being processed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e4b0f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4b0f-129">See also</span></span>



[<span data-ttu-id="e4b0f-130">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="e4b0f-130">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

