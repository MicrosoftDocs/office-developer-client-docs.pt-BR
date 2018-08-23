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
ms.openlocfilehash: 990fe49d39a73c5bf80b9fdda96d2e5997869edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595416"
---
# <a name="ssizerestriction"></a><span data-ttu-id="a5aa6-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="a5aa6-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="a5aa6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5aa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5aa6-105">Descreve uma restrição de tamanho para o qual é utilizada para testar o tamanho de um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a5aa6-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a5aa6-106">Header file:</span></span>  <br/> |<span data-ttu-id="a5aa6-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a5aa6-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="a5aa6-108">Members</span><span class="sxs-lookup"><span data-stu-id="a5aa6-108">Members</span></span>

 <span data-ttu-id="a5aa6-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="a5aa6-109">**relop**</span></span>
  
> <span data-ttu-id="a5aa6-110">Operador relacional que é usada na comparação tamanho.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="a5aa6-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="a5aa6-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="a5aa6-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="a5aa6-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="a5aa6-113">A comparação é feita com base no primeiro um valor maior ou igual.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="a5aa6-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="a5aa6-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="a5aa6-115">A comparação é feita com base em um valor maior de primeiro.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="a5aa6-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="a5aa6-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="a5aa6-117">A comparação é feita com base no primeiro um valor menor ou igual.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="a5aa6-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="a5aa6-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="a5aa6-119">A comparação é feita com base em um valor menor de primeiro.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="a5aa6-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="a5aa6-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="a5aa6-121">A comparação é feita com base nos valores desiguais.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="a5aa6-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="a5aa6-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="a5aa6-123">A comparação é feita com base em como valores (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="a5aa6-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="a5aa6-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="a5aa6-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="a5aa6-125">A comparação é feita com base nos valores iguais.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="a5aa6-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="a5aa6-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="a5aa6-127">Marca de propriedade que identifica a propriedade a ser testado.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="a5aa6-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="a5aa6-128">**cb**</span></span>
  
> <span data-ttu-id="a5aa6-129">Contagem de bytes no valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a5aa6-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5aa6-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5aa6-130">Remarks</span></span>

<span data-ttu-id="a5aa6-131">Para obter uma discussão geral de como funcionam os restrições, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="a5aa6-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5aa6-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5aa6-132">See also</span></span>



[<span data-ttu-id="a5aa6-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="a5aa6-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="a5aa6-134">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="a5aa6-134">MAPI Structures</span></span>](mapi-structures.md)

