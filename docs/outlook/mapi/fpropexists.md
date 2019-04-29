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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429485"
---
# <a name="fpropexists"></a><span data-ttu-id="59030-103">FPropExists</span><span class="sxs-lookup"><span data-stu-id="59030-103">FPropExists</span></span>

  
  
<span data-ttu-id="59030-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="59030-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="59030-105">Procura uma determinada marca de propriedade em uma interface do [IMAPIProp](imapipropiunknown.md) ou uma interface derivada de **IMAPIProp**, como [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md).</span><span class="sxs-lookup"><span data-stu-id="59030-105">Searches for a given property tag in an [IMAPIProp](imapipropiunknown.md) interface or an interface derived from **IMAPIProp**, such as [IMessage](imessageimapiprop.md) or [IMAPIFolder](imapifolderimapicontainer.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59030-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="59030-106">Header file:</span></span>  <br/> |<span data-ttu-id="59030-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="59030-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="59030-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="59030-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="59030-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="59030-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="59030-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="59030-110">Called by:</span></span>  <br/> |<span data-ttu-id="59030-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="59030-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a><span data-ttu-id="59030-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59030-112">Parameters</span></span>

 <span data-ttu-id="59030-113">_pobj_</span><span class="sxs-lookup"><span data-stu-id="59030-113">_pobj_</span></span>
  
> <span data-ttu-id="59030-114">no Ponteiro para a interface **IMAPIProp** ou a interface derivada de **IMAPIProp** dentro da qual procurar a marca da propriedade.</span><span class="sxs-lookup"><span data-stu-id="59030-114">[in] Pointer to the **IMAPIProp** interface or interface derived from **IMAPIProp** within which to search for the property tag.</span></span> 
    
 <span data-ttu-id="59030-115">_ulPropTag_</span><span class="sxs-lookup"><span data-stu-id="59030-115">_ulPropTag_</span></span>
  
> <span data-ttu-id="59030-116">no Marca de propriedade para a qual Pesquisar.</span><span class="sxs-lookup"><span data-stu-id="59030-116">[in] Property tag for which to search.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="59030-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="59030-117">Return value</span></span>

<span data-ttu-id="59030-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="59030-118">TRUE</span></span> 
  
> <span data-ttu-id="59030-119">Uma correspondência para a marca de propriedade fornecida foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="59030-119">A match for the given property tag was found.</span></span> 
    
<span data-ttu-id="59030-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="59030-120">FALSE</span></span> 
  
> <span data-ttu-id="59030-121">Uma correspondência para a marca de propriedade fornecida não foi encontrada.</span><span class="sxs-lookup"><span data-stu-id="59030-121">A match for the given property tag was not found.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="59030-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="59030-122">Remarks</span></span>

<span data-ttu-id="59030-123">Se a marca de propriedade no parâmetro _ulPropTag_ tiver o tipo PT_UNSPECIFIED, a função **FPropExists** procurará uma correspondência com base apenas no identificador de propriedade.</span><span class="sxs-lookup"><span data-stu-id="59030-123">If the property tag in the  _ulPropTag_ parameter has type PT_UNSPECIFIED, the **FPropExists** function looks for a match based only on the property identifier.</span></span> <span data-ttu-id="59030-124">Caso contrário, a correspondência é para a marca de propriedade inteira, incluindo o tipo.</span><span class="sxs-lookup"><span data-stu-id="59030-124">Otherwise, the match is for the entire property tag, including the type.</span></span> 
  

