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
ms.openlocfilehash: 3f04c5be240f63d35ea8dba0f7abbf1085f2a41d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766526"
---
# <a name="fbadrglpnameid"></a><span data-ttu-id="b0e0e-103">FBadRglpNameID</span><span class="sxs-lookup"><span data-stu-id="b0e0e-103">FBadRglpNameID</span></span>

  
  
<span data-ttu-id="b0e0e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b0e0e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b0e0e-105">Valida uma matriz de estruturas que descrevem propriedades nomeadas e verifica sua alocação.</span><span class="sxs-lookup"><span data-stu-id="b0e0e-105">Validates an array of structures that describe named properties and verifies their allocation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b0e0e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b0e0e-106">Header file:</span></span>  <br/> |<span data-ttu-id="b0e0e-107">Mapival.h</span><span class="sxs-lookup"><span data-stu-id="b0e0e-107">Mapival.h</span></span>  <br/> |
|<span data-ttu-id="b0e0e-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b0e0e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b0e0e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b0e0e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b0e0e-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b0e0e-110">Called by:</span></span>  <br/> |<span data-ttu-id="b0e0e-111">Provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="b0e0e-111">Service providers</span></span>  <br/> |
   
```cpp
BOOL FBadRglpNameID(
  LPMAPINAMEID FAR * lppNameId,
  ULONG cNames
);
```

## <a name="parameters"></a><span data-ttu-id="b0e0e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0e0e-112">Parameters</span></span>

 <span data-ttu-id="b0e0e-113">_lppNameId_</span><span class="sxs-lookup"><span data-stu-id="b0e0e-113">_lppNameId_</span></span>
  
> <span data-ttu-id="b0e0e-114">[in] Ponteiro para uma matriz de estruturas [MAPINAMEID](mapinameid.md) descrevendo as propriedades nomeadas.</span><span class="sxs-lookup"><span data-stu-id="b0e0e-114">[in] Pointer to an array of [MAPINAMEID](mapinameid.md) structures describing the named properties.</span></span> 
    
 <span data-ttu-id="b0e0e-115">_cNames_</span><span class="sxs-lookup"><span data-stu-id="b0e0e-115">_cNames_</span></span>
  
> <span data-ttu-id="b0e0e-116">[in] Contagem de estruturas de propriedade nomeada na matriz apontado pelo parâmetro _lppNameId_ .</span><span class="sxs-lookup"><span data-stu-id="b0e0e-116">[in] Count of named property structures in the array pointed to by the  _lppNameId_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b0e0e-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b0e0e-117">Return value</span></span>

<span data-ttu-id="b0e0e-118">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="b0e0e-118">TRUE</span></span> 
  
> <span data-ttu-id="b0e0e-119">Um ou mais das estruturas de nome de propriedade especificado são inválido.</span><span class="sxs-lookup"><span data-stu-id="b0e0e-119">One or more of the specified property name structures is invalid.</span></span> 
    
<span data-ttu-id="b0e0e-120">FALSO</span><span class="sxs-lookup"><span data-stu-id="b0e0e-120">FALSE</span></span> 
  
> <span data-ttu-id="b0e0e-121">As estruturas de nome de propriedade especificado são válidas.</span><span class="sxs-lookup"><span data-stu-id="b0e0e-121">The specified property name structures are all valid.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0e0e-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0e0e-122">Remarks</span></span>

<span data-ttu-id="b0e0e-123">A função **FBadRglpNameID** pode ser usada ao configurar para uma chamada para [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) ou [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span><span class="sxs-lookup"><span data-stu-id="b0e0e-123">The **FBadRglpNameID** function can be used when setting up for a call to [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) or [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).</span></span> 
  

