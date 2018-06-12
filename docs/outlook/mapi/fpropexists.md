---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766615"
---
# <a name="fpropexists"></a><span data-ttu-id="606c8-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="606c8-103">FPropExists</span></span>

  
  
<span data-ttu-id="606c8-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="606c8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="606c8-105">Procura uma marca de propriedade fornecida em uma interface de [IMAPIProp](imapipropiunknown.md) ou um derivado do **IMAPIProp**, como [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="606c8-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="606c8-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="606c8-106">Header file:</span></span>  <br/> |<span data-ttu-id="606c8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="606c8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="606c8-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="606c8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="606c8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="606c8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="606c8-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="606c8-110">Called by:</span></span>  <br/> |<span data-ttu-id="606c8-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="606c8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="606c8-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="606c8-112">Parameters</span></span>

 <span data-ttu-id="606c8-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="606c8-113">_pobj_</span></span>
  
> <span data-ttu-id="606c8-114">[in] Ponteiro para a interface **IMAPIProp** ou derivados **IMAPIProp** dentro do qual procurar a marca de propriedade.</span><span class="sxs-lookup"><span data-stu-id="606c8-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="606c8-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="606c8-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="606c8-116">[in] Marca de propriedade a ser procurado.</span><span class="sxs-lookup"><span data-stu-id="606c8-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="606c8-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="606c8-117">Return value</span></span>

<span data-ttu-id="606c8-118">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="606c8-118">TRUE</span></span> 
  
> <span data-ttu-id="606c8-119">Foi encontrada uma correspondência para a marca de propriedade fornecida.</span><span class="sxs-lookup"><span data-stu-id="606c8-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="606c8-120">FALSO</span><span class="sxs-lookup"><span data-stu-id="606c8-120">FALSE</span></span> 
  
> <span data-ttu-id="606c8-121">Não foi encontrada uma correspondência para a marca de propriedade fornecida.</span><span class="sxs-lookup"><span data-stu-id="606c8-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="606c8-122">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="606c8-122">Remarks</span></span>

<span data-ttu-id="606c8-123">Se a marca de propriedade no parâmetro _ulPropTag_ tiver tipo PT_UNSPECIFIED, a função **FPropExists** procura por uma correspondência com base apenas no identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="606c8-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="606c8-124">Caso contrário, a correspondência diferencia para a marca de propriedade inteira, incluindo o tipo.</span><span class="sxs-lookup"><span data-stu-id="606c8-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

