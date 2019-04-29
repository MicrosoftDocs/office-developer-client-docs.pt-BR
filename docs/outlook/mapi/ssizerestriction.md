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
# <a name="ssizerestriction"></a><span data-ttu-id="7c42f-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="7c42f-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="7c42f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c42f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c42f-105">Descreve uma restrição de tamanho que é usada para testar o tamanho de um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c42f-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c42f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7c42f-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c42f-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="7c42f-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="7c42f-108">Members</span><span class="sxs-lookup"><span data-stu-id="7c42f-108">Members</span></span>

 <span data-ttu-id="7c42f-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="7c42f-109">**relop**</span></span>
  
> <span data-ttu-id="7c42f-110">Operador relacional usado na comparação de tamanho.</span><span class="sxs-lookup"><span data-stu-id="7c42f-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="7c42f-111">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="7c42f-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="7c42f-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="7c42f-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="7c42f-113">A comparação é feita com base em um valor maior ou igual a um primeiro.</span><span class="sxs-lookup"><span data-stu-id="7c42f-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="7c42f-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="7c42f-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="7c42f-115">A comparação é feita com base em um primeiro valor maior.</span><span class="sxs-lookup"><span data-stu-id="7c42f-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="7c42f-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="7c42f-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="7c42f-117">A comparação é feita com base em um valor menor ou igual a.</span><span class="sxs-lookup"><span data-stu-id="7c42f-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="7c42f-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="7c42f-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="7c42f-119">A comparação é feita com base em um primeiro valor menor.</span><span class="sxs-lookup"><span data-stu-id="7c42f-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="7c42f-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="7c42f-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="7c42f-121">A comparação é feita com base em valores desiguais.</span><span class="sxs-lookup"><span data-stu-id="7c42f-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="7c42f-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="7c42f-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="7c42f-123">A comparação é feita com base nos valores LIKE (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="7c42f-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="7c42f-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="7c42f-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="7c42f-125">A comparação é feita com base em valores iguais.</span><span class="sxs-lookup"><span data-stu-id="7c42f-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="7c42f-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="7c42f-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="7c42f-127">Marca de propriedade identificando a propriedade a ser testada.</span><span class="sxs-lookup"><span data-stu-id="7c42f-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="7c42f-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="7c42f-128">**cb**</span></span>
  
> <span data-ttu-id="7c42f-129">Contagem de bytes no valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="7c42f-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c42f-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c42f-130">Remarks</span></span>

<span data-ttu-id="7c42f-131">Para uma discussão geral de como as restrições funcionam, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="7c42f-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c42f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c42f-132">See also</span></span>



[<span data-ttu-id="7c42f-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="7c42f-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="7c42f-134">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="7c42f-134">MAPI Structures</span></span>](mapi-structures.md)

