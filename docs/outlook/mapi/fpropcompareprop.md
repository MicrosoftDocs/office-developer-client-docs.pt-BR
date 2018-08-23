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
ms.openlocfilehash: adccbaf65adec2c517c4890f722198e8262092cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564602"
---
# <a name="fpropcompareprop"></a><span data-ttu-id="7cb69-103">FPropCompareProp</span><span class="sxs-lookup"><span data-stu-id="7cb69-103">FPropCompareProp</span></span>

<span data-ttu-id="7cb69-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7cb69-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7cb69-105">Compara dois valores de propriedade usando um operador relacional especificado.</span><span class="sxs-lookup"><span data-stu-id="7cb69-105">Compares two property values using a specified relational operator.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7cb69-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7cb69-106">Header file:</span></span>  <br/> |<span data-ttu-id="7cb69-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7cb69-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7cb69-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="7cb69-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7cb69-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7cb69-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7cb69-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="7cb69-110">Called by:</span></span>  <br/> |<span data-ttu-id="7cb69-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="7cb69-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
BOOL FPropCompareProp(
  LPSPropValue lpSPropValue1,
  ULONG ulRelOp,
  LPSPropValue lpSPropValue2
);
```

## <a name="parameters"></a><span data-ttu-id="7cb69-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cb69-112">Parameters</span></span>

<span data-ttu-id="7cb69-113">_lpSPropValue1_</span><span class="sxs-lookup"><span data-stu-id="7cb69-113">_lpSPropValue1_</span></span>
  
> <span data-ttu-id="7cb69-114">[in] Ponteiro para uma estrutura [SPropValue](spropvalue.md) definindo o valor da propriedade primeiro para comparação.</span><span class="sxs-lookup"><span data-stu-id="7cb69-114">[in] Pointer to an [SPropValue](spropvalue.md) structure defining the first property value for comparison.</span></span> 
    
<span data-ttu-id="7cb69-115">_ulRelOp_</span><span class="sxs-lookup"><span data-stu-id="7cb69-115">_ulRelOp_</span></span>
  
> <span data-ttu-id="7cb69-116">[in] O operador relacional a ser usado na comparação.</span><span class="sxs-lookup"><span data-stu-id="7cb69-116">[in] The relational operator to use in the comparison.</span></span> <span data-ttu-id="7cb69-117">Para valores permitidos, consulte a estrutura [SComparePropsRestriction](scomparepropsrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="7cb69-117">For allowable values, see the [SComparePropsRestriction](scomparepropsrestriction.md) structure.</span></span> 
    
<span data-ttu-id="7cb69-118">_lpSPropValue2_</span><span class="sxs-lookup"><span data-stu-id="7cb69-118">_lpSPropValue2_</span></span>
  
> <span data-ttu-id="7cb69-119">[in] Ponteiro para uma estrutura **SPropValue** definindo o valor da propriedade segundo para comparação.</span><span class="sxs-lookup"><span data-stu-id="7cb69-119">[in] Pointer to an **SPropValue** structure defining the second property value for comparison.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7cb69-120">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7cb69-120">Return value</span></span>

<span data-ttu-id="7cb69-121">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="7cb69-121">TRUE</span></span> 
  
> <span data-ttu-id="7cb69-122">Os valores de propriedade satisfazer o objeto relation especificado.</span><span class="sxs-lookup"><span data-stu-id="7cb69-122">The property values satisfy the specified relation.</span></span> 
    
<span data-ttu-id="7cb69-123">FALSO</span><span class="sxs-lookup"><span data-stu-id="7cb69-123">FALSE</span></span> 
  
> <span data-ttu-id="7cb69-124">Os valores de propriedade não atenderem a relação especificada.</span><span class="sxs-lookup"><span data-stu-id="7cb69-124">The property values do not satisfy the specified relation.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7cb69-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cb69-125">Remarks</span></span>

<span data-ttu-id="7cb69-126">O método de comparação depende os tipos de propriedade especificados nas definições de propriedade [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="7cb69-126">The comparison method depends on the property types specified in the [SPropValue](spropvalue.md) property definitions.</span></span> <span data-ttu-id="7cb69-127">As funções **FPropCompareProp** e [FPropContainsProp](fpropcontainsprop.md) podem ser usadas para preparar restrições para gerar uma tabela.</span><span class="sxs-lookup"><span data-stu-id="7cb69-127">The **FPropCompareProp** and [FPropContainsProp](fpropcontainsprop.md) functions can be used to prepare restrictions for generating a table.</span></span> 
  
<span data-ttu-id="7cb69-128">A ordem de comparação é _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span><span class="sxs-lookup"><span data-stu-id="7cb69-128">The order of comparison is  _lpSPropValue1_, _ ulRelOp _, _ lpSPropValue2 _.</span></span> <span data-ttu-id="7cb69-129">Se os tipos de propriedade dos valores de propriedade a ser comparada não coincidirem, a função **FPropCompareProp** retorna FALSE.</span><span class="sxs-lookup"><span data-stu-id="7cb69-129">If the property types of the property values to be compared do not match, the **FPropCompareProp** function returns FALSE.</span></span> 
  

