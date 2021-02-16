---
title: Função SHAPETEXT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251788
localization_priority: Normal
ms.assetid: 87ea5e8f-c3e0-009f-4bf8-8c34fbdb83a6
description: Obtém o texto de uma forma.
ms.openlocfilehash: bb9b1fbe5900cd051828ed6c7ff07546567c1b23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419342"
---
# <a name="shapetext-function"></a><span data-ttu-id="d7093-103">Função SHAPETEXT</span><span class="sxs-lookup"><span data-stu-id="d7093-103">SHAPETEXT Function</span></span>

<span data-ttu-id="d7093-104">Obtém o texto de uma forma.</span><span class="sxs-lookup"><span data-stu-id="d7093-104">Gets the text from a shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d7093-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7093-105">Syntax</span></span>

<span data-ttu-id="d7093-106">SHAPETEXT (\*\* *shapename! TheText* \*\* \*\* *[,flag]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d7093-106">SHAPETEXT (\*\* *shapename!TheText* \*\* \*\* *[,flag]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d7093-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7093-107">Parameters</span></span>

|<span data-ttu-id="d7093-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="d7093-108">**Name**</span></span>|<span data-ttu-id="d7093-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="d7093-109">**Required/Optional**</span></span>|<span data-ttu-id="d7093-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="d7093-110">**Data Type**</span></span>|<span data-ttu-id="d7093-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7093-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d7093-112">_shapename! TheText_</span><span class="sxs-lookup"><span data-stu-id="d7093-112">_shapename!TheText_</span></span> <br/> |<span data-ttu-id="d7093-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d7093-113">Required</span></span>  <br/> ||<span data-ttu-id="d7093-114">Uma referência à célula chamada TheText na forma de destino.</span><span class="sxs-lookup"><span data-stu-id="d7093-114">A reference to the cell named TheText in the target shape.</span></span>  <span data-ttu-id="d7093-115">_Shapename!_</span><span class="sxs-lookup"><span data-stu-id="d7093-115">_Shapename!_</span></span> <span data-ttu-id="d7093-116">é o nome da forma da qual você deseja recuperar o texto.</span><span class="sxs-lookup"><span data-stu-id="d7093-116">is the name of the shape from which you want to retrieve the text.</span></span>  <br/> |
| <span data-ttu-id="d7093-117">_sinalizador_</span><span class="sxs-lookup"><span data-stu-id="d7093-117">_flag_</span></span> <br/> |<span data-ttu-id="d7093-118">Opcional</span><span class="sxs-lookup"><span data-stu-id="d7093-118">Optional</span></span>  <br/> |<span data-ttu-id="d7093-119">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="d7093-119">**Numeric**</span></span> <br/> |<span data-ttu-id="d7093-120">Um bit que especifica o formato do texto.</span><span class="sxs-lookup"><span data-stu-id="d7093-120">A bit that specifies the format of the text.</span></span> <span data-ttu-id="d7093-121">O sinalizador padrão (0) mostra o texto exatamente como está na forma.</span><span class="sxs-lookup"><span data-stu-id="d7093-121">The default flag (0) shows the text exactly as it is shown in the shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d7093-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="d7093-122">Return value</span></span>

<span data-ttu-id="d7093-123">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="d7093-123">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7093-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7093-124">Remarks</span></span>

<span data-ttu-id="d7093-125">Utilize a combinação de qualquer um dos sinalizadores a seguir com a função STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="d7093-125">You can use any combination of the following flags with the SHAPETEXT function.</span></span>
  
|<span data-ttu-id="d7093-126">**Flag**</span><span class="sxs-lookup"><span data-stu-id="d7093-126">**Flag**</span></span>|<span data-ttu-id="d7093-127">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d7093-127">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d7093-128">0</span><span class="sxs-lookup"><span data-stu-id="d7093-128">0</span></span>  <br/> |<span data-ttu-id="d7093-129">Mostrar o texto exatamente como está na forma.</span><span class="sxs-lookup"><span data-stu-id="d7093-129">Show text exactly as shown in shape.</span></span>  <br/> |
|<span data-ttu-id="d7093-130">1 </span><span class="sxs-lookup"><span data-stu-id="d7093-130">1</span></span>  <br/> |<span data-ttu-id="d7093-131">Incluir hífens discricionários.</span><span class="sxs-lookup"><span data-stu-id="d7093-131">Include discretionary hyphens.</span></span>  <br/> |
|<span data-ttu-id="d7093-132">2 </span><span class="sxs-lookup"><span data-stu-id="d7093-132">2</span></span>  <br/> |<span data-ttu-id="d7093-133">Não incluir texto expandido nos campos.</span><span class="sxs-lookup"><span data-stu-id="d7093-133">Don't include expanded text in fields.</span></span>  <br/> |
|<span data-ttu-id="d7093-134">4 </span><span class="sxs-lookup"><span data-stu-id="d7093-134">4</span></span>  <br/> |<span data-ttu-id="d7093-135">Converter tabulações em espaços simples.</span><span class="sxs-lookup"><span data-stu-id="d7093-135">Convert tabs to a single space.</span></span>  <br/> |
|<span data-ttu-id="d7093-136">8 </span><span class="sxs-lookup"><span data-stu-id="d7093-136">8</span></span>  <br/> |<span data-ttu-id="d7093-137">Converter tabulações em um conjunto de espaços.</span><span class="sxs-lookup"><span data-stu-id="d7093-137">Convert tabs to a set of spaces.</span></span>  <br/> |
|<span data-ttu-id="d7093-138">16 </span><span class="sxs-lookup"><span data-stu-id="d7093-138">16</span></span>  <br/> |<span data-ttu-id="d7093-139">Converter retornos de texto e alimentação de linhas em espaços.</span><span class="sxs-lookup"><span data-stu-id="d7093-139">Convert carriage returns and line feeds to spaces.</span></span>  <br/> |
|<span data-ttu-id="d7093-140">32</span><span class="sxs-lookup"><span data-stu-id="d7093-140">32</span></span>  <br/> |<span data-ttu-id="d7093-141">Converter aspas tipográficas em aspas normais.</span><span class="sxs-lookup"><span data-stu-id="d7093-141">Convert typographer quotes to regular quotes.</span></span>  <br/> |
|<span data-ttu-id="d7093-142">64</span><span class="sxs-lookup"><span data-stu-id="d7093-142">64</span></span>  <br/> |<span data-ttu-id="d7093-143">Converter espaços em branco adjacentes em um espaço simples.</span><span class="sxs-lookup"><span data-stu-id="d7093-143">Convert adjacent white space to a single space.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="d7093-144">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d7093-144">Example 1</span></span>

<span data-ttu-id="d7093-145">SHAPETEXT(sheetN!theText)</span><span class="sxs-lookup"><span data-stu-id="d7093-145">SHAPETEXT(sheetN!theText)</span></span>
  
<span data-ttu-id="d7093-146">Retornará o texto da forma sheetN exatamente como está na forma.</span><span class="sxs-lookup"><span data-stu-id="d7093-146">Returns the text of the shape named sheetN, exactly as it is shown in the shape.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d7093-147">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d7093-147">Example 2</span></span>

<span data-ttu-id="d7093-148">SHAPETEXT(theText)</span><span class="sxs-lookup"><span data-stu-id="d7093-148">SHAPETEXT(theText)</span></span>
  
<span data-ttu-id="d7093-149">Retornará o texto da forma atual exatamente como está na forma.</span><span class="sxs-lookup"><span data-stu-id="d7093-149">Returns the text of the current shape exactly as it is shown in the shape.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d7093-150">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d7093-150">Example 3</span></span>

<span data-ttu-id="d7093-151">SHAPETEXT(theText, 84)</span><span class="sxs-lookup"><span data-stu-id="d7093-151">SHAPETEXT(theText, 84)</span></span>
  
<span data-ttu-id="d7093-p103">Retornará o texto da forma atual. Converterá também espaço em branco adjacente em espaço simples (64), retornos de texto e alimentação de linhas em espaços (16) e tabulações em espaço simples (4). A soma desses sinalizadores é 84.</span><span class="sxs-lookup"><span data-stu-id="d7093-p103">Returns the text of the current shape. It also converts adjacent white space to a single space (64), converts carriage returns and line feeds to spaces (16), and converts tabs to a single space (4). The sum of these flags is 84.</span></span>
  

