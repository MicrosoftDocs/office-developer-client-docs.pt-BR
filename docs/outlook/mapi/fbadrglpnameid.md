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
ms.openlocfilehash: 4eef7c0b1078cb9e7ced21e2403f0b3948362d6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434827"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="03d97-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="03d97-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="03d97-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03d97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03d97-105">Valida uma matriz de estruturas que descrevem propriedades nomeadas e verifica sua alocação.</span><span class="sxs-lookup"><span data-stu-id="03d97-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="03d97-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="03d97-106">Header file:</span></span>  <br/> |<span data-ttu-id="03d97-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="03d97-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="03d97-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="03d97-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="03d97-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="03d97-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="03d97-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="03d97-110">Called by:</span></span>  <br/> |<span data-ttu-id="03d97-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="03d97-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="03d97-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="03d97-112">Parameters</span></span>

 <span data-ttu-id="03d97-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="03d97-113">_lppNameId_</span></span>
  
> <span data-ttu-id="03d97-114">[in] Ponteiro para uma matriz de [estruturas MAPINAMEID](mapinameid.md) que descrevem as propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="03d97-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="03d97-115">_cNames_</span><span class="sxs-lookup"><span data-stu-id="03d97-115">_cNames_</span></span>
  
> <span data-ttu-id="03d97-116">[in] Contagem de estruturas de propriedades nomeadas na matriz apontada pelo _parâmetro lppNameId._</span><span class="sxs-lookup"><span data-stu-id="03d97-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="03d97-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="03d97-117">Return value</span></span>

<span data-ttu-id="03d97-118">TRUE</span><span class="sxs-lookup"><span data-stu-id="03d97-118">TRUE</span></span> 
  
> <span data-ttu-id="03d97-119">Uma ou mais das estruturas de nome de propriedade especificadas são inválidas.</span><span class="sxs-lookup"><span data-stu-id="03d97-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="03d97-120">FALSE</span><span class="sxs-lookup"><span data-stu-id="03d97-120">FALSE</span></span> 
  
> <span data-ttu-id="03d97-121">Todas as estruturas de nome de propriedade especificadas são válidas.</span><span class="sxs-lookup"><span data-stu-id="03d97-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="03d97-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="03d97-122">Remarks</span></span>

<span data-ttu-id="03d97-123">A **função FBadRglpNameID** pode ser usada ao configurar uma chamada para [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="03d97-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

