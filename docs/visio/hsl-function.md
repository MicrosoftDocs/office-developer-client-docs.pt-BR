---
title: Função HSL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Retorna um valor que representa um índice na paleta de cores do documento. Ele especifica uma cor por seus componentes de matiz, saturação e luminosidade.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420959"
---
# <a name="hsl-function"></a><span data-ttu-id="c39b1-104">Função HSL</span><span class="sxs-lookup"><span data-stu-id="c39b1-104">HSL Function</span></span>

<span data-ttu-id="c39b1-105">Retorna um valor que representa um índice na paleta de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="c39b1-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="c39b1-106">Ele especifica uma cor por seus componentes de matiz, saturação e luminosidade.</span><span class="sxs-lookup"><span data-stu-id="c39b1-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c39b1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c39b1-107">Syntax</span></span>

<span data-ttu-id="c39b1-108">HSL(\*\* *matiz* \*\*, \*\* *saturação* \*\*, \*\* *luminosidade* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c39b1-108">HSL(\*\* *hue* \*\*, \*\* *saturation* \*\*, \*\* *luminosity* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c39b1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c39b1-109">Parameters</span></span>

|<span data-ttu-id="c39b1-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c39b1-110">**Name**</span></span>|<span data-ttu-id="c39b1-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="c39b1-111">**Required/Optional**</span></span>|<span data-ttu-id="c39b1-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c39b1-112">**Data Type**</span></span>|<span data-ttu-id="c39b1-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c39b1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c39b1-114">_hue_</span><span class="sxs-lookup"><span data-stu-id="c39b1-114">_hue_</span></span> <br/> |<span data-ttu-id="c39b1-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c39b1-115">Required</span></span>  <br/> |<span data-ttu-id="c39b1-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="c39b1-116">**Number**</span></span> <br/> |<span data-ttu-id="c39b1-117">A matiz da cor, expressa como um número entre 0 e 239, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="c39b1-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="c39b1-118">_saturação_</span><span class="sxs-lookup"><span data-stu-id="c39b1-118">_saturation_</span></span> <br/> |<span data-ttu-id="c39b1-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c39b1-119">Required</span></span>  <br/> |<span data-ttu-id="c39b1-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="c39b1-120">**Number**</span></span> <br/> |<span data-ttu-id="c39b1-121">A saturação da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="c39b1-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="c39b1-122">_luminosidade_</span><span class="sxs-lookup"><span data-stu-id="c39b1-122">_luminosity_</span></span> <br/> |<span data-ttu-id="c39b1-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c39b1-123">Required</span></span>  <br/> |<span data-ttu-id="c39b1-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="c39b1-124">**Number**</span></span> <br/> | <span data-ttu-id="c39b1-125">A luminosidade da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="c39b1-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c39b1-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c39b1-126">Return value</span></span>

<span data-ttu-id="c39b1-127">Número</span><span class="sxs-lookup"><span data-stu-id="c39b1-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c39b1-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c39b1-128">Remarks</span></span>

<span data-ttu-id="c39b1-129">Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à lista de documentos de cores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="c39b1-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="c39b1-130">A tabela a seguir relaciona algumas cores padrão e seus valores de matiz, saturação e luminosidade.</span><span class="sxs-lookup"><span data-stu-id="c39b1-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="c39b1-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="c39b1-131">**Color**</span></span>|<span data-ttu-id="c39b1-132">**Valor de matiz**</span><span class="sxs-lookup"><span data-stu-id="c39b1-132">**Hue value**</span></span>|<span data-ttu-id="c39b1-133">**Valor de saturação**</span><span class="sxs-lookup"><span data-stu-id="c39b1-133">**Saturation value**</span></span>|<span data-ttu-id="c39b1-134">**Valor de luminosidade**</span><span class="sxs-lookup"><span data-stu-id="c39b1-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="c39b1-135">Preto</span><span class="sxs-lookup"><span data-stu-id="c39b1-135">Black</span></span>  <br/> |<span data-ttu-id="c39b1-136">0</span><span class="sxs-lookup"><span data-stu-id="c39b1-136">0</span></span>  <br/> |<span data-ttu-id="c39b1-137">0</span><span class="sxs-lookup"><span data-stu-id="c39b1-137">0</span></span>  <br/> |<span data-ttu-id="c39b1-138">24</span><span class="sxs-lookup"><span data-stu-id="c39b1-138">24</span></span>  <br/> |
|<span data-ttu-id="c39b1-139">Azul</span><span class="sxs-lookup"><span data-stu-id="c39b1-139">Blue</span></span>  <br/> |<span data-ttu-id="c39b1-140">160</span><span class="sxs-lookup"><span data-stu-id="c39b1-140">160</span></span>  <br/> |<span data-ttu-id="c39b1-141">240</span><span class="sxs-lookup"><span data-stu-id="c39b1-141">240</span></span>  <br/> |<span data-ttu-id="c39b1-142">120</span><span class="sxs-lookup"><span data-stu-id="c39b1-142">120</span></span>  <br/> |
|<span data-ttu-id="c39b1-143">Verde</span><span class="sxs-lookup"><span data-stu-id="c39b1-143">Green</span></span>  <br/> |<span data-ttu-id="c39b1-144">80</span><span class="sxs-lookup"><span data-stu-id="c39b1-144">80</span></span>  <br/> |<span data-ttu-id="c39b1-145">240</span><span class="sxs-lookup"><span data-stu-id="c39b1-145">240</span></span>  <br/> |<span data-ttu-id="c39b1-146">120</span><span class="sxs-lookup"><span data-stu-id="c39b1-146">120</span></span>  <br/> |
|<span data-ttu-id="c39b1-147">Ciano</span><span class="sxs-lookup"><span data-stu-id="c39b1-147">Cyan</span></span>  <br/> |<span data-ttu-id="c39b1-148">120</span><span class="sxs-lookup"><span data-stu-id="c39b1-148">120</span></span>  <br/> |<span data-ttu-id="c39b1-149">240</span><span class="sxs-lookup"><span data-stu-id="c39b1-149">240</span></span>  <br/> |<span data-ttu-id="c39b1-150">120</span><span class="sxs-lookup"><span data-stu-id="c39b1-150">120</span></span>  <br/> |
|<span data-ttu-id="c39b1-151">Vermelho</span><span class="sxs-lookup"><span data-stu-id="c39b1-151">Red</span></span>  <br/> |<span data-ttu-id="c39b1-152">0</span><span class="sxs-lookup"><span data-stu-id="c39b1-152">0</span></span>  <br/> |<span data-ttu-id="c39b1-153">240</span><span class="sxs-lookup"><span data-stu-id="c39b1-153">240</span></span>  <br/> |<span data-ttu-id="c39b1-154">120</span><span class="sxs-lookup"><span data-stu-id="c39b1-154">120</span></span>  <br/> |
|<span data-ttu-id="c39b1-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="c39b1-155">Magenta</span></span>  <br/> |<span data-ttu-id="c39b1-156">200</span><span class="sxs-lookup"><span data-stu-id="c39b1-156">200</span></span>  <br/> |<span data-ttu-id="c39b1-157">240</span><span class="sxs-lookup"><span data-stu-id="c39b1-157">240</span></span>  <br/> |<span data-ttu-id="c39b1-158">120</span><span class="sxs-lookup"><span data-stu-id="c39b1-158">120</span></span>  <br/> |
|<span data-ttu-id="c39b1-159">Amarelo</span><span class="sxs-lookup"><span data-stu-id="c39b1-159">Yellow</span></span>  <br/> |<span data-ttu-id="c39b1-160">40</span><span class="sxs-lookup"><span data-stu-id="c39b1-160">40</span></span>  <br/> |<span data-ttu-id="c39b1-161">240</span><span class="sxs-lookup"><span data-stu-id="c39b1-161">240</span></span>  <br/> |<span data-ttu-id="c39b1-162">120</span><span class="sxs-lookup"><span data-stu-id="c39b1-162">120</span></span>  <br/> |
|<span data-ttu-id="c39b1-163">Branco</span><span class="sxs-lookup"><span data-stu-id="c39b1-163">White</span></span>  <br/> |<span data-ttu-id="c39b1-164">0</span><span class="sxs-lookup"><span data-stu-id="c39b1-164">0</span></span>  <br/> |<span data-ttu-id="c39b1-165">0</span><span class="sxs-lookup"><span data-stu-id="c39b1-165">0</span></span>  <br/> |<span data-ttu-id="c39b1-166">240</span><span class="sxs-lookup"><span data-stu-id="c39b1-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="c39b1-167">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c39b1-167">Example 1</span></span>

<span data-ttu-id="c39b1-168">HSL(160.240.120)</span><span class="sxs-lookup"><span data-stu-id="c39b1-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="c39b1-169">Retornará o índice da cor azul.</span><span class="sxs-lookup"><span data-stu-id="c39b1-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c39b1-170">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c39b1-170">Example 2</span></span>

<span data-ttu-id="c39b1-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span><span class="sxs-lookup"><span data-stu-id="c39b1-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="c39b1-172">Retornará o índice de uma cor que espelha a cor de preenchimento de primeiro plano com uma luminosidade crescente.</span><span class="sxs-lookup"><span data-stu-id="c39b1-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

