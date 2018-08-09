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
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766789"
---
# <a name="hrentryidfromsz"></a><span data-ttu-id="ee3d2-103">HrEntryIDFromSz</span><span class="sxs-lookup"><span data-stu-id="ee3d2-103">HrEntryIDFromSz</span></span>

  
  
<span data-ttu-id="ee3d2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ee3d2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ee3d2-105">Recria um identificador de entrada de sua codificação ASCII.</span><span class="sxs-lookup"><span data-stu-id="ee3d2-105">Recreates an entry identifier from its ASCII encoding.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee3d2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ee3d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="ee3d2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ee3d2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ee3d2-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ee3d2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ee3d2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ee3d2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ee3d2-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ee3d2-110">Called by:</span></span>  <br/> |<span data-ttu-id="ee3d2-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="ee3d2-111">Client applications</span></span>  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a><span data-ttu-id="ee3d2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee3d2-112">Parameters</span></span>

 <span data-ttu-id="ee3d2-113">_SZ_</span><span class="sxs-lookup"><span data-stu-id="ee3d2-113">_sz_</span></span>
  
> <span data-ttu-id="ee3d2-114">[in] Ponteiro para a cadeia de caracteres ASCII do qual criar um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="ee3d2-114">[in] Pointer to the ASCII string from which to create an entry identifier.</span></span> 
    
 <span data-ttu-id="ee3d2-115">_PCB_</span><span class="sxs-lookup"><span data-stu-id="ee3d2-115">_pcb_</span></span>
  
> <span data-ttu-id="ee3d2-116">[out] Ponteiro para o tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _ppentry_ .</span><span class="sxs-lookup"><span data-stu-id="ee3d2-116">[out] Pointer to the size, in bytes, of the entry identifier pointed to by the  _ppentry_ parameter.</span></span> 
    
 <span data-ttu-id="ee3d2-117">_ppentry_</span><span class="sxs-lookup"><span data-stu-id="ee3d2-117">_ppentry_</span></span>
  
> <span data-ttu-id="ee3d2-118">[out] Ponteiro para um ponteiro para a estrutura [ENTRYID](entryid.md) retornado que contém o novo identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="ee3d2-118">[out] Pointer to a pointer to the returned [ENTRYID](entryid.md) structure that contains the new entry identifier.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ee3d2-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ee3d2-119">Return value</span></span>

<span data-ttu-id="ee3d2-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="ee3d2-120">S_OK</span></span>
  
> <span data-ttu-id="ee3d2-121">A recriação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ee3d2-121">The recreation was successful.</span></span>
    
<span data-ttu-id="ee3d2-122">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="ee3d2-122">MAPI_E_INVALID_ENTRYID</span></span>
  
> <span data-ttu-id="ee3d2-123">A identificação de entrada era inválida.</span><span class="sxs-lookup"><span data-stu-id="ee3d2-123">The entry ID was invalid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ee3d2-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee3d2-124">Remarks</span></span>

<span data-ttu-id="ee3d2-125">As funções **HrEntryIDFromSz** e [HrSzFromEntryID](hrszfromentryid.md) fornecem conversão entre a cadeia de caracteres e formatos binários de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="ee3d2-125">The **HrEntryIDFromSz** and [HrSzFromEntryID](hrszfromentryid.md) functions provide conversion between the string and binary formats of entry identifiers.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ee3d2-126">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="ee3d2-126">Notes to callers</span></span>

<span data-ttu-id="ee3d2-127">A função **HrEntryIDFromSz** aloca memória para a cadeia de caracteres ASCII usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ee3d2-127">The **HrEntryIDFromSz** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

