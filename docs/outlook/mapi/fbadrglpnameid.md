---
title: FBadRglpNameID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FBadRglpNameID
api_type:
- COM
ms.assetid: fec5d5ac-bca6-4fff-b264-45cdb6b37f55
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 96dddc438df67b76f854827eab4dc3e210523243
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588143"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="c8fa5-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="c8fa5-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="c8fa5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8fa5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8fa5-105">Valida uma matriz de estruturas que descrevem propriedades nomeadas e verifica sua alocação.</span><span class="sxs-lookup"><span data-stu-id="c8fa5-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c8fa5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c8fa5-106">Header file:</span></span>  <br/> |<span data-ttu-id="c8fa5-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="c8fa5-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="c8fa5-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="c8fa5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c8fa5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c8fa5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c8fa5-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="c8fa5-110">Called by:</span></span>  <br/> |<span data-ttu-id="c8fa5-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="c8fa5-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="c8fa5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8fa5-112">Parameters</span></span>

 <span data-ttu-id="c8fa5-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="c8fa5-113">_lppNameId_</span></span>
  
> <span data-ttu-id="c8fa5-114">[in] Ponteiro para uma matriz de estruturas [MAPINAMEID](mapinameid.md) descrevendo as propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="c8fa5-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="c8fa5-115">_cNames_</span><span class="sxs-lookup"><span data-stu-id="c8fa5-115">_cNames_</span></span>
  
> <span data-ttu-id="c8fa5-116">[in] Contagem de estruturas de propriedade nomeada na matriz apontado pelo parâmetro _lppNameId_ .</span><span class="sxs-lookup"><span data-stu-id="c8fa5-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c8fa5-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c8fa5-117">Return value</span></span>

<span data-ttu-id="c8fa5-118">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="c8fa5-118">TRUE</span></span> 
  
> <span data-ttu-id="c8fa5-119">Um ou mais das estruturas de nome de propriedade especificado são inválido.</span><span class="sxs-lookup"><span data-stu-id="c8fa5-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="c8fa5-120">FALSO</span><span class="sxs-lookup"><span data-stu-id="c8fa5-120">FALSE</span></span> 
  
> <span data-ttu-id="c8fa5-121">As estruturas de nome de propriedade especificado são válidas.</span><span class="sxs-lookup"><span data-stu-id="c8fa5-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c8fa5-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="c8fa5-122">Remarks</span></span>

<span data-ttu-id="c8fa5-123">A função **FBadRglpNameID** pode ser usada ao configurar para uma chamada para [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="c8fa5-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

