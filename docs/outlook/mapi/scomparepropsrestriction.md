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
ms.openlocfilehash: 513ec0db4e99e687d8aeb9e1d6acdef73df4d158
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33440000"
---
# <a name="scomparepropsrestriction"></a><span data-ttu-id="31d9d-103">SComparePropsRestriction</span><span class="sxs-lookup"><span data-stu-id="31d9d-103">SComparePropsRestriction</span></span>

<span data-ttu-id="31d9d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31d9d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31d9d-105">Descreve uma restrição de propriedade de comparação, que testa duas propriedades usando um operador relacional.</span><span class="sxs-lookup"><span data-stu-id="31d9d-105">Describes a compare property restriction, which tests two properties using a relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31d9d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="31d9d-106">Header file:</span></span>  <br/> |<span data-ttu-id="31d9d-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="31d9d-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _SComparePropsRestriction
{
  ULONG relop;
  ULONG ulPropTag1;
  ULONG ulPropTag2;
} SComparePropsRestriction;

```

## <a name="members"></a><span data-ttu-id="31d9d-108">Members</span><span class="sxs-lookup"><span data-stu-id="31d9d-108">Members</span></span>

<span data-ttu-id="31d9d-109">**re ltda**</span><span class="sxs-lookup"><span data-stu-id="31d9d-109">**relop**</span></span>
  
> <span data-ttu-id="31d9d-110">Operador relacional a ser usado para comparar as duas propriedades.</span><span class="sxs-lookup"><span data-stu-id="31d9d-110">Relational operator to use to compare the two properties.</span></span> <span data-ttu-id="31d9d-111">Os valores possíveis são:</span><span class="sxs-lookup"><span data-stu-id="31d9d-111">Possible values are as follows:</span></span>
    
  - <span data-ttu-id="31d9d-112">RELOP_GE: a comparação é feita com base em um primeiro valor maior ou igual.</span><span class="sxs-lookup"><span data-stu-id="31d9d-112">RELOP_GE: The comparison is made based on a greater or equal first value.</span></span>
      
  - <span data-ttu-id="31d9d-113">RELOP_GT: a comparação é feita com base em um primeiro valor maior.</span><span class="sxs-lookup"><span data-stu-id="31d9d-113">RELOP_GT: The comparison is made based on a greater first value.</span></span>
      
  - <span data-ttu-id="31d9d-114">RELOP_LE: a comparação é feita com base em um primeiro valor menor ou igual.</span><span class="sxs-lookup"><span data-stu-id="31d9d-114">RELOP_LE: The comparison is made based on a lesser or equal first value.</span></span>
      
  - <span data-ttu-id="31d9d-115">RELOP_LT: a comparação é feita com base em um primeiro valor menor.</span><span class="sxs-lookup"><span data-stu-id="31d9d-115">RELOP_LT: The comparison is made based on a lesser first value.</span></span>
      
  - <span data-ttu-id="31d9d-116">RELOP_NE: a comparação é feita com base em valores de valores de valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="31d9d-116">RELOP_NE: The comparison is made based on unequal values.</span></span>
      
  - <span data-ttu-id="31d9d-117">RELOP_RE: a comparação é feita com base nos valores LIKE (expressão regular).</span><span class="sxs-lookup"><span data-stu-id="31d9d-117">RELOP_RE: The comparison is made based on LIKE (regular expression) values.</span></span>
      
  - <span data-ttu-id="31d9d-118">RELOP_EQ: a comparação é feita com base em valores iguais.</span><span class="sxs-lookup"><span data-stu-id="31d9d-118">RELOP_EQ: The comparison is made based on equal values.</span></span>
    
<span data-ttu-id="31d9d-119">**ulPropTag1**</span><span class="sxs-lookup"><span data-stu-id="31d9d-119">**ulPropTag1**</span></span>
  
> <span data-ttu-id="31d9d-120">Marca de propriedade da primeira propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="31d9d-120">Property tag of the first property to be compared.</span></span> 
    
<span data-ttu-id="31d9d-121">**ulPropTag2**</span><span class="sxs-lookup"><span data-stu-id="31d9d-121">**ulPropTag2**</span></span>
  
> <span data-ttu-id="31d9d-122">Marca de propriedade da segunda propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="31d9d-122">Property tag of the second property to be compared.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31d9d-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="31d9d-123">Remarks</span></span>

<span data-ttu-id="31d9d-124">A ordem de comparação _é (marca de propriedade 1) (operador relacional) (marca de propriedade 2)._</span><span class="sxs-lookup"><span data-stu-id="31d9d-124">The comparison order is  _(property tag 1) (relational operator) (property tag 2)_.</span></span> <span data-ttu-id="31d9d-125">As propriedades a serem comparadas devem ser do mesmo tipo.</span><span class="sxs-lookup"><span data-stu-id="31d9d-125">The properties to be compared must be of the same type.</span></span> <span data-ttu-id="31d9d-126">A tentativa de comparar propriedades de tipos diferentes faz com que o MAPI ou o provedor de serviços retorne o valor de erro MAPI_E_TOO_COMPLEX do método [IMAPITable](imapitableiunknown.md) para o qual a estrutura é passada como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="31d9d-126">Attempting to compare properties of different types causes MAPI or the service provider to return the error value MAPI_E_TOO_COMPLEX from the [IMAPITable](imapitableiunknown.md) method to which the structure is passed as a parameter.</span></span> 
  
<span data-ttu-id="31d9d-127">O resultado de uma restrição de valor de propriedade de comparação é indefinido quando uma ou ambas as propriedades não existem.</span><span class="sxs-lookup"><span data-stu-id="31d9d-127">The result of a compare property value restriction is undefined when one or both of the properties do not exist.</span></span> <span data-ttu-id="31d9d-128">Quando um cliente exige um comportamento bem definido para essa restrição e não tem certeza se a propriedade existe, (por exemplo, não é uma coluna necessária de uma tabela), ele deve criar uma restrição **AND** para ingressar na restrição de comparação de propriedade com uma restrição existente.</span><span class="sxs-lookup"><span data-stu-id="31d9d-128">When a client requires well-defined behavior for such a restriction and is not sure whether the property exists, (for example, it is not a required column of a table) it should create an **AND** restriction to join the compare property restriction with an exist restriction.</span></span> <span data-ttu-id="31d9d-129">Use uma [estrutura SExistRestriction](sexistrestriction.md) para definir a restrição existente e uma [estrutura SAndRestriction](sandrestriction.md) para definir a **restrição AND.**</span><span class="sxs-lookup"><span data-stu-id="31d9d-129">Use an [SExistRestriction](sexistrestriction.md) structure to define the exist restriction and an [SAndRestriction](sandrestriction.md) structure to define the **AND** restriction.</span></span> 
  
<span data-ttu-id="31d9d-130">As propriedades especificadas nos **membros ulPropTag1** e **ulPropTag2** poderão ter vários valores se o provedor de serviços a suportar.</span><span class="sxs-lookup"><span data-stu-id="31d9d-130">The properties specified in the **ulPropTag1** and **ulPropTag2** members can be multi-valued if the service provider supports it.</span></span> 
  
<span data-ttu-id="31d9d-131">Para obter mais informações sobre a **estrutura SComparePropsRestriction** e restrições em geral, consulte [Sobre restrições.](about-restrictions.md)</span><span class="sxs-lookup"><span data-stu-id="31d9d-131">For more information about the **SComparePropsRestriction** structure and restrictions in general, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="31d9d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="31d9d-132">See also</span></span>

- [<span data-ttu-id="31d9d-133">SBitMaskRestriction</span><span class="sxs-lookup"><span data-stu-id="31d9d-133">SBitMaskRestriction</span></span>](sbitmaskrestriction.md)
- [<span data-ttu-id="31d9d-134">SRestriction</span><span class="sxs-lookup"><span data-stu-id="31d9d-134">SRestriction</span></span>](srestriction.md)
- [<span data-ttu-id="31d9d-135">Estruturas MAPI</span><span class="sxs-lookup"><span data-stu-id="31d9d-135">MAPI Structures</span></span>](mapi-structures.md)

