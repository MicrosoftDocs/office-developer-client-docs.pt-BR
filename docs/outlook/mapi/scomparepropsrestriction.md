---
title: SComparePropsRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SComparePropsRestriction
api_type:
- COM
ms.assetid: 3231a91a-1ef2-4dd8-9f3e-79ca56d2eae9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7177b2f0f709939b7580fa7abb87490073bb00c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588808"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="d19dc-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="d19dc-103">SComparePropsRestriction</span></span>

<span data-ttu-id="d19dc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d19dc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d19dc-105">Descreve uma restrição de propriedade de comparação, qual testa duas propriedades usando um operador relacional.</span><span class="sxs-lookup"><span data-stu-id="d19dc-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d19dc-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="d19dc-106">Header file:</span></span>  <br/> |<span data-ttu-id="d19dc-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d19dc-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="d19dc-108">Members</span><span class="sxs-lookup"><span data-stu-id="d19dc-108">Members</span></span>

<span data-ttu-id="d19dc-109">**RelOp**</span><span class="sxs-lookup"><span data-stu-id="d19dc-109">**relop**</span></span>
  
> <span data-ttu-id="d19dc-110">Operador relacional a ser usado para comparar as duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d19dc-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="d19dc-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="d19dc-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="d19dc-112">RELOP_GE: A comparação é feita com base no primeiro um valor maior ou igual.</span><span class="sxs-lookup"><span data-stu-id="d19dc-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="d19dc-113">RELOP_GT: A comparação é feita com base em um valor maior de primeiro.</span><span class="sxs-lookup"><span data-stu-id="d19dc-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="d19dc-114">RELOP_LE: A comparação é feita com base no primeiro um valor menor ou igual.</span><span class="sxs-lookup"><span data-stu-id="d19dc-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="d19dc-115">RELOP_LT: A comparação é feita com base em um valor menor de primeiro.</span><span class="sxs-lookup"><span data-stu-id="d19dc-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="d19dc-116">RELOP_NE: A comparação é feita com base nos valores desiguais.</span><span class="sxs-lookup"><span data-stu-id="d19dc-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="d19dc-117">RELOP_RE: A comparação é feita com base em como valores (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="d19dc-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="d19dc-118">RELOP_EQ: A comparação é feita com base nos valores iguais.</span><span class="sxs-lookup"><span data-stu-id="d19dc-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="d19dc-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="d19dc-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="d19dc-120">Marca de propriedade da primeira propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="d19dc-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="d19dc-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="d19dc-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="d19dc-122">Marca de propriedade da segunda propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="d19dc-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d19dc-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="d19dc-123">Remarks</span></span>

<span data-ttu-id="d19dc-124">A ordem de comparação é _(1) (operador relacional) de marca de propriedade (marca de propriedade 2)_.</span><span class="sxs-lookup"><span data-stu-id="d19dc-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="d19dc-125">As propriedades a serem comparadas devem ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="d19dc-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="d19dc-126">Faz com que tentando comparar propriedades de diferentes tipos de MAPI ou o provedor de serviços para retornar o valor de erro MAPI_E_TOO_COMPLEX do método [IMAPITable](imapitableiunknown.md) ao qual a estrutura é passada como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d19dc-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="d19dc-127">O resultado de uma restrição de valor de propriedade de comparação é indefinido quando uma ou ambas as propriedades não existem.</span><span class="sxs-lookup"><span data-stu-id="d19dc-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="d19dc-128">Quando um cliente exige comportamento bem definido para uma restrição tal e não é certeza se a propriedade existe (por exemplo, não é uma coluna obrigatória de uma tabela) deve criar uma restrição de **e** para ingressar a restrição de propriedade comparar com um existe restrição.</span><span class="sxs-lookup"><span data-stu-id="d19dc-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="d19dc-129">Use uma estrutura de [SExistRestriction](sexistrestriction.md) para definir a restrição existe e uma estrutura de [SAndRestriction](sandrestriction.md) para definir a restrição **AND** .</span><span class="sxs-lookup"><span data-stu-id="d19dc-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="d19dc-130">As propriedades especificadas nos membros **ulPropTag1** e **ulPropTag2** podem ser valores múltiplos se o provedor de serviços lhe fornecer apoio.</span><span class="sxs-lookup"><span data-stu-id="d19dc-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="d19dc-131">Para obter mais informações sobre a estrutura de **SComparePropsRestriction** e restrições em geral, consulte [Sobre restrições](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="d19dc-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d19dc-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="d19dc-132">See also</span></span>

- [<span data-ttu-id="d19dc-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="d19dc-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="d19dc-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="d19dc-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="d19dc-135">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="d19dc-135">MAPI Structures</span></span>](mapi-structures.md)

