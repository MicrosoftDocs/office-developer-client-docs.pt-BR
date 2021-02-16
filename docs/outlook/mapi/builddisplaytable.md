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
ms.openlocfilehash: 8c5e6078be05ff846b7737ff53e9a6338fcb2141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431593"
---
# <a name="builddisplaytable"></a><span data-ttu-id="f511a-103">BuildDisplayTable</span><span class="sxs-lookup"><span data-stu-id="f511a-103">BuildDisplayTable</span></span>

  
  
<span data-ttu-id="f511a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f511a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f511a-105">Cria uma tabela de exibição a partir dos dados da página de propriedades contidos em uma ou mais [estruturas DTPAGE.](dtpage.md)</span><span class="sxs-lookup"><span data-stu-id="f511a-105">Creates a display table from the property page data contained in one or more [DTPAGE](dtpage.md) structures.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f511a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f511a-106">Header file:</span></span>  <br/> |<span data-ttu-id="f511a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f511a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f511a-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f511a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f511a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f511a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f511a-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f511a-110">Called by:</span></span>  <br/> |<span data-ttu-id="f511a-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="f511a-111">Service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f511a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f511a-112">Parameters</span></span>

 <span data-ttu-id="f511a-113">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="f511a-113">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="f511a-114">[in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="f511a-114">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="f511a-115">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="f511a-115">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="f511a-116">[in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="f511a-116">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="f511a-117">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="f511a-117">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="f511a-118">[in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="f511a-118">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="f511a-119">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="f511a-119">_lpMalloc_</span></span>
  
> <span data-ttu-id="f511a-120">Não éusado; deve ser definido como NULL.</span><span class="sxs-lookup"><span data-stu-id="f511a-120">Unused; should be set to NULL.</span></span> 
    
 <span data-ttu-id="f511a-121">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="f511a-121">_hInstance_</span></span>
  
> <span data-ttu-id="f511a-122">[in] Uma instância de um objeto MAPI do qual **BuildDisplayTable** recupera recursos.</span><span class="sxs-lookup"><span data-stu-id="f511a-122">[in] An instance of a MAPI object from which **BuildDisplayTable** retrieves resources.</span></span> 
    
 <span data-ttu-id="f511a-123">_cPages_</span><span class="sxs-lookup"><span data-stu-id="f511a-123">_cPages_</span></span>
  
> <span data-ttu-id="f511a-124">[in] Contagem de [estruturas DTPAGE](dtpage.md) na matriz apontada pelo _parâmetro lpPage._</span><span class="sxs-lookup"><span data-stu-id="f511a-124">[in] Count of [DTPAGE](dtpage.md) structures in the array pointed to by the  _lpPage_ parameter.</span></span> 
    
 <span data-ttu-id="f511a-125">_lpPage_</span><span class="sxs-lookup"><span data-stu-id="f511a-125">_lpPage_</span></span>
  
> <span data-ttu-id="f511a-126">[in] Ponteiro para uma matriz de **estruturas DTPAGE** que contêm informações sobre as páginas da tabela de exibição a serem criadas.</span><span class="sxs-lookup"><span data-stu-id="f511a-126">[in] Pointer to an array of **DTPAGE** structures that contain information about the display table pages to be built.</span></span> 
    
 <span data-ttu-id="f511a-127">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f511a-127">_ulFlags_</span></span>
  
> <span data-ttu-id="f511a-128">[in] Máscara de bits de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="f511a-128">[in] Bitmask of flags.</span></span> <span data-ttu-id="f511a-129">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f511a-129">The following flag can be set:</span></span>
    
<span data-ttu-id="f511a-130">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f511a-130">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f511a-131">As cadeias de caracteres passadas estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f511a-131">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f511a-132">Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f511a-132">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span> 
    
 <span data-ttu-id="f511a-133">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f511a-133">_lppTable_</span></span>
  
> <span data-ttu-id="f511a-134">[out] Ponteiro para um ponteiro para a tabela de exibição, que expõe a interface [IMAPITable.](imapitableiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="f511a-134">[out] Pointer to a pointer to the display table, which exposes the [IMAPITable](imapitableiunknown.md) interface.</span></span> 
    
 <span data-ttu-id="f511a-135">_lppTblData_</span><span class="sxs-lookup"><span data-stu-id="f511a-135">_lppTblData_</span></span>
  
> <span data-ttu-id="f511a-136">[in, out] Ponteiro para um ponteiro para um objeto de dados de tabela expondo a interface [ITableData](itabledataiunknown.md) na tabela retornada no _parâmetro lppTable._</span><span class="sxs-lookup"><span data-stu-id="f511a-136">[in, out] Pointer to a pointer to a table data object exposing the [ITableData](itabledataiunknown.md) interface on the table returned in the  _lppTable_ parameter.</span></span> <span data-ttu-id="f511a-137">Se nenhum objeto de dados de tabela for desejado,  _lppTblData_ deverá ser definido como NULL em vez de um valor de ponteiro.</span><span class="sxs-lookup"><span data-stu-id="f511a-137">If no table data object is desired,  _lppTblData_ should be set to NULL instead of a pointer value.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f511a-138">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f511a-138">Return value</span></span>

<span data-ttu-id="f511a-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="f511a-139">None</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f511a-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="f511a-140">Remarks</span></span>

<span data-ttu-id="f511a-141">MAPI uses the functions pointed to  _by lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such [as IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="f511a-141">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f511a-142">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f511a-142">Notes to callers</span></span>

<span data-ttu-id="f511a-143">Tudo o que é possível é lido a partir do recurso de caixa de diálogo, incluindo:</span><span class="sxs-lookup"><span data-stu-id="f511a-143">Everything possible is read from the dialog resource, including:</span></span>
  
- <span data-ttu-id="f511a-144">O título da página, ou seja, o  _membro ulbLpszLabel_ da estrutura [DTBLPAGE](dtblpage.md) lida a partir do título da caixa de diálogo no recurso.</span><span class="sxs-lookup"><span data-stu-id="f511a-144">The page title that is, the  _ulbLpszLabel_ member of the [DTBLPAGE](dtblpage.md) structure read from the dialog title in the resource.</span></span> 
    
- <span data-ttu-id="f511a-145">Todos os títulos de controle, ou seja, os membros  _ulbLpszLabel_ de outras estruturas de controle lidos do texto de controle no recurso.</span><span class="sxs-lookup"><span data-stu-id="f511a-145">All control titles that is, the  _ulbLpszLabel_ members of other control structures read from the control text in the resource.</span></span> 
    
 <span data-ttu-id="f511a-146">**BuildDisplayTable** substitui qualquer coisa passada nas estruturas de controle de entrada com informações do recurso de caixa de diálogo, o que significa que o chamador de **BuildDisplayTable** não pode especificar dinamicamente títulos de página ou controle.</span><span class="sxs-lookup"><span data-stu-id="f511a-146">**BuildDisplayTable** overwrites anything passed in the input control structures with information from the dialog resource, which means the caller of **BuildDisplayTable** cannot dynamically specify page or control titles.</span></span> <span data-ttu-id="f511a-147">Os chamadores que precisam fazer isso podem fazer **BuildDisplayTable** retornar o objeto de dados de tabela em  _lppTableData_ e alterar linhas nele; ou eles podem criar a tabela de exibição manualmente em um objeto de dados de tabela.</span><span class="sxs-lookup"><span data-stu-id="f511a-147">Callers who need to do that can have **BuildDisplayTable** return the table data object in  _lppTableData_ and change rows in it; or they can build the display table by hand in a table data object instead.</span></span> 
  
<span data-ttu-id="f511a-148">Se  _lppTableData_ não estiver definido como NULL, o provedor será responsável por liberar o objeto de dados da tabela quando terminar com a tabela de exibição.</span><span class="sxs-lookup"><span data-stu-id="f511a-148">If  _lppTableData_ is not set to NULL, the provider is responsible for freeing the table data object when it is finished with the display table.</span></span> 
  

