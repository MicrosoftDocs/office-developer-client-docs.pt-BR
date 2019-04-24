---
title: Função HUE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: Retorna o valor do componente de matiz de uma cor.
ms.openlocfilehash: 39fdd160f5cd792e95930a3e7c7cea3c37ed16c1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329908"
---
# <a name="hue-function"></a><span data-ttu-id="a0df2-103">Função HUE</span><span class="sxs-lookup"><span data-stu-id="a0df2-103">HUE Function</span></span>

<span data-ttu-id="a0df2-104">Retorna o valor do componente de matiz de uma cor.</span><span class="sxs-lookup"><span data-stu-id="a0df2-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a0df2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0df2-105">Syntax</span></span>

<span data-ttu-id="a0df2-106">MATIZ (\* \* *expressão* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a0df2-106">HUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a0df2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0df2-107">Parameters</span></span>

|<span data-ttu-id="a0df2-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a0df2-108">**Name**</span></span>|<span data-ttu-id="a0df2-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="a0df2-109">**Required/Optional**</span></span>|<span data-ttu-id="a0df2-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="a0df2-110">**Data Type**</span></span>|<span data-ttu-id="a0df2-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a0df2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a0df2-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="a0df2-112">_expression_</span></span> <br/> |<span data-ttu-id="a0df2-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="a0df2-113">Required</span></span>  <br/> |<span data-ttu-id="a0df2-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a0df2-114">**String**</span></span> <br/> |<span data-ttu-id="a0df2-115">Uma expressão que é avaliada para uma cor.</span><span class="sxs-lookup"><span data-stu-id="a0df2-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a0df2-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a0df2-116">Return value</span></span>

<span data-ttu-id="a0df2-117">Número</span><span class="sxs-lookup"><span data-stu-id="a0df2-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0df2-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0df2-118">Remarks</span></span>

<span data-ttu-id="a0df2-p101">O valor retornado é um número entre 0 e 239, inclusive. A entrada é um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores. A função retornará 0 para uma entrada inválida.</span><span class="sxs-lookup"><span data-stu-id="a0df2-p101">The return value is a number in the range 0 to 239, inclusive. The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a0df2-122">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a0df2-122">Example 1</span></span>

<span data-ttu-id="a0df2-123">MATIZ (planilha. 4! FillForegnd</span><span class="sxs-lookup"><span data-stu-id="a0df2-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="a0df2-124">Retornará a matiz da cor de preenchimento de primeiro plano de Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="a0df2-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a0df2-125">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a0df2-125">Example 2</span></span>

<span data-ttu-id="a0df2-126">MATIZ (7)</span><span class="sxs-lookup"><span data-stu-id="a0df2-126">HUE(7)</span></span>
  
<span data-ttu-id="a0df2-127">Retornará 120 se o documento utilizar a paleta de cores padrão do Microsoft Visio, sendo ciano a cor do índice 7.</span><span class="sxs-lookup"><span data-stu-id="a0df2-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a0df2-128">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="a0df2-128">Example 3</span></span>

<span data-ttu-id="a0df2-129">HUE(HSL(10, 20, 30) )</span><span class="sxs-lookup"><span data-stu-id="a0df2-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="a0df2-130">Retornará 10.</span><span class="sxs-lookup"><span data-stu-id="a0df2-130">Returns 10.</span></span>
  

