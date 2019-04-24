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
ms.openlocfilehash: 7726811467324242037ec11a69ae0b1b123d7f21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328067"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="6af84-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="6af84-103">FPropCompareProp</span></span>

<span data-ttu-id="6af84-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6af84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6af84-105">Compara dois valores de propriedade usando um operador relacional especificado.</span><span class="sxs-lookup"><span data-stu-id="6af84-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6af84-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="6af84-106">Header file:</span></span>  <br/> |<span data-ttu-id="6af84-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="6af84-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="6af84-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="6af84-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6af84-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6af84-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6af84-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="6af84-110">Called by:</span></span>  <br/> |<span data-ttu-id="6af84-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="6af84-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="6af84-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6af84-112">Parameters</span></span>

<span data-ttu-id="6af84-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="6af84-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="6af84-114">no Ponteiro para uma estrutura [SPropValue](spropvalue.md) que define o valor da primeira propriedade para comparação.</span><span class="sxs-lookup"><span data-stu-id="6af84-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="6af84-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="6af84-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="6af84-116">no O operador relacional a ser usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="6af84-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="6af84-117">Para valores permitidos, consulte a estrutura [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="6af84-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="6af84-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="6af84-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="6af84-119">no Ponteiro para uma estrutura **SPropValue** que define o segundo valor de propriedade para comparação.</span><span class="sxs-lookup"><span data-stu-id="6af84-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6af84-120">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6af84-120">Return value</span></span>

<span data-ttu-id="6af84-121">TRUE</span><span class="sxs-lookup"><span data-stu-id="6af84-121">TRUE</span></span> 
  
> <span data-ttu-id="6af84-122">Os valores de propriedade satisfazem a relação especificada.</span><span class="sxs-lookup"><span data-stu-id="6af84-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="6af84-123">FALSE</span><span class="sxs-lookup"><span data-stu-id="6af84-123">FALSE</span></span> 
  
> <span data-ttu-id="6af84-124">Os valores de propriedade não satisfazem a relação especificada.</span><span class="sxs-lookup"><span data-stu-id="6af84-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6af84-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="6af84-125">Remarks</span></span>

<span data-ttu-id="6af84-126">O método Comparison depende dos tipos de propriedade especificados nas definições da propriedade [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="6af84-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="6af84-127">As funções **FPropCompareProp** e [FPropContainsProp](fpropcontainsprop.md) podem ser usadas para preparar restrições para a geração de uma tabela.</span><span class="sxs-lookup"><span data-stu-id="6af84-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="6af84-128">A ordem de comparação é _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="6af84-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="6af84-129">Se os tipos de propriedade dos valores de propriedade a serem comparados não corresponderem, a função **FPropCompareProp** retornará false.</span><span class="sxs-lookup"><span data-stu-id="6af84-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

