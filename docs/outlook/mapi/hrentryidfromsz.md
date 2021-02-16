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
# <a name="hrentryidfromsz"></a><span data-ttu-id="2a036-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="2a036-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="2a036-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a036-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a036-105">Recria um identificador de entrada de sua codificação ASCII.</span><span class="sxs-lookup"><span data-stu-id="2a036-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2a036-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="2a036-106">Header file:</span></span>  <br/> |<span data-ttu-id="2a036-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2a036-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2a036-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="2a036-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2a036-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2a036-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2a036-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="2a036-110">Called by:</span></span>  <br/> |<span data-ttu-id="2a036-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="2a036-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="2a036-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2a036-112">Parameters</span></span>

 <span data-ttu-id="2a036-113">_sz_</span><span class="sxs-lookup"><span data-stu-id="2a036-113">_sz_</span></span>
  
> <span data-ttu-id="2a036-114">[in] Ponteiro para a cadeia de caracteres ASCII a partir da qual criar um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="2a036-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="2a036-115">_pcb_</span><span class="sxs-lookup"><span data-stu-id="2a036-115">_pcb_</span></span>
  
> <span data-ttu-id="2a036-116">[out] Ponteiro para o tamanho, em bytes, do identificador de entrada apontado pelo _parâmetro ppentry._</span><span class="sxs-lookup"><span data-stu-id="2a036-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="2a036-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="2a036-117">_ppentry_</span></span>
  
> <span data-ttu-id="2a036-118">[out] Ponteiro para um ponteiro para a estrutura [ENTRYID retornada](entryid.md) que contém o novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="2a036-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2a036-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2a036-119">Return value</span></span>

<span data-ttu-id="2a036-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a036-120">S_OK</span></span>
  
> <span data-ttu-id="2a036-121">A recriação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2a036-121">The recreation was successful.</span></span>
    
<span data-ttu-id="2a036-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="2a036-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="2a036-123">A ID de entrada era inválida.</span><span class="sxs-lookup"><span data-stu-id="2a036-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2a036-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a036-124">Remarks</span></span>

<span data-ttu-id="2a036-125">As **funções HrEntryIDFromSz** e [HrSzFromEntryID](hrszfromentryid.md) fornecem conversão entre a cadeia de caracteres e os formatos binários dos identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="2a036-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2a036-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="2a036-126">Notes to callers</span></span>

<span data-ttu-id="2a036-127">A **função HrEntryIDFromSz** aloca memória para a cadeia de caracteres ASCII usando a [função MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="2a036-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

