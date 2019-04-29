---
title: Função BOUND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60099
localization_priority: Normal
ms.assetid: 36374d78-1028-bd7f-6282-66555ee31306
description: Restringe o valor de uma célula a um intervalo ou série de intervalos.
ms.openlocfilehash: 85fbe66d4e458ac4e42c9eb3c65b9a3a1d8211df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425957"
---
# <a name="bound-function"></a><span data-ttu-id="33fde-103">Função BOUND</span><span class="sxs-lookup"><span data-stu-id="33fde-103">BOUND Function</span></span>

<span data-ttu-id="33fde-104">Restringe o valor de uma célula a um intervalo ou série de intervalos.</span><span class="sxs-lookup"><span data-stu-id="33fde-104">Constrains the value of a cell to a range or set of ranges.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="33fde-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33fde-105">Syntax</span></span>

<span data-ttu-id="33fde-106">BOUND (\* \* *Value* \* \*, \* \* *Type* \* \*, \* \* *ignore* \* \*, \* \* *value1* \* \*, \* \* *value2* \* \* \* \* \* [, ignorar (n), value1 (n), value2 (n),...] \* \* \*)</span><span class="sxs-lookup"><span data-stu-id="33fde-106">BOUND (\*\* *value* \*\*, \*\* *type* \*\*, \*\* *ignore* \*\*, \*\* *value1* \*\*, \*\* *value2* \*\* \*\* \* [,ignore(n), value1(n), value2(n),...] \* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="33fde-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33fde-107">Parameters</span></span>

|<span data-ttu-id="33fde-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="33fde-108">**Name**</span></span>|<span data-ttu-id="33fde-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="33fde-109">**Required/Optional**</span></span>|<span data-ttu-id="33fde-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="33fde-110">**Data Type**</span></span>|<span data-ttu-id="33fde-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="33fde-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="33fde-112">_value_</span><span class="sxs-lookup"><span data-stu-id="33fde-112">_value_</span></span> <br/> |<span data-ttu-id="33fde-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33fde-113">Required</span></span>  <br/> |<span data-ttu-id="33fde-114">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="33fde-114">**Numeric**</span></span> <br/> |<span data-ttu-id="33fde-115">O valor que está sendo restringido no momento.</span><span class="sxs-lookup"><span data-stu-id="33fde-115">The current value being constrained.</span></span>  <br/> |
| <span data-ttu-id="33fde-116">_type_</span><span class="sxs-lookup"><span data-stu-id="33fde-116">_type_</span></span> <br/> |<span data-ttu-id="33fde-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33fde-117">Required</span></span>  <br/> |<span data-ttu-id="33fde-118">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="33fde-118">**Numeric**</span></span> <br/> |<span data-ttu-id="33fde-119">Se a restrição é inclusive (0), exclusive (1) ou desativada (2).</span><span class="sxs-lookup"><span data-stu-id="33fde-119">Whether the constraint is inclusive (0), exclusive (1), or disabled (2).</span></span>  <br/> |
| <span data-ttu-id="33fde-120">_ignora_</span><span class="sxs-lookup"><span data-stu-id="33fde-120">_ignore_</span></span> <br/> |<span data-ttu-id="33fde-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33fde-121">Required</span></span>  <br/> |<span data-ttu-id="33fde-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="33fde-122">**Boolean**</span></span> <br/> | <span data-ttu-id="33fde-123">TRUE para ignorar o intervalo; FALSE para restringir o valor da célula ao intervalo.</span><span class="sxs-lookup"><span data-stu-id="33fde-123">TRUE to ignore the range; FALSE to constrain the value of the cell to the range.</span></span>  <br/> |
| <span data-ttu-id="33fde-124">_valor1_</span><span class="sxs-lookup"><span data-stu-id="33fde-124">_value1_</span></span> <br/> |<span data-ttu-id="33fde-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33fde-125">Required</span></span>  <br/> |<span data-ttu-id="33fde-126">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="33fde-126">**Numeric**</span></span> <br/> |<span data-ttu-id="33fde-127">O primeiro valor de um intervalo.</span><span class="sxs-lookup"><span data-stu-id="33fde-127">First value in a range.</span></span>  <br/> |
| <span data-ttu-id="33fde-128">_value2_</span><span class="sxs-lookup"><span data-stu-id="33fde-128">_value2_</span></span> <br/> |<span data-ttu-id="33fde-129">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="33fde-129">Required</span></span>  <br/> |<span data-ttu-id="33fde-130">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="33fde-130">**Numeric**</span></span> <br/> |<span data-ttu-id="33fde-131">O segundo valor de um intervalo.</span><span class="sxs-lookup"><span data-stu-id="33fde-131">Second value in a range.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33fde-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="33fde-132">Remarks</span></span>

<span data-ttu-id="33fde-133">Use a função BOUND para restringir o valor de uma célula a um limite superior ou inferior; por exemplo, para controlar objetos que não devem ser estendidos acima ou abaixo de uma altura mínima ou máxima.</span><span class="sxs-lookup"><span data-stu-id="33fde-133">Use the BOUND function to restrict a cell's value to an upper and lower bound, for example, to control objects that should not be stretched above or below a minimum or maximum height.</span></span> <span data-ttu-id="33fde-134">A restrição pode incluir ou excluir o intervalo ou intervalos.</span><span class="sxs-lookup"><span data-stu-id="33fde-134">The constraint can be inclusive or exclusive with respect to the range or ranges.</span></span> <span data-ttu-id="33fde-135">Se o valor atual não deve ser restrito, defina o parâmetro _Type_ como 2 (Disabled).</span><span class="sxs-lookup"><span data-stu-id="33fde-135">If the current value should not be constrained, set the  _type_ parameter to 2 (disabled).</span></span> 
  
<span data-ttu-id="33fde-136">Você pode definir vários intervalos fornecendo várias ocorrências dos parâmetros _ignore_, _value1_e _value2_ .</span><span class="sxs-lookup"><span data-stu-id="33fde-136">You can define multiple ranges by supplying multiple occurrences of the  _ignore_,  _value1_, and  _value2_ parameters.</span></span> <span data-ttu-id="33fde-137">Use o parâmetro _ignore_ para desabilitar as restrições por um intervalo específico.</span><span class="sxs-lookup"><span data-stu-id="33fde-137">Use the  _ignore_ parameter to disable constraints by a particular range.</span></span> 
  
<span data-ttu-id="33fde-138">A fórmula contendo a função BOUND não é substituída quando seu valor é alterado; em vez disso, a fórmula é preservada e o novo valor é colocado no parâmetro _Value_ .</span><span class="sxs-lookup"><span data-stu-id="33fde-138">The formula containing the BOUND function does not get overwritten when its value changes; instead, the formula is preserved and the new value is placed into the  _value_ parameter.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="33fde-139">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="33fde-139">Example 1</span></span>

<span data-ttu-id="33fde-140">Este exemplo utiliza a função BOUND para forçar uma alça de controle a ficar dentro da caixa de limite de uma forma.</span><span class="sxs-lookup"><span data-stu-id="33fde-140">This example uses the BOUND function to force a control handle to stay within the bounding box of a shape.</span></span> 
  
<span data-ttu-id="33fde-141">Controls. X1 = BOUND (largura\*0,5, 0, falso, largura\*0, largura\*1)</span><span class="sxs-lookup"><span data-stu-id="33fde-141">Controls.X1 = BOUND(Width\*0.5, 0, FALSE, Width\*0, Width\*1)</span></span>
  
<span data-ttu-id="33fde-142">Controls. Y1 = BOUND (altura\*0,5, 0, falso, altura\*0, altura\*1)</span><span class="sxs-lookup"><span data-stu-id="33fde-142">Controls.Y1 = BOUND(Height\*0.5, 0, FALSE, Height\*0, Height\*1)</span></span>
  
## <a name="example-2"></a><span data-ttu-id="33fde-143">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="33fde-143">Example 2</span></span>

<span data-ttu-id="33fde-144">Este exemplo utiliza a função BOUND para restringir a largura de uma forma a 2 polegadas, 4 polegadas ou 6 polegadas.</span><span class="sxs-lookup"><span data-stu-id="33fde-144">This example uses the BOUND function to constrain a shape's width to 2 inches, 4 inches, or 6 inches.</span></span> 
  
<span data-ttu-id="33fde-145">Width = BOUND(, 0, FALSO, 2 pol, 2 pol, FALSO, 4 pol, 4 pol, FALSO, 6 pol, 6 pol)</span><span class="sxs-lookup"><span data-stu-id="33fde-145">Width = BOUND(, 0, FALSE, 2 in, 2 in, FALSE, 4 in, 4 in, FALSE, 6 in, 6 in)</span></span>
  

