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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766806"
---
# <a name="hrszfromentryid"></a><span data-ttu-id="0611f-103">HrSzFromEntryID</span><span class="sxs-lookup"><span data-stu-id="0611f-103">HrSzFromEntryID</span></span>

  
  
<span data-ttu-id="0611f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0611f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0611f-105">Codifica um identificador de entrada em uma sequência de caracteres ASCII.</span><span class="sxs-lookup"><span data-stu-id="0611f-105">Encodes an entry identifier into an ASCII string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0611f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="0611f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0611f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="0611f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="0611f-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="0611f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0611f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0611f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0611f-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="0611f-110">Called by:</span></span>  <br/> |<span data-ttu-id="0611f-111">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="0611f-111">Client applications</span></span>  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a><span data-ttu-id="0611f-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="0611f-112">Parameters</span></span>

 <span data-ttu-id="0611f-113">_cb_</span><span class="sxs-lookup"><span data-stu-id="0611f-113">_cb_</span></span>
  
> <span data-ttu-id="0611f-114">[in] Tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _pentry_ .</span><span class="sxs-lookup"><span data-stu-id="0611f-114">[in] Size, in bytes, of the entry identifier pointed to by the  _pentry_ parameter.</span></span> 
    
 <span data-ttu-id="0611f-115">_pentry_</span><span class="sxs-lookup"><span data-stu-id="0611f-115">_pentry_</span></span>
  
> <span data-ttu-id="0611f-116">[in] Ponteiro para uma estrutura [ENTRYID](entryid.md) que contém o identificador de entrada a ser codificada.</span><span class="sxs-lookup"><span data-stu-id="0611f-116">[in] Pointer to an [ENTRYID](entryid.md) structure that contains the entry identifier to be encoded.</span></span> 
    
 <span data-ttu-id="0611f-117">_psz_</span><span class="sxs-lookup"><span data-stu-id="0611f-117">_psz_</span></span>
  
> <span data-ttu-id="0611f-118">[out] Ponteiro para a cadeia de caracteres ASCII retornado.</span><span class="sxs-lookup"><span data-stu-id="0611f-118">[out] Pointer to the returned ASCII string.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0611f-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0611f-119">Return value</span></span>

<span data-ttu-id="0611f-120">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="0611f-120">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0611f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0611f-121">Remarks</span></span>

<span data-ttu-id="0611f-122">As funções [HrEntryIDFromSz](hrentryidfromsz.md) e **HrSzFromEntryID** fornecem conversão entre a cadeia de caracteres e formatos binários de identificadores de entrada.</span><span class="sxs-lookup"><span data-stu-id="0611f-122">The [HrEntryIDFromSz](hrentryidfromsz.md) and **HrSzFromEntryID** functions provide conversion between the string and binary formats of entry identifiers.</span></span> <span data-ttu-id="0611f-123">Com MAPI, você deve usar as estruturas com dados binários.</span><span class="sxs-lookup"><span data-stu-id="0611f-123">With MAPI, you should use structures with binary data.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0611f-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0611f-124">Notes to callers</span></span>

<span data-ttu-id="0611f-125">A função **HrSzFromEntryID** aloca memória para a cadeia de caracteres ASCII usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0611f-125">The **HrSzFromEntryID** function allocates memory for the ASCII string using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  

