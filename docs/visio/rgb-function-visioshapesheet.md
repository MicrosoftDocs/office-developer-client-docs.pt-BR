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
description: Retorna um valor que representa um índice na paleta de cores do documento. Especifica uma cor por seus componentes vermelho, verde e azul, onde cada um é um número no intervalo de 0 a 255, inclusive, ou uma expressão que é avaliada como um número.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326737"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="037ec-104">Função RGB (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="037ec-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="037ec-105">Retorna um valor que representa um índice na paleta de cores do documento.</span><span class="sxs-lookup"><span data-stu-id="037ec-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="037ec-106">Especifica uma cor por seus componentes vermelho, verde e azul, onde cada um é um número no intervalo de 0 a 255, inclusive, ou uma expressão que é avaliada como um número.</span><span class="sxs-lookup"><span data-stu-id="037ec-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="037ec-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="037ec-107">Syntax</span></span>

<span data-ttu-id="037ec-108">RGB (\* \* *vermelho* \* \*, \* \* *verde* \* \*, \* \* *azul* \* \*)</span><span class="sxs-lookup"><span data-stu-id="037ec-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="037ec-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="037ec-109">Parameters</span></span>

|<span data-ttu-id="037ec-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="037ec-110">**Name**</span></span>|<span data-ttu-id="037ec-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="037ec-111">**Required/Optional**</span></span>|<span data-ttu-id="037ec-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="037ec-112">**Data Type**</span></span>|<span data-ttu-id="037ec-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="037ec-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="037ec-114">_vermelha_</span><span class="sxs-lookup"><span data-stu-id="037ec-114">_red_</span></span> <br/> |<span data-ttu-id="037ec-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="037ec-115">Required</span></span>  <br/> |<span data-ttu-id="037ec-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="037ec-116">**Number**</span></span> <br/> |<span data-ttu-id="037ec-117">O componente vermelho.</span><span class="sxs-lookup"><span data-stu-id="037ec-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="037ec-118">_natureza_</span><span class="sxs-lookup"><span data-stu-id="037ec-118">_green_</span></span> <br/> |<span data-ttu-id="037ec-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="037ec-119">Required</span></span>  <br/> |<span data-ttu-id="037ec-120">**Número**</span><span class="sxs-lookup"><span data-stu-id="037ec-120">**Number**</span></span> <br/> |<span data-ttu-id="037ec-121">O componente verde.</span><span class="sxs-lookup"><span data-stu-id="037ec-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="037ec-122">_azuis_</span><span class="sxs-lookup"><span data-stu-id="037ec-122">_blue_</span></span> <br/> |<span data-ttu-id="037ec-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="037ec-123">Required</span></span>  <br/> |<span data-ttu-id="037ec-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="037ec-124">**Nmber**</span></span> <br/> |<span data-ttu-id="037ec-125">O componente azul.</span><span class="sxs-lookup"><span data-stu-id="037ec-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="037ec-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="037ec-126">Return value</span></span>

<span data-ttu-id="037ec-127">Número</span><span class="sxs-lookup"><span data-stu-id="037ec-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="037ec-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="037ec-128">Remarks</span></span>

