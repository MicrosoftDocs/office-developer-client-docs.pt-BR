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
description: Retorna um valor representando um índice na paleta de cores do documento. Especifica uma cor por seu matiz, saturação e luminosidade componentes do.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772035"
---
# <a name="hsl-function"></a><span data-ttu-id="25bb0-104">Função HSL</span><span class="sxs-lookup"><span data-stu-id="25bb0-104">HSL Function</span></span>

<span data-ttu-id="25bb0-105">Retorna um valor representando um índice na paleta de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="25bb0-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="25bb0-106">Especifica uma cor por seu matiz, saturação e luminosidade componentes do.</span><span class="sxs-lookup"><span data-stu-id="25bb0-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="25bb0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25bb0-107">Syntax</span></span>

<span data-ttu-id="25bb0-108">HSL (* * *matiz* * *, * * *saturação* * *, * * *luminosidade* * *)</span><span class="sxs-lookup"><span data-stu-id="25bb0-108">HSL(** *hue* **, ** *saturation* **, ** *luminosity* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="25bb0-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25bb0-109">Parameters</span></span>

|<span data-ttu-id="25bb0-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="25bb0-110">**Name**</span></span>|<span data-ttu-id="25bb0-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="25bb0-111">**Required/Optional**</span></span>|<span data-ttu-id="25bb0-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="25bb0-112">**Data Type**</span></span>|<span data-ttu-id="25bb0-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="25bb0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="25bb0-114">_matiz_</span><span class="sxs-lookup"><span data-stu-id="25bb0-114">_hue_</span></span> <br/> |<span data-ttu-id="25bb0-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="25bb0-115">Required</span></span>  <br/> |<span data-ttu-id="25bb0-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="25bb0-116">**Number**</span></span> <br/> |<span data-ttu-id="25bb0-117">A matiz da cor, expressa como um número entre 0 e 239, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="25bb0-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="25bb0-118">_saturação_</span><span class="sxs-lookup"><span data-stu-id="25bb0-118">_saturation_</span></span> <br/> |<span data-ttu-id="25bb0-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="25bb0-119">Required</span></span>  <br/> |<span data-ttu-id="25bb0-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="25bb0-120">**Number**</span></span> <br/> |<span data-ttu-id="25bb0-121">A saturação da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="25bb0-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="25bb0-122">_luminosidade_</span><span class="sxs-lookup"><span data-stu-id="25bb0-122">_luminosity_</span></span> <br/> |<span data-ttu-id="25bb0-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="25bb0-123">Required</span></span>  <br/> |<span data-ttu-id="25bb0-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="25bb0-124">**Number**</span></span> <br/> | <span data-ttu-id="25bb0-125">A luminosidade da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="25bb0-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="25bb0-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="25bb0-126">Return value</span></span>

<span data-ttu-id="25bb0-127">Number</span><span class="sxs-lookup"><span data-stu-id="25bb0-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="25bb0-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="25bb0-128">Remarks</span></span>

<span data-ttu-id="25bb0-129">Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à lista de documentos de cores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="25bb0-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="25bb0-130">A tabela a seguir relaciona algumas cores padrão e seus valores de matiz, saturação e luminosidade.</span><span class="sxs-lookup"><span data-stu-id="25bb0-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="25bb0-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="25bb0-131">**Color**</span></span>|<span data-ttu-id="25bb0-132">**Valor de matiz**</span><span class="sxs-lookup"><span data-stu-id="25bb0-132">**Hue value**</span></span>|<span data-ttu-id="25bb0-133">**Valor de saturação**</span><span class="sxs-lookup"><span data-stu-id="25bb0-133">**Saturation value**</span></span>|<span data-ttu-id="25bb0-134">**Valor de luminosidade**</span><span class="sxs-lookup"><span data-stu-id="25bb0-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="25bb0-135">Preto</span><span class="sxs-lookup"><span data-stu-id="25bb0-135">Black</span></span>  <br/> |<span data-ttu-id="25bb0-136">0</span><span class="sxs-lookup"><span data-stu-id="25bb0-136">0</span></span>  <br/> |<span data-ttu-id="25bb0-137">0</span><span class="sxs-lookup"><span data-stu-id="25bb0-137">0</span></span>  <br/> |<span data-ttu-id="25bb0-138">24</span><span class="sxs-lookup"><span data-stu-id="25bb0-138">24</span></span>  <br/> |
|<span data-ttu-id="25bb0-139">Azul</span><span class="sxs-lookup"><span data-stu-id="25bb0-139">Blue</span></span>  <br/> |<span data-ttu-id="25bb0-140">160</span><span class="sxs-lookup"><span data-stu-id="25bb0-140">160</span></span>  <br/> |<span data-ttu-id="25bb0-141">240</span><span class="sxs-lookup"><span data-stu-id="25bb0-141">240</span></span>  <br/> |<span data-ttu-id="25bb0-142">120</span><span class="sxs-lookup"><span data-stu-id="25bb0-142">120</span></span>  <br/> |
|<span data-ttu-id="25bb0-143">Verde</span><span class="sxs-lookup"><span data-stu-id="25bb0-143">Green</span></span>  <br/> |<span data-ttu-id="25bb0-144">80</span><span class="sxs-lookup"><span data-stu-id="25bb0-144">80</span></span>  <br/> |<span data-ttu-id="25bb0-145">240</span><span class="sxs-lookup"><span data-stu-id="25bb0-145">240</span></span>  <br/> |<span data-ttu-id="25bb0-146">120</span><span class="sxs-lookup"><span data-stu-id="25bb0-146">120</span></span>  <br/> |
|<span data-ttu-id="25bb0-147">Ciano</span><span class="sxs-lookup"><span data-stu-id="25bb0-147">Cyan</span></span>  <br/> |<span data-ttu-id="25bb0-148">120</span><span class="sxs-lookup"><span data-stu-id="25bb0-148">120</span></span>  <br/> |<span data-ttu-id="25bb0-149">240</span><span class="sxs-lookup"><span data-stu-id="25bb0-149">240</span></span>  <br/> |<span data-ttu-id="25bb0-150">120</span><span class="sxs-lookup"><span data-stu-id="25bb0-150">120</span></span>  <br/> |
|<span data-ttu-id="25bb0-151">Vermelho</span><span class="sxs-lookup"><span data-stu-id="25bb0-151">Red</span></span>  <br/> |<span data-ttu-id="25bb0-152">0</span><span class="sxs-lookup"><span data-stu-id="25bb0-152">0</span></span>  <br/> |<span data-ttu-id="25bb0-153">240</span><span class="sxs-lookup"><span data-stu-id="25bb0-153">240</span></span>  <br/> |<span data-ttu-id="25bb0-154">120</span><span class="sxs-lookup"><span data-stu-id="25bb0-154">120</span></span>  <br/> |
|<span data-ttu-id="25bb0-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="25bb0-155">Magenta</span></span>  <br/> |<span data-ttu-id="25bb0-156">200</span><span class="sxs-lookup"><span data-stu-id="25bb0-156">200</span></span>  <br/> |<span data-ttu-id="25bb0-157">240</span><span class="sxs-lookup"><span data-stu-id="25bb0-157">240</span></span>  <br/> |<span data-ttu-id="25bb0-158">120</span><span class="sxs-lookup"><span data-stu-id="25bb0-158">120</span></span>  <br/> |
|<span data-ttu-id="25bb0-159">Amarelo</span><span class="sxs-lookup"><span data-stu-id="25bb0-159">Yellow</span></span>  <br/> |<span data-ttu-id="25bb0-160">40</span><span class="sxs-lookup"><span data-stu-id="25bb0-160">40</span></span>  <br/> |<span data-ttu-id="25bb0-161">240</span><span class="sxs-lookup"><span data-stu-id="25bb0-161">240</span></span>  <br/> |<span data-ttu-id="25bb0-162">120</span><span class="sxs-lookup"><span data-stu-id="25bb0-162">120</span></span>  <br/> |
|<span data-ttu-id="25bb0-163">Branco</span><span class="sxs-lookup"><span data-stu-id="25bb0-163">White</span></span>  <br/> |<span data-ttu-id="25bb0-164">0</span><span class="sxs-lookup"><span data-stu-id="25bb0-164">0</span></span>  <br/> |<span data-ttu-id="25bb0-165">0</span><span class="sxs-lookup"><span data-stu-id="25bb0-165">0</span></span>  <br/> |<span data-ttu-id="25bb0-166">240</span><span class="sxs-lookup"><span data-stu-id="25bb0-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="25bb0-167">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="25bb0-167">Example 1</span></span>

<span data-ttu-id="25bb0-168">HSL(160,240,120)</span><span class="sxs-lookup"><span data-stu-id="25bb0-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="25bb0-169">Retornará o índice da cor azul.</span><span class="sxs-lookup"><span data-stu-id="25bb0-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="25bb0-170">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="25bb0-170">Example 2</span></span>

<span data-ttu-id="25bb0-171">HSL(Hue(FillForegnd),Sat(FillForegnd),min(Lum(FillForegnd)+100,240))</span><span class="sxs-lookup"><span data-stu-id="25bb0-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="25bb0-172">Retornará o índice de uma cor que espelha a cor de preenchimento de primeiro plano com uma luminosidade crescente.</span><span class="sxs-lookup"><span data-stu-id="25bb0-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

