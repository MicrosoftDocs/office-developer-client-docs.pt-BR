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
ms.openlocfilehash: d214cb5d449e2f7e42e7ee72774fdc146495adb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767791"
---
# <a name="lpropcompareprop"></a><span data-ttu-id="3efc9-103">LPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="3efc9-103">LPropCompareProp</span></span>

  
  
<span data-ttu-id="3efc9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3efc9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3efc9-105">Compara dois valores de propriedade para determinar se eles são iguais.</span><span class="sxs-lookup"><span data-stu-id="3efc9-105">Compares two property values to determine whether they are equal.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3efc9-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3efc9-106">Header file:</span></span>  <br/> |<span data-ttu-id="3efc9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3efc9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3efc9-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="3efc9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3efc9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3efc9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3efc9-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="3efc9-110">Called by:</span></span>  <br/> |<span data-ttu-id="3efc9-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="3efc9-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LONG LPropCompareProp(
  LPSPropValue lpSPropValueA,
  LPSPropValue lpSPropValueB
);
```

## <a name="parameters"></a><span data-ttu-id="3efc9-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3efc9-112">Parameters</span></span>

 <span data-ttu-id="3efc9-113">_lpSPropValueA_</span><span class="sxs-lookup"><span data-stu-id="3efc9-113">_lpSPropValueA_</span></span>
  
> <span data-ttu-id="3efc9-114">[in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo o primeiro valor de propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="3efc9-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value to be compared.</span></span> 
    
 <span data-ttu-id="3efc9-115">_lpSPropValueB_</span><span class="sxs-lookup"><span data-stu-id="3efc9-115">_lpSPropValueB_</span></span>
  
> <span data-ttu-id="3efc9-116">[in] Ponteiro para uma estrutura **SPropValue** definindo o segundo valor da propriedade a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="3efc9-116">[in] Pointer to an **SPropValue** structure defining the second property value to be compared.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3efc9-117">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3efc9-117">Return value</span></span>

 <span data-ttu-id="3efc9-118">**LPropCompareProp** retorna um dos seguintes valores para a maioria dos tipos de propriedade:</span><span class="sxs-lookup"><span data-stu-id="3efc9-118">**LPropCompareProp** returns one of the following values for most property types:</span></span> 
  
- <span data-ttu-id="3efc9-119">Menor do que zero se o valor indicado pelo parâmetro _lpSPropValueA_ é menor do que indicado pelo parâmetro _lpSPropValueB_ .</span><span class="sxs-lookup"><span data-stu-id="3efc9-119">Less than zero if the value indicated by the  _lpSPropValueA_ parameter is less than that indicated by the  _lpSPropValueB_ parameter.</span></span> 
    
- <span data-ttu-id="3efc9-120">Maior do que zero se o valor indicado pelo _lpSPropValueA_ é maior do que indicado pelo _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="3efc9-120">Greater than zero if the value indicated by  _lpSPropValueA_ is greater than that indicated by  _lpSPropValueB_.</span></span>
    
- <span data-ttu-id="3efc9-121">Zero se o valor indicado pelo _lpSPropValueA_ equivale ao valor indicado pelo _lpSPropValueB_.</span><span class="sxs-lookup"><span data-stu-id="3efc9-121">Zero if the value indicated by  _lpSPropValueA_ equals the value indicated by  _lpSPropValueB_.</span></span> 
    
<span data-ttu-id="3efc9-122">Para tipos de propriedade que não tenham nenhuma intrínsecas pedidos, como Boolean ou tipos de erro, a função **LPropCompareProp** retorna um valor indefinido se os dois valores de propriedade não são iguais.</span><span class="sxs-lookup"><span data-stu-id="3efc9-122">For property types that have no intrinsic ordering, such as Boolean or error types, the **LPropCompareProp** function returns an undefined value if the two property values are not equal.</span></span> <span data-ttu-id="3efc9-123">Esse valor indefinido é diferente de zero e consistente em chamadas.</span><span class="sxs-lookup"><span data-stu-id="3efc9-123">This undefined value is nonzero and consistent across calls.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3efc9-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="3efc9-124">Remarks</span></span>

<span data-ttu-id="3efc9-125">Use a função de **LPropCompareProp** somente se os tipos de duas propriedades a serem comparadas são iguais.</span><span class="sxs-lookup"><span data-stu-id="3efc9-125">Use the **LPropCompareProp** function only if the types of the two properties to be compared are the same.</span></span> 
  
<span data-ttu-id="3efc9-126">Antes de chamar **LPropCompareProp**, um aplicativo cliente ou um provedor de serviços deve recuperar as propriedades para comparação com uma chamada ao método [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3efc9-126">Before calling **LPropCompareProp**, a client application or service provider must first retrieve the properties for comparison with a call to the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="3efc9-127">Quando um cliente ou provedor chamadas **LPropCompareProp**, a função examina primeiro as marcas de propriedade para certificar-se de que a comparação dos valores de propriedade é válida.</span><span class="sxs-lookup"><span data-stu-id="3efc9-127">When a client or provider calls **LPropCompareProp**, the function first examines the property tags to make sure that the comparison of property values is valid.</span></span> <span data-ttu-id="3efc9-128">A função compara os valores de propriedade, retornando um valor apropriado.</span><span class="sxs-lookup"><span data-stu-id="3efc9-128">The function then compares the property values, returning an appropriate value.</span></span> 
  
<span data-ttu-id="3efc9-129">Se os valores de propriedade são diferentes, **LPropCompareProp** determina qual é o maior.</span><span class="sxs-lookup"><span data-stu-id="3efc9-129">If the property values are unequal, **LPropCompareProp** determines which one is the greater.</span></span> <span data-ttu-id="3efc9-130">As propriedades que compara **LPropCompareProp** não precisará pertencem ao mesmo objeto.</span><span class="sxs-lookup"><span data-stu-id="3efc9-130">The properties that **LPropCompareProp** compares do not have to belong to the same object.</span></span> 
  

