---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411551"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="11af3-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="11af3-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="11af3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11af3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11af3-105">Codifica um identificador de entrada em uma cadeia de caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="11af3-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11af3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="11af3-106">Header file:</span></span>  <br/> |<span data-ttu-id="11af3-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="11af3-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="11af3-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="11af3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="11af3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="11af3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="11af3-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="11af3-110">Called by:</span></span>  <br/> |<span data-ttu-id="11af3-111">Aplicativos do cliente</span><span class="sxs-lookup"><span data-stu-id="11af3-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="11af3-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11af3-112">Parameters</span></span>

 <span data-ttu-id="11af3-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="11af3-113">_cb_</span></span>
  
> <span data-ttu-id="11af3-114">[in] Tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _pentry._</span><span class="sxs-lookup"><span data-stu-id="11af3-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="11af3-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="11af3-115">_pentry_</span></span>
  
> <span data-ttu-id="11af3-116">[in] Ponteiro para uma [estrutura ENTRYID](entryid.md) que contém o identificador de entrada a ser codificado.</span><span class="sxs-lookup"><span data-stu-id="11af3-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="11af3-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="11af3-117">_psz_</span></span>
  
> <span data-ttu-id="11af3-118">[out] Ponteiro para a cadeia de caracteres ASCII retornada.</span><span class="sxs-lookup"><span data-stu-id="11af3-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="11af3-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="11af3-119">Return value</span></span>

<span data-ttu-id="11af3-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="11af3-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11af3-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="11af3-121">Remarks</span></span>

<span data-ttu-id="11af3-122">As [funções HrEntryIDFromSz](hrentryidfromsz.md) e **HrSzFromEntryID** fornecem conversão entre a cadeia de caracteres e os formatos binários dos identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="11af3-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="11af3-123">Com o MAPI, você deve usar estruturas com dados binários.</span><span class="sxs-lookup"><span data-stu-id="11af3-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="11af3-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="11af3-124">Notes to callers</span></span>

<span data-ttu-id="11af3-125">A **função HrSzFromEntryID** aloca memória para a cadeia de caracteres ASCII usando a [função MAPIAllocateBuffer.](mapiallocatebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="11af3-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

