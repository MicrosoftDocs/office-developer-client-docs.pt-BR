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
ms.openlocfilehash: 24ceb7b5358447de3a240756227b86224d2c354c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439083"
---
# <a name="ssizerestriction"></a><span data-ttu-id="16dc9-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="16dc9-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="16dc9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="16dc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="16dc9-105">Descreve uma restrição de tamanho que é usada para testar o tamanho de um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="16dc9-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="16dc9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="16dc9-106">Header file:</span></span>  <br/> |<span data-ttu-id="16dc9-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="16dc9-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="16dc9-108">Members</span><span class="sxs-lookup"><span data-stu-id="16dc9-108">Members</span></span>

 <span data-ttu-id="16dc9-109">**re ltda**</span><span class="sxs-lookup"><span data-stu-id="16dc9-109">**relop**</span></span>
  
> <span data-ttu-id="16dc9-110">Operador relacional que é usado na comparação de tamanho.</span><span class="sxs-lookup"><span data-stu-id="16dc9-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="16dc9-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="16dc9-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="16dc9-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="16dc9-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="16dc9-113">A comparação é feita com base em um primeiro valor maior ou igual.</span><span class="sxs-lookup"><span data-stu-id="16dc9-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="16dc9-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="16dc9-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="16dc9-115">A comparação é feita com base em um primeiro valor maior.</span><span class="sxs-lookup"><span data-stu-id="16dc9-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="16dc9-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="16dc9-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="16dc9-117">A comparação é feita com base em um primeiro valor menor ou igual.</span><span class="sxs-lookup"><span data-stu-id="16dc9-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="16dc9-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="16dc9-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="16dc9-119">A comparação é feita com base em um primeiro valor menor.</span><span class="sxs-lookup"><span data-stu-id="16dc9-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="16dc9-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="16dc9-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="16dc9-121">A comparação é feita com base em valores de valores de valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="16dc9-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="16dc9-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="16dc9-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="16dc9-123">A comparação é feita com base nos valores LIKE (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="16dc9-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="16dc9-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="16dc9-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="16dc9-125">A comparação é feita com base em valores iguais.</span><span class="sxs-lookup"><span data-stu-id="16dc9-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="16dc9-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="16dc9-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="16dc9-127">Marca de propriedade que identifica a propriedade a ser testado.</span><span class="sxs-lookup"><span data-stu-id="16dc9-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="16dc9-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="16dc9-128">**cb**</span></span>
  
> <span data-ttu-id="16dc9-129">Contagem de bytes no valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="16dc9-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="16dc9-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="16dc9-130">Remarks</span></span>

<span data-ttu-id="16dc9-131">Para uma discussão geral sobre como funcionam as restrições, consulte [Sobre restrições.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="16dc9-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="16dc9-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="16dc9-132">See also</span></span>



[<span data-ttu-id="16dc9-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="16dc9-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="16dc9-134">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="16dc9-134">MAPI Structures</span></span>](mapi-structures.md)

