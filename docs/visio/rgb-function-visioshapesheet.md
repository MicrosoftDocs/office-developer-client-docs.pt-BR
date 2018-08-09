---
title: Função RGB (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Retorna um valor representando um índice na paleta de cores do documento. Especifica uma cor por seus componentes vermelhos, verdes e azuis, onde cada uma é um número no intervalo de 0 a 255, inclusive, ou uma expressão que é avaliada neste número.
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772725"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="8043c-104">Função RGB (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="8043c-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="8043c-105">Retorna um valor representando um índice na paleta de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="8043c-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="8043c-106">Especifica uma cor por seus componentes vermelhos, verdes e azuis, onde cada uma é um número no intervalo de 0 a 255, inclusive, ou uma expressão que é avaliada neste número.</span><span class="sxs-lookup"><span data-stu-id="8043c-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8043c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8043c-107">Syntax</span></span>

<span data-ttu-id="8043c-108">RGB (* * *vermelho* * *, * * *verde* * *, * * *azul* * *)</span><span class="sxs-lookup"><span data-stu-id="8043c-108">RGB(** *red* **, ** *green* **, ** *blue* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8043c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8043c-109">Parameters</span></span>

|<span data-ttu-id="8043c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="8043c-110">**Name**</span></span>|<span data-ttu-id="8043c-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="8043c-111">**Required/Optional**</span></span>|<span data-ttu-id="8043c-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="8043c-112">**Data Type**</span></span>|<span data-ttu-id="8043c-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8043c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8043c-114">_vermelho_</span><span class="sxs-lookup"><span data-stu-id="8043c-114">_red_</span></span> <br/> |<span data-ttu-id="8043c-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8043c-115">Required</span></span>  <br/> |<span data-ttu-id="8043c-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="8043c-116">**Number**</span></span> <br/> |<span data-ttu-id="8043c-117">O componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="8043c-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="8043c-118">_verde_</span><span class="sxs-lookup"><span data-stu-id="8043c-118">_green_</span></span> <br/> |<span data-ttu-id="8043c-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8043c-119">Required</span></span>  <br/> |<span data-ttu-id="8043c-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="8043c-120">**Number**</span></span> <br/> |<span data-ttu-id="8043c-121">O componente verde.</span><span class="sxs-lookup"><span data-stu-id="8043c-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="8043c-122">_azul_</span><span class="sxs-lookup"><span data-stu-id="8043c-122">_blue_</span></span> <br/> |<span data-ttu-id="8043c-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="8043c-123">Required</span></span>  <br/> |<span data-ttu-id="8043c-124">**Número**</span><span class="sxs-lookup"><span data-stu-id="8043c-124">**Nmber**</span></span> <br/> |<span data-ttu-id="8043c-125">O componente azul.</span><span class="sxs-lookup"><span data-stu-id="8043c-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8043c-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8043c-126">Return value</span></span>

<span data-ttu-id="8043c-127">Number</span><span class="sxs-lookup"><span data-stu-id="8043c-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8043c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="8043c-128">Remarks</span></span>

<span data-ttu-id="8043c-129">Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à paleta.</span><span class="sxs-lookup"><span data-stu-id="8043c-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="8043c-130">A tabela a seguir relaciona algumas cores padrão e seus valores de vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="8043c-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="8043c-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="8043c-131">**Color**</span></span>|<span data-ttu-id="8043c-132">**Valor de vermelho**</span><span class="sxs-lookup"><span data-stu-id="8043c-132">**Red value**</span></span>|<span data-ttu-id="8043c-133">**Valor de verde**</span><span class="sxs-lookup"><span data-stu-id="8043c-133">**Green value**</span></span>|<span data-ttu-id="8043c-134">**Valor de azul**</span><span class="sxs-lookup"><span data-stu-id="8043c-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="8043c-135">Preto</span><span class="sxs-lookup"><span data-stu-id="8043c-135">Black</span></span>  <br/> |<span data-ttu-id="8043c-136">0</span><span class="sxs-lookup"><span data-stu-id="8043c-136">0</span></span>  <br/> |<span data-ttu-id="8043c-137">0</span><span class="sxs-lookup"><span data-stu-id="8043c-137">0</span></span>  <br/> |<span data-ttu-id="8043c-138">0</span><span class="sxs-lookup"><span data-stu-id="8043c-138">0</span></span>  <br/> |
|<span data-ttu-id="8043c-139">Azul</span><span class="sxs-lookup"><span data-stu-id="8043c-139">Blue</span></span>  <br/> |<span data-ttu-id="8043c-140">0</span><span class="sxs-lookup"><span data-stu-id="8043c-140">0</span></span>  <br/> |<span data-ttu-id="8043c-141">0</span><span class="sxs-lookup"><span data-stu-id="8043c-141">0</span></span>  <br/> |<span data-ttu-id="8043c-142">255</span><span class="sxs-lookup"><span data-stu-id="8043c-142">255</span></span>  <br/> |
|<span data-ttu-id="8043c-143">Verde</span><span class="sxs-lookup"><span data-stu-id="8043c-143">Green</span></span>  <br/> |<span data-ttu-id="8043c-144">0</span><span class="sxs-lookup"><span data-stu-id="8043c-144">0</span></span>  <br/> |<span data-ttu-id="8043c-145">255</span><span class="sxs-lookup"><span data-stu-id="8043c-145">255</span></span>  <br/> |<span data-ttu-id="8043c-146">0</span><span class="sxs-lookup"><span data-stu-id="8043c-146">0</span></span>  <br/> |
|<span data-ttu-id="8043c-147">Ciano</span><span class="sxs-lookup"><span data-stu-id="8043c-147">Cyan</span></span>  <br/> |<span data-ttu-id="8043c-148">0</span><span class="sxs-lookup"><span data-stu-id="8043c-148">0</span></span>  <br/> |<span data-ttu-id="8043c-149">255</span><span class="sxs-lookup"><span data-stu-id="8043c-149">255</span></span>  <br/> |<span data-ttu-id="8043c-150">255</span><span class="sxs-lookup"><span data-stu-id="8043c-150">255</span></span>  <br/> |
|<span data-ttu-id="8043c-151">Vermelho</span><span class="sxs-lookup"><span data-stu-id="8043c-151">Red</span></span>  <br/> |<span data-ttu-id="8043c-152">255</span><span class="sxs-lookup"><span data-stu-id="8043c-152">255</span></span>  <br/> |<span data-ttu-id="8043c-153">0</span><span class="sxs-lookup"><span data-stu-id="8043c-153">0</span></span>  <br/> |<span data-ttu-id="8043c-154">0</span><span class="sxs-lookup"><span data-stu-id="8043c-154">0</span></span>  <br/> |
|<span data-ttu-id="8043c-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="8043c-155">Magenta</span></span>  <br/> |<span data-ttu-id="8043c-156">255</span><span class="sxs-lookup"><span data-stu-id="8043c-156">255</span></span>  <br/> |<span data-ttu-id="8043c-157">0</span><span class="sxs-lookup"><span data-stu-id="8043c-157">0</span></span>  <br/> |<span data-ttu-id="8043c-158">255</span><span class="sxs-lookup"><span data-stu-id="8043c-158">255</span></span>  <br/> |
|<span data-ttu-id="8043c-159">Amarelo</span><span class="sxs-lookup"><span data-stu-id="8043c-159">Yellow</span></span>  <br/> |<span data-ttu-id="8043c-160">255</span><span class="sxs-lookup"><span data-stu-id="8043c-160">255</span></span>  <br/> |<span data-ttu-id="8043c-161">255</span><span class="sxs-lookup"><span data-stu-id="8043c-161">255</span></span>  <br/> |<span data-ttu-id="8043c-162">0</span><span class="sxs-lookup"><span data-stu-id="8043c-162">0</span></span>  <br/> |
|<span data-ttu-id="8043c-163">Branco</span><span class="sxs-lookup"><span data-stu-id="8043c-163">White</span></span>  <br/> |<span data-ttu-id="8043c-164">255</span><span class="sxs-lookup"><span data-stu-id="8043c-164">255</span></span>  <br/> |<span data-ttu-id="8043c-165">255</span><span class="sxs-lookup"><span data-stu-id="8043c-165">255</span></span>  <br/> |<span data-ttu-id="8043c-166">255</span><span class="sxs-lookup"><span data-stu-id="8043c-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="8043c-167">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8043c-167">Example 1</span></span>

<span data-ttu-id="8043c-168">RGB(0,0,255)</span><span class="sxs-lookup"><span data-stu-id="8043c-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="8043c-169">Retornará o índice da cor azul.</span><span class="sxs-lookup"><span data-stu-id="8043c-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8043c-170">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8043c-170">Example 2</span></span>

<span data-ttu-id="8043c-171">RGB (vermelho (Sheet.1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="8043c-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="8043c-172">Retornará o índice de uma cor cujo componente vermelho espelhe o primeiro plano de preenchimento de Sheet.1.</span><span class="sxs-lookup"><span data-stu-id="8043c-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

