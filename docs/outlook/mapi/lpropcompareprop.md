---
title: LPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPropCompareProp
api_type:
- COM
ms.assetid: f14ad568-fe45-4875-957d-415d39dc6f28
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7417ddeb814cafb954d5ab80a6dae771fd0f7a79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414610"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="44837-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="44837-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="44837-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44837-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44837-105">Compara dois valores de propriedade para determinar se eles são iguais.</span><span class="sxs-lookup"><span data-stu-id="44837-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44837-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="44837-106">Header file:</span></span>  <br/> |<span data-ttu-id="44837-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="44837-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="44837-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="44837-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="44837-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="44837-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="44837-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="44837-110">Called by:</span></span>  <br/> |<span data-ttu-id="44837-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="44837-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="44837-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44837-112">Parameters</span></span>

 <span data-ttu-id="44837-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="44837-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="44837-114">[in] Ponteiro para uma [estrutura SPropValue](spropvalue.md) definindo o primeiro valor de propriedade a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="44837-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="44837-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="44837-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="44837-116">[in] Ponteiro para uma **estrutura SPropValue** definindo o segundo valor de propriedade a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="44837-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="44837-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="44837-117">Return value</span></span>

 <span data-ttu-id="44837-118">**LPropCompareProp** retorna um dos seguintes valores para a maioria dos tipos de propriedade:</span><span class="sxs-lookup"><span data-stu-id="44837-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="44837-119">Menor que zero se o valor indicado pelo parâmetro _lpSPropValueA_ for menor que o indicado pelo parâmetro _lpSPropValueB._</span><span class="sxs-lookup"><span data-stu-id="44837-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="44837-120">Maior que zero se o valor indicado por  _lpSPropValueA_ for maior do que o indicado por  _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="44837-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="44837-121">Zero se o valor indicado por  _lpSPropValueA_ for igual ao valor indicado por  _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="44837-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="44837-122">Para tipos de propriedade que não tenham ordenação intrínseca, como booleano ou tipos de erro, a função **LPropCompareProp** retornará um valor indefinido se os dois valores de propriedade não são iguais.</span><span class="sxs-lookup"><span data-stu-id="44837-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="44837-123">Esse valor indefinido não é zero e é consistente entre chamadas.</span><span class="sxs-lookup"><span data-stu-id="44837-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="44837-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="44837-124">Remarks</span></span>

<span data-ttu-id="44837-125">Use a **função LPropCompareProp** somente se os tipos das duas propriedades a serem comparadas são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="44837-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="44837-126">Antes de **chamar LPropCompareProp**, um aplicativo cliente ou provedor de serviços deve primeiro recuperar as propriedades para comparação com uma chamada para o método [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="44837-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="44837-127">Quando um cliente ou provedor chama **LPropCompareProp**, a função primeiro examina as marcas de propriedade para garantir que a comparação de valores de propriedade é válida.</span><span class="sxs-lookup"><span data-stu-id="44837-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="44837-128">Em seguida, a função compara os valores da propriedade, retornando um valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="44837-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="44837-129">Se os valores da propriedade são desapropriedade, **LPropCompareProp** determina qual deles é o maior.</span><span class="sxs-lookup"><span data-stu-id="44837-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="44837-130">As propriedades comparadas **por LPropCompareProp** não devem pertencer ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="44837-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

