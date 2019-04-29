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
# <a name="lpropcompareprop"></a><span data-ttu-id="78f0f-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="78f0f-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="78f0f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78f0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78f0f-105">Compara dois valores de propriedade para determinar se eles são iguais.</span><span class="sxs-lookup"><span data-stu-id="78f0f-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78f0f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="78f0f-106">Header file:</span></span>  <br/> |<span data-ttu-id="78f0f-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="78f0f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="78f0f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="78f0f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="78f0f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="78f0f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="78f0f-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="78f0f-110">Called by:</span></span>  <br/> |<span data-ttu-id="78f0f-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="78f0f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="78f0f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="78f0f-112">Parameters</span></span>

 <span data-ttu-id="78f0f-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="78f0f-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="78f0f-114">no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define o valor da primeira propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="78f0f-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="78f0f-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="78f0f-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="78f0f-116">no Ponteiro para uma estrutura **SPropValue** que define o segundo valor de propriedade a ser comparado.</span><span class="sxs-lookup"><span data-stu-id="78f0f-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="78f0f-117">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="78f0f-117">Return value</span></span>

 <span data-ttu-id="78f0f-118">**LPropCompareProp** retorna um dos seguintes valores para a maioria dos tipos de propriedade:</span><span class="sxs-lookup"><span data-stu-id="78f0f-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="78f0f-119">Menor que zero se o valor indicado pelo parâmetro _lpSPropValueA_ for menor que o indicado pelo parâmetro _lpSPropValueB_ .</span><span class="sxs-lookup"><span data-stu-id="78f0f-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="78f0f-120">Maior que zero se o valor indicado por _lpSPropValueA_ for maior que o indicado por _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="78f0f-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="78f0f-121">Zero se o valor indicado por _lpSPropValueA_ igual ao valor indicado por _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="78f0f-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="78f0f-122">Para tipos de propriedade que não têm ordenação intrínseca, como tipos Boolean ou de erro, a função **LPropCompareProp** retornará um valor indefinido se os dois valores de propriedade não forem iguais.</span><span class="sxs-lookup"><span data-stu-id="78f0f-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="78f0f-123">Esse valor indefinido é diferente de zero e consiste em chamadas.</span><span class="sxs-lookup"><span data-stu-id="78f0f-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="78f0f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="78f0f-124">Remarks</span></span>

<span data-ttu-id="78f0f-125">Use a função **LPropCompareProp** somente se os tipos das duas propriedades a serem comparadas forem os mesmos.</span><span class="sxs-lookup"><span data-stu-id="78f0f-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="78f0f-126">Antes de chamar **LPropCompareProp**, um aplicativo cliente ou provedor de serviços deve recuperar primeiro as propriedades para comparação com uma chamada para o método [IMAPIProp::](imapiprop-getprops.md) GetProps.</span><span class="sxs-lookup"><span data-stu-id="78f0f-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="78f0f-127">Quando um cliente ou provedor chama **LPropCompareProp**, a função primeiro examina as marcas de propriedade para garantir que a comparação dos valores de propriedade é válida.</span><span class="sxs-lookup"><span data-stu-id="78f0f-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="78f0f-128">A função, em seguida, compara os valores de propriedade, retornando um valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="78f0f-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="78f0f-129">Se os valores da propriedade forem diferentes, **LPropCompareProp** determinará qual deles é maior.</span><span class="sxs-lookup"><span data-stu-id="78f0f-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="78f0f-130">As propriedades que o **LPropCompareProp** compara não precisam pertencer ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="78f0f-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

