---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437725"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="480e5-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="480e5-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="480e5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="480e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="480e5-105">Recria um identificador de entrada da codificação ASCII.</span><span class="sxs-lookup"><span data-stu-id="480e5-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="480e5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="480e5-106">Header file:</span></span>  <br/> |<span data-ttu-id="480e5-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="480e5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="480e5-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="480e5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="480e5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="480e5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="480e5-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="480e5-110">Called by:</span></span>  <br/> |<span data-ttu-id="480e5-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="480e5-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="480e5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="480e5-112">Parameters</span></span>

 <span data-ttu-id="480e5-113">_v_</span><span class="sxs-lookup"><span data-stu-id="480e5-113">_sz_</span></span>
  
> <span data-ttu-id="480e5-114">no Ponteiro para a cadeia de caracteres ASCII da qual criar um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="480e5-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="480e5-115">_PCB_</span><span class="sxs-lookup"><span data-stu-id="480e5-115">_pcb_</span></span>
  
> <span data-ttu-id="480e5-116">bota Ponteiro para o tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _ppentry_ .</span><span class="sxs-lookup"><span data-stu-id="480e5-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="480e5-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="480e5-117">_ppentry_</span></span>
  
> <span data-ttu-id="480e5-118">bota Ponteiro para um ponteiro para a estrutura [EntryID](entryid.md) retornada que contém o novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="480e5-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="480e5-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="480e5-119">Return value</span></span>

<span data-ttu-id="480e5-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="480e5-120">S_OK</span></span>
  
> <span data-ttu-id="480e5-121">A recreação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="480e5-121">The recreation was successful.</span></span>
    
<span data-ttu-id="480e5-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="480e5-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="480e5-123">A identificação de entrada era inválida.</span><span class="sxs-lookup"><span data-stu-id="480e5-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="480e5-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="480e5-124">Remarks</span></span>

<span data-ttu-id="480e5-125">As funções **HrEntryIDFromSz** e [HrSzFromEntryID](hrszfromentryid.md) fornecem conversão entre a cadeia de caracteres e os formatos binários de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="480e5-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="480e5-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="480e5-126">Notes to callers</span></span>

<span data-ttu-id="480e5-127">A função **HrEntryIDFromSz** aloca memória para a cadeia de caracteres ASCII usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="480e5-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

