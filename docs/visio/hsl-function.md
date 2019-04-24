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
description: Retorna um valor que representa um índice na paleta de cores do documento. Especifica uma cor por seus componentes de matiz, saturação e luminosidade.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329922"
---
# <a name="hsl-function"></a><span data-ttu-id="74513-104">Função HSL</span><span class="sxs-lookup"><span data-stu-id="74513-104">HSL Function</span></span>

<span data-ttu-id="74513-105">Retorna um valor que representa um índice na paleta de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="74513-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="74513-106">Especifica uma cor por seus componentes de matiz, saturação e luminosidade.</span><span class="sxs-lookup"><span data-stu-id="74513-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="74513-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="74513-107">Syntax</span></span>

<span data-ttu-id="74513-108">HSL (\* \* *matiz* \* \*, \* \* *saturação* \* \*, \* \* *luminosidade* \* \*)</span><span class="sxs-lookup"><span data-stu-id="74513-108">HSL(\*\* *hue* \*\*, \*\* *saturation* \*\*, \*\* *luminosity* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="74513-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="74513-109">Parameters</span></span>

|<span data-ttu-id="74513-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="74513-110">**Name**</span></span>|<span data-ttu-id="74513-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="74513-111">**Required/Optional**</span></span>|<span data-ttu-id="74513-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="74513-112">**Data Type**</span></span>|<span data-ttu-id="74513-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="74513-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="74513-114">_Tom_</span><span class="sxs-lookup"><span data-stu-id="74513-114">_hue_</span></span> <br/> |<span data-ttu-id="74513-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="74513-115">Required</span></span>  <br/> |<span data-ttu-id="74513-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="74513-116">**Number**</span></span> <br/> |<span data-ttu-id="74513-117">A matiz da cor, expressa como um número entre 0 e 239, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="74513-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="74513-118">_saturação_</span><span class="sxs-lookup"><span data-stu-id="74513-118">_saturation_</span></span> <br/> |<span data-ttu-id="74513-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="74513-119">Required</span></span>  <br/> |<span data-ttu-id="74513-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="74513-120">**Number**</span></span> <br/> |<span data-ttu-id="74513-121">A saturação da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="74513-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="74513-122">_luminosidade_</span><span class="sxs-lookup"><span data-stu-id="74513-122">_luminosity_</span></span> <br/> |<span data-ttu-id="74513-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="74513-123">Required</span></span>  <br/> |<span data-ttu-id="74513-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="74513-124">**Number**</span></span> <br/> | <span data-ttu-id="74513-125">A luminosidade da cor, expressa como um número entre 0 e 240, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="74513-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="74513-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="74513-126">Return value</span></span>

<span data-ttu-id="74513-127">Número</span><span class="sxs-lookup"><span data-stu-id="74513-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="74513-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="74513-128">Remarks</span></span>

<span data-ttu-id="74513-129">Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à lista de documentos de cores disponíveis.</span><span class="sxs-lookup"><span data-stu-id="74513-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="74513-130">A tabela a seguir relaciona algumas cores padrão e seus valores de matiz, saturação e luminosidade.</span><span class="sxs-lookup"><span data-stu-id="74513-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="74513-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="74513-131">**Color**</span></span>|<span data-ttu-id="74513-132">**Valor de matiz**</span><span class="sxs-lookup"><span data-stu-id="74513-132">**Hue value**</span></span>|<span data-ttu-id="74513-133">**Valor de saturação**</span><span class="sxs-lookup"><span data-stu-id="74513-133">**Saturation value**</span></span>|<span data-ttu-id="74513-134">**Valor de luminosidade**</span><span class="sxs-lookup"><span data-stu-id="74513-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="74513-135">Preto</span><span class="sxs-lookup"><span data-stu-id="74513-135">Black</span></span>  <br/> |<span data-ttu-id="74513-136">,0</span><span class="sxs-lookup"><span data-stu-id="74513-136">0</span></span>  <br/> |<span data-ttu-id="74513-137">,0</span><span class="sxs-lookup"><span data-stu-id="74513-137">0</span></span>  <br/> |<span data-ttu-id="74513-138">dia</span><span class="sxs-lookup"><span data-stu-id="74513-138">24</span></span>  <br/> |
|<span data-ttu-id="74513-139">Azul</span><span class="sxs-lookup"><span data-stu-id="74513-139">Blue</span></span>  <br/> |<span data-ttu-id="74513-140">160</span><span class="sxs-lookup"><span data-stu-id="74513-140">160</span></span>  <br/> |<span data-ttu-id="74513-141">240</span><span class="sxs-lookup"><span data-stu-id="74513-141">240</span></span>  <br/> |<span data-ttu-id="74513-142">120</span><span class="sxs-lookup"><span data-stu-id="74513-142">120</span></span>  <br/> |
|<span data-ttu-id="74513-143">Verde</span><span class="sxs-lookup"><span data-stu-id="74513-143">Green</span></span>  <br/> |<span data-ttu-id="74513-144">80</span><span class="sxs-lookup"><span data-stu-id="74513-144">80</span></span>  <br/> |<span data-ttu-id="74513-145">240</span><span class="sxs-lookup"><span data-stu-id="74513-145">240</span></span>  <br/> |<span data-ttu-id="74513-146">120</span><span class="sxs-lookup"><span data-stu-id="74513-146">120</span></span>  <br/> |
|<span data-ttu-id="74513-147">Ciano</span><span class="sxs-lookup"><span data-stu-id="74513-147">Cyan</span></span>  <br/> |<span data-ttu-id="74513-148">120</span><span class="sxs-lookup"><span data-stu-id="74513-148">120</span></span>  <br/> |<span data-ttu-id="74513-149">240</span><span class="sxs-lookup"><span data-stu-id="74513-149">240</span></span>  <br/> |<span data-ttu-id="74513-150">120</span><span class="sxs-lookup"><span data-stu-id="74513-150">120</span></span>  <br/> |
|<span data-ttu-id="74513-151">Vermelho</span><span class="sxs-lookup"><span data-stu-id="74513-151">Red</span></span>  <br/> |<span data-ttu-id="74513-152">,0</span><span class="sxs-lookup"><span data-stu-id="74513-152">0</span></span>  <br/> |<span data-ttu-id="74513-153">240</span><span class="sxs-lookup"><span data-stu-id="74513-153">240</span></span>  <br/> |<span data-ttu-id="74513-154">120</span><span class="sxs-lookup"><span data-stu-id="74513-154">120</span></span>  <br/> |
|<span data-ttu-id="74513-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="74513-155">Magenta</span></span>  <br/> |<span data-ttu-id="74513-156">200</span><span class="sxs-lookup"><span data-stu-id="74513-156">200</span></span>  <br/> |<span data-ttu-id="74513-157">240</span><span class="sxs-lookup"><span data-stu-id="74513-157">240</span></span>  <br/> |<span data-ttu-id="74513-158">120</span><span class="sxs-lookup"><span data-stu-id="74513-158">120</span></span>  <br/> |
|<span data-ttu-id="74513-159">Amarelo</span><span class="sxs-lookup"><span data-stu-id="74513-159">Yellow</span></span>  <br/> |<span data-ttu-id="74513-160">40</span><span class="sxs-lookup"><span data-stu-id="74513-160">40</span></span>  <br/> |<span data-ttu-id="74513-161">240</span><span class="sxs-lookup"><span data-stu-id="74513-161">240</span></span>  <br/> |<span data-ttu-id="74513-162">120</span><span class="sxs-lookup"><span data-stu-id="74513-162">120</span></span>  <br/> |
|<span data-ttu-id="74513-163">Branco</span><span class="sxs-lookup"><span data-stu-id="74513-163">White</span></span>  <br/> |<span data-ttu-id="74513-164">,0</span><span class="sxs-lookup"><span data-stu-id="74513-164">0</span></span>  <br/> |<span data-ttu-id="74513-165">,0</span><span class="sxs-lookup"><span data-stu-id="74513-165">0</span></span>  <br/> |<span data-ttu-id="74513-166">240</span><span class="sxs-lookup"><span data-stu-id="74513-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="74513-167">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="74513-167">Example 1</span></span>

<span data-ttu-id="74513-168">HSL (160240120)</span><span class="sxs-lookup"><span data-stu-id="74513-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="74513-169">Retornará o índice da cor azul.</span><span class="sxs-lookup"><span data-stu-id="74513-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="74513-170">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="74513-170">Example 2</span></span>

<span data-ttu-id="74513-171">HSL (matiz (FillForegnd), SAT (FillForegnd), mín (LUM (FillForegnd) + 100240))</span><span class="sxs-lookup"><span data-stu-id="74513-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="74513-172">Retornará o índice de uma cor que espelha a cor de preenchimento de primeiro plano com uma luminosidade crescente.</span><span class="sxs-lookup"><span data-stu-id="74513-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

