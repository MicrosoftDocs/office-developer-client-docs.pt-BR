---
title: BuildDisplayTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- BuildDisplayTable
api_type:
- HeaderDef
ms.assetid: 0846415b-6fe1-4504-8620-108af6719015
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b821394f32a938f4878ee93e685aafbeb0786597
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766255"
---
# <a name="builddisplaytable"></a><span data-ttu-id="8f57d-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="8f57d-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="8f57d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8f57d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8f57d-105">Cria uma tabela de exibição dos dados da página de propriedade contidos em uma ou mais estruturas [DTPAGE](dtpage.md) .</span><span class="sxs-lookup"><span data-stu-id="8f57d-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8f57d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="8f57d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8f57d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="8f57d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="8f57d-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="8f57d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="8f57d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="8f57d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="8f57d-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="8f57d-110">Called by:</span></span>  <br/> |<span data-ttu-id="8f57d-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="8f57d-111">Service providers</span></span>  <br/> |
   
```cpp
STDAPI BuildDisplayTable(
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpMalloc,
  HINSTANCE hInstance,
  UINT cPages,
  LPDTPAGE lpPage,
  ULONG ulFlags,
  LPMAPITABLE * lppTable,
  LPTABLEDATA * lppTblData
);
```

## <a name="parameters"></a><span data-ttu-id="8f57d-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f57d-112">Parameters</span></span>

 <span data-ttu-id="8f57d-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="8f57d-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="8f57d-114">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="8f57d-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="8f57d-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="8f57d-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="8f57d-116">[in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="8f57d-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="8f57d-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="8f57d-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="8f57d-118">[in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="8f57d-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="8f57d-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="8f57d-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="8f57d-120">Não utilizado; deve ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="8f57d-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="8f57d-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="8f57d-121">_hInstance_</span></span>
  
> <span data-ttu-id="8f57d-122">[in] Uma instância de um objeto MAPI do qual **BuildDisplayTable** recupera recursos.</span><span class="sxs-lookup"><span data-stu-id="8f57d-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="8f57d-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="8f57d-123">_cPages_</span></span>
  
> <span data-ttu-id="8f57d-124">[in] Contagem de estruturas [DTPAGE](dtpage.md) na matriz apontado pelo parâmetro _lpPage_ .</span><span class="sxs-lookup"><span data-stu-id="8f57d-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="8f57d-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="8f57d-125">_lpPage_</span></span>
  
> <span data-ttu-id="8f57d-126">[in] Ponteiro para uma matriz de estruturas **DTPAGE** que contêm informações sobre as páginas de tabela de exibição a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8f57d-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="8f57d-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8f57d-127">_ulFlags_</span></span>
  
> <span data-ttu-id="8f57d-128">[in] Bitmask dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="8f57d-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="8f57d-129">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="8f57d-129">The following flag can be set:</span></span>
    
<span data-ttu-id="8f57d-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8f57d-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8f57d-131">As cadeias de caracteres passada na estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8f57d-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="8f57d-132">Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8f57d-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="8f57d-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="8f57d-133">_lppTable_</span></span>
  
> <span data-ttu-id="8f57d-134">[out] Ponteiro para um ponteiro para a tabela de exibição, que expõe a interface [IMAPITable](imapitableiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="8f57d-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="8f57d-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="8f57d-135">_lppTblData_</span></span>
  
> <span data-ttu-id="8f57d-136">[além, out] Ponteiro para um ponteiro para um objeto de dados de tabela expondo a interface [ITableData](itabledataiunknown.md) na tabela retornada no parâmetro _lppTable_ .</span><span class="sxs-lookup"><span data-stu-id="8f57d-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="8f57d-137">Se nenhum objeto de dados de tabela for desejado, _lppTblData_ deve ser definido como NULL, em vez de um valor de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="8f57d-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8f57d-138">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8f57d-138">Return value</span></span>

<span data-ttu-id="8f57d-139">None</span><span class="sxs-lookup"><span data-stu-id="8f57d-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8f57d-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f57d-140">Remarks</span></span>

<span data-ttu-id="8f57d-141">O MAPI usa as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação, especificamente para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="8f57d-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8f57d-142">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="8f57d-142">Notes to callers</span></span>

<span data-ttu-id="8f57d-143">Tudo possível é lido a partir do recurso de diálogo, incluindo:</span><span class="sxs-lookup"><span data-stu-id="8f57d-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="8f57d-144">O título da página que é, o membro _ulbLpszLabel_ da estrutura [DTBLPAGE](dtblpage.md) ler o título de diálogo no recurso.</span><span class="sxs-lookup"><span data-stu-id="8f57d-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="8f57d-145">Todos os títulos de controle que é, os membros _ulbLpszLabel_ outras estruturas de controle ler o texto do controle no recurso.</span><span class="sxs-lookup"><span data-stu-id="8f57d-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="8f57d-146">**BuildDisplayTable** substitui qualquer coisa passados as estruturas de controle de entrada com as informações do recurso de diálogo, o que significa que o chamador de **BuildDisplayTable** dinamicamente não é possível especificar os títulos de página ou o controle.</span><span class="sxs-lookup"><span data-stu-id="8f57d-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="8f57d-147">Chamadores que precisam fazer o que podem ter **BuildDisplayTable** retornam o objeto de dados de tabela em _lppTableData_ e altere linhas nela; ou, eles podem criar a tabela de exibição manualmente em um objeto de dados de tabela, em vez disso.</span><span class="sxs-lookup"><span data-stu-id="8f57d-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="8f57d-148">Se _lppTableData_ não estiver definida como NULL, o provedor é responsável por liberar o objeto de dados de tabela quando ele for concluído com a tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="8f57d-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

