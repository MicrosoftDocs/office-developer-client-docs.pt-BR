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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344475"
---
# <a name="ssizerestriction"></a><span data-ttu-id="ae576-103">SSizeRestriction</span><span class="sxs-lookup"><span data-stu-id="ae576-103">SSizeRestriction</span></span>

  
  
<span data-ttu-id="ae576-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae576-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ae576-105">Descreve uma restrição de tamanho que é usada para testar o tamanho de um valor de propriedade.</span><span class="sxs-lookup"><span data-stu-id="ae576-105">Describes a size restriction which is used to test the size of a property value.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae576-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ae576-106">Header file:</span></span>  <br/> |<span data-ttu-id="ae576-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="ae576-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SSizeRestriction
{
  ULONG relop;
  ULONG ulPropTag;
  ULONG cb;
} SSizeRestriction;

```

## <a name="members"></a><span data-ttu-id="ae576-108">Members</span><span class="sxs-lookup"><span data-stu-id="ae576-108">Members</span></span>

 <span data-ttu-id="ae576-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="ae576-109">**relop**</span></span>
  
> <span data-ttu-id="ae576-110">Operador relacional usado na comparação de tamanho.</span><span class="sxs-lookup"><span data-stu-id="ae576-110">Relational operator that is used in the size comparison.</span></span> <span data-ttu-id="ae576-111">Os valores possíveis são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="ae576-111">Possible values are as follows:</span></span> 
    
<span data-ttu-id="ae576-112">RELOP_GE</span><span class="sxs-lookup"><span data-stu-id="ae576-112">RELOP_GE</span></span> 
  
> <span data-ttu-id="ae576-113">A comparação é feita com base em um valor maior ou igual a um primeiro.</span><span class="sxs-lookup"><span data-stu-id="ae576-113">The comparison is made based on a greater or equal first value.</span></span>
    
<span data-ttu-id="ae576-114">RELOP_GT</span><span class="sxs-lookup"><span data-stu-id="ae576-114">RELOP_GT</span></span> 
  
> <span data-ttu-id="ae576-115">A comparação é feita com base em um primeiro valor maior.</span><span class="sxs-lookup"><span data-stu-id="ae576-115">The comparison is made based on a greater first value.</span></span>
    
<span data-ttu-id="ae576-116">RELOP_LE</span><span class="sxs-lookup"><span data-stu-id="ae576-116">RELOP_LE</span></span> 
  
> <span data-ttu-id="ae576-117">A comparação é feita com base em um valor menor ou igual a.</span><span class="sxs-lookup"><span data-stu-id="ae576-117">The comparison is made based on a lesser or equal first value.</span></span>
    
<span data-ttu-id="ae576-118">RELOP_LT</span><span class="sxs-lookup"><span data-stu-id="ae576-118">RELOP_LT</span></span> 
  
> <span data-ttu-id="ae576-119">A comparação é feita com base em um primeiro valor menor.</span><span class="sxs-lookup"><span data-stu-id="ae576-119">The comparison is made based on a lesser first value.</span></span>
    
<span data-ttu-id="ae576-120">RELOP_NE</span><span class="sxs-lookup"><span data-stu-id="ae576-120">RELOP_NE</span></span> 
  
> <span data-ttu-id="ae576-121">A comparação é feita com base em valores desiguais.</span><span class="sxs-lookup"><span data-stu-id="ae576-121">The comparison is made based on unequal values.</span></span>
    
<span data-ttu-id="ae576-122">RELOP_RE</span><span class="sxs-lookup"><span data-stu-id="ae576-122">RELOP_RE</span></span> 
  
> <span data-ttu-id="ae576-123">A comparação é feita com base nos valores LIKE (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="ae576-123">The comparison is made based on LIKE (regular expression) values.</span></span>
    
<span data-ttu-id="ae576-124">RELOP_EQ</span><span class="sxs-lookup"><span data-stu-id="ae576-124">RELOP_EQ</span></span> 
  
> <span data-ttu-id="ae576-125">A comparação é feita com base em valores iguais.</span><span class="sxs-lookup"><span data-stu-id="ae576-125">The comparison is made based on equal values.</span></span>
    
 <span data-ttu-id="ae576-126">**ulPropTag**</span><span class="sxs-lookup"><span data-stu-id="ae576-126">**ulPropTag**</span></span>
  
> <span data-ttu-id="ae576-127">Marca de propriedade identificando a propriedade a ser testada.</span><span class="sxs-lookup"><span data-stu-id="ae576-127">Property tag identifying the property to test.</span></span>
    
 <span data-ttu-id="ae576-128">**cb**</span><span class="sxs-lookup"><span data-stu-id="ae576-128">**cb**</span></span>
  
> <span data-ttu-id="ae576-129">Contagem de bytes no valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="ae576-129">Count of bytes in the property value.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ae576-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae576-130">Remarks</span></span>

<span data-ttu-id="ae576-131">Para uma discussão geral de como as restrições funcionam, consulte [about Restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="ae576-131">For a general discussion of how restrictions work, see [About Restrictions](about-restrictions.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ae576-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae576-132">See also</span></span>



[<span data-ttu-id="ae576-133">SRestriction</span><span class="sxs-lookup"><span data-stu-id="ae576-133">SRestriction</span></span>](srestriction.md)


[<span data-ttu-id="ae576-134">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="ae576-134">MAPI Structures</span></span>](mapi-structures.md)

