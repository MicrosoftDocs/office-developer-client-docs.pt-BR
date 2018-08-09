---
title: SSizeRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSizeRestriction
api_type:
- COM
ms.assetid: 4e7340d1-3cb9-4276-b83f-1c8f94acb909
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 134eb844ef7b72d396c300b27a87a3a7ae320cf1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770504"
---
# <a name="ssizerestriction"></a><span data-ttu-id="e01ab-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="e01ab-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="e01ab-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e01ab-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e01ab-105">Descreve uma restrição de tamanho para o qual é utilizada para testar o tamanho de um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="e01ab-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e01ab-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e01ab-106">Header file:</span></span>  <br/> |<span data-ttu-id="e01ab-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e01ab-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="e01ab-108">Members</span><span class="sxs-lookup"><span data-stu-id="e01ab-108">Members</span></span>

 <span data-ttu-id="e01ab-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="e01ab-109">**relop**</span></span>
  
> <span data-ttu-id="e01ab-110">Operador relacional que é usada na comparação tamanho.</span><span class="sxs-lookup"><span data-stu-id="e01ab-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="e01ab-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="e01ab-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="e01ab-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="e01ab-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="e01ab-113">A comparação é feita com base no primeiro um valor maior ou igual.</span><span class="sxs-lookup"><span data-stu-id="e01ab-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="e01ab-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="e01ab-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="e01ab-115">A comparação é feita com base em um valor maior de primeiro.</span><span class="sxs-lookup"><span data-stu-id="e01ab-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="e01ab-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="e01ab-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="e01ab-117">A comparação é feita com base no primeiro um valor menor ou igual.</span><span class="sxs-lookup"><span data-stu-id="e01ab-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="e01ab-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="e01ab-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="e01ab-119">A comparação é feita com base em um valor menor de primeiro.</span><span class="sxs-lookup"><span data-stu-id="e01ab-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="e01ab-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="e01ab-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="e01ab-121">A comparação é feita com base nos valores desiguais.</span><span class="sxs-lookup"><span data-stu-id="e01ab-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="e01ab-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="e01ab-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="e01ab-123">A comparação é feita com base em como valores (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="e01ab-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="e01ab-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="e01ab-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="e01ab-125">A comparação é feita com base nos valores iguais.</span><span class="sxs-lookup"><span data-stu-id="e01ab-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="e01ab-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="e01ab-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="e01ab-127">Marca de propriedade que identifica a propriedade a ser testado.</span><span class="sxs-lookup"><span data-stu-id="e01ab-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="e01ab-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="e01ab-128">**cb**</span></span>
  
> <span data-ttu-id="e01ab-129">Contagem de bytes no valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="e01ab-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e01ab-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="e01ab-130">Remarks</span></span>

<span data-ttu-id="e01ab-131">Para obter uma discussão geral de como funcionam os restrições, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="e01ab-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e01ab-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="e01ab-132">See also</span></span>



[<span data-ttu-id="e01ab-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="e01ab-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="e01ab-134">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="e01ab-134">MAPI Structures</span></span>](mapi-structures.md)