<span data-ttu-id="037ec-129">Se a cor retornada pela função ainda não existir na paleta de cores do documento atual, ela será adicionada à paleta.</span><span class="sxs-lookup"><span data-stu-id="037ec-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="037ec-130">A tabela a seguir relaciona algumas cores padrão e seus valores de vermelho, verde e azul.</span><span class="sxs-lookup"><span data-stu-id="037ec-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="037ec-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="037ec-131">**Color**</span></span>|<span data-ttu-id="037ec-132">**Valor de vermelho**</span><span class="sxs-lookup"><span data-stu-id="037ec-132">**Red value**</span></span>|<span data-ttu-id="037ec-133">**Valor de verde**</span><span class="sxs-lookup"><span data-stu-id="037ec-133">**Green value**</span></span>|<span data-ttu-id="037ec-134">**Valor de azul**</span><span class="sxs-lookup"><span data-stu-id="037ec-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="037ec-135">Preto</span><span class="sxs-lookup"><span data-stu-id="037ec-135">Black</span></span>  <br/> |<span data-ttu-id="037ec-136">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-136">0</span></span>  <br/> |<span data-ttu-id="037ec-137">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-137">0</span></span>  <br/> |<span data-ttu-id="037ec-138">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-138">0</span></span>  <br/> |
|<span data-ttu-id="037ec-139">Azul</span><span class="sxs-lookup"><span data-stu-id="037ec-139">Blue</span></span>  <br/> |<span data-ttu-id="037ec-140">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-140">0</span></span>  <br/> |<span data-ttu-id="037ec-141">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-141">0</span></span>  <br/> |<span data-ttu-id="037ec-142">255</span><span class="sxs-lookup"><span data-stu-id="037ec-142">255</span></span>  <br/> |
|<span data-ttu-id="037ec-143">Verde</span><span class="sxs-lookup"><span data-stu-id="037ec-143">Green</span></span>  <br/> |<span data-ttu-id="037ec-144">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-144">0</span></span>  <br/> |<span data-ttu-id="037ec-145">255</span><span class="sxs-lookup"><span data-stu-id="037ec-145">255</span></span>  <br/> |<span data-ttu-id="037ec-146">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-146">0</span></span>  <br/> |
|<span data-ttu-id="037ec-147">Ciano</span><span class="sxs-lookup"><span data-stu-id="037ec-147">Cyan</span></span>  <br/> |<span data-ttu-id="037ec-148">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-148">0</span></span>  <br/> |<span data-ttu-id="037ec-149">255</span><span class="sxs-lookup"><span data-stu-id="037ec-149">255</span></span>  <br/> |<span data-ttu-id="037ec-150">255</span><span class="sxs-lookup"><span data-stu-id="037ec-150">255</span></span>  <br/> |
|<span data-ttu-id="037ec-151">Vermelho</span><span class="sxs-lookup"><span data-stu-id="037ec-151">Red</span></span>  <br/> |<span data-ttu-id="037ec-152">255</span><span class="sxs-lookup"><span data-stu-id="037ec-152">255</span></span>  <br/> |<span data-ttu-id="037ec-153">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-153">0</span></span>  <br/> |<span data-ttu-id="037ec-154">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-154">0</span></span>  <br/> |
|<span data-ttu-id="037ec-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="037ec-155">Magenta</span></span>  <br/> |<span data-ttu-id="037ec-156">255</span><span class="sxs-lookup"><span data-stu-id="037ec-156">255</span></span>  <br/> |<span data-ttu-id="037ec-157">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-157">0</span></span>  <br/> |<span data-ttu-id="037ec-158">255</span><span class="sxs-lookup"><span data-stu-id="037ec-158">255</span></span>  <br/> |
|<span data-ttu-id="037ec-159">Amarelo</span><span class="sxs-lookup"><span data-stu-id="037ec-159">Yellow</span></span>  <br/> |<span data-ttu-id="037ec-160">255</span><span class="sxs-lookup"><span data-stu-id="037ec-160">255</span></span>  <br/> |<span data-ttu-id="037ec-161">255</span><span class="sxs-lookup"><span data-stu-id="037ec-161">255</span></span>  <br/> |<span data-ttu-id="037ec-162">,0</span><span class="sxs-lookup"><span data-stu-id="037ec-162">0</span></span>  <br/> |
|<span data-ttu-id="037ec-163">Branco</span><span class="sxs-lookup"><span data-stu-id="037ec-163">White</span></span>  <br/> |<span data-ttu-id="037ec-164">255</span><span class="sxs-lookup"><span data-stu-id="037ec-164">255</span></span>  <br/> |<span data-ttu-id="037ec-165">255</span><span class="sxs-lookup"><span data-stu-id="037ec-165">255</span></span>  <br/> |<span data-ttu-id="037ec-166">255</span><span class="sxs-lookup"><span data-stu-id="037ec-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="037ec-167">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="037ec-167">Example 1</span></span>

<span data-ttu-id="037ec-168">RGB (0, 0255)</span><span class="sxs-lookup"><span data-stu-id="037ec-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="037ec-169">Retornará o índice da cor azul.</span><span class="sxs-lookup"><span data-stu-id="037ec-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="037ec-170">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="037ec-170">Example 2</span></span>

<span data-ttu-id="037ec-171">RGB (vermelho (planilha. 1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="037ec-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="037ec-172">Retornará o índice de uma cor cujo componente vermelho espelhe o primeiro plano de preenchimento de Sheet.1.</span><span class="sxs-lookup"><span data-stu-id="037ec-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

