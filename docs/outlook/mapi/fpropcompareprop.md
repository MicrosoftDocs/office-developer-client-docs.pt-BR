---
title: FPropCompareProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropCompareProp
api_type:
- COM
ms.assetid: 17cb53c4-7154-4a4e-b4ec-de720fa055cb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 69bbed644a8173bf9291ca48a63960f693108318
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766608"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="985c5-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="985c5-103">FPropCompareProp</span></span>

<span data-ttu-id="985c5-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="985c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="985c5-105">Compara dois valores de propriedade usando um operador relacional especificado.</span><span class="sxs-lookup"><span data-stu-id="985c5-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="985c5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="985c5-106">Header file:</span></span>  <br/> |<span data-ttu-id="985c5-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="985c5-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="985c5-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="985c5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="985c5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="985c5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="985c5-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="985c5-110">Called by:</span></span>  <br/> |<span data-ttu-id="985c5-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="985c5-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="985c5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="985c5-112">Parameters</span></span>

<span data-ttu-id="985c5-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="985c5-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="985c5-114">[in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo o valor da propriedade primeiro para comparação.</span><span class="sxs-lookup"><span data-stu-id="985c5-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="985c5-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="985c5-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="985c5-116">[in] O operador relacional a ser usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="985c5-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="985c5-117">Para valores permitidos, consulte a estrutura [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="985c5-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="985c5-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="985c5-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="985c5-119">[in] Ponteiro para uma estrutura **SPropValue** definindo o valor da propriedade segundo para comparação.</span><span class="sxs-lookup"><span data-stu-id="985c5-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="985c5-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="985c5-120">Return value</span></span>

<span data-ttu-id="985c5-121">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="985c5-121">TRUE</span></span> 
  
> <span data-ttu-id="985c5-122">Os valores de propriedade satisfazer o objeto relation especificado.</span><span class="sxs-lookup"><span data-stu-id="985c5-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="985c5-123">FALSO</span><span class="sxs-lookup"><span data-stu-id="985c5-123">FALSE</span></span> 
  
> <span data-ttu-id="985c5-124">Os valores de propriedade não atenderem a relação especificada.</span><span class="sxs-lookup"><span data-stu-id="985c5-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="985c5-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="985c5-125">Remarks</span></span>

<span data-ttu-id="985c5-126">O método de comparação depende os tipos de propriedade especificados nas definições de propriedade [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="985c5-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="985c5-127">As funções **FPropCompareProp** e [FPropContainsProp](fpropcontainsprop.md) podem ser usadas para preparar restrições para gerar uma tabela.</span><span class="sxs-lookup"><span data-stu-id="985c5-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="985c5-128">A ordem de comparação é _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="985c5-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="985c5-129">Se os tipos de propriedade dos valores de propriedade a ser comparada não coincidirem, a função **FPropCompareProp** retorna FALSE.</span><span class="sxs-lookup"><span data-stu-id="985c5-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

