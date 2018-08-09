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
ms.openlocfilehash: 2a532e305eb7cbabc5ba07dcace6c07a337e7743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772034"
---
# <a name="hue-function"></a><span data-ttu-id="f90d5-103">Função HUE</span><span class="sxs-lookup"><span data-stu-id="f90d5-103">HUE Function</span></span>

<span data-ttu-id="f90d5-104">Retorna o valor do componente de matiz de uma cor.</span><span class="sxs-lookup"><span data-stu-id="f90d5-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f90d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f90d5-105">Syntax</span></span>

<span data-ttu-id="f90d5-106">MATIZ (* * *expressão* * *)</span><span class="sxs-lookup"><span data-stu-id="f90d5-106">HUE(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f90d5-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f90d5-107">Parameters</span></span>

|<span data-ttu-id="f90d5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="f90d5-108">**Name**</span></span>|<span data-ttu-id="f90d5-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="f90d5-109">**Required/Optional**</span></span>|<span data-ttu-id="f90d5-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="f90d5-110">**Data Type**</span></span>|<span data-ttu-id="f90d5-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f90d5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f90d5-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="f90d5-112">_expression_</span></span> <br/> |<span data-ttu-id="f90d5-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f90d5-113">Required</span></span>  <br/> |<span data-ttu-id="f90d5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f90d5-114">**String**</span></span> <br/> |<span data-ttu-id="f90d5-115">Uma expressão que é avaliada para uma cor.</span><span class="sxs-lookup"><span data-stu-id="f90d5-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f90d5-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f90d5-116">Return value</span></span>

<span data-ttu-id="f90d5-117">Number</span><span class="sxs-lookup"><span data-stu-id="f90d5-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f90d5-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="f90d5-118">Remarks</span></span>

<span data-ttu-id="f90d5-p101">O valor retornado é um número entre 0 e 239, inclusive. A entrada é um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores. A função retornará 0 para uma entrada inválida.</span><span class="sxs-lookup"><span data-stu-id="f90d5-p101">The return value is a number in the range 0 to 239, inclusive. The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f90d5-122">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f90d5-122">Example 1</span></span>

<span data-ttu-id="f90d5-123">MATIZ (Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="f90d5-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="f90d5-124">Retornará a matiz da cor de preenchimento de primeiro plano de Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="f90d5-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f90d5-125">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="f90d5-125">Example 2</span></span>

<span data-ttu-id="f90d5-126">HUE(7)</span><span class="sxs-lookup"><span data-stu-id="f90d5-126">HUE(7)</span></span>
  
<span data-ttu-id="f90d5-127">Retornará 120 se o documento utilizar a paleta de cores padrão do Microsoft Visio, sendo ciano a cor do índice 7.</span><span class="sxs-lookup"><span data-stu-id="f90d5-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f90d5-128">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="f90d5-128">Example 3</span></span>

<span data-ttu-id="f90d5-129">HUE(HSL(10, 20, 30) )</span><span class="sxs-lookup"><span data-stu-id="f90d5-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="f90d5-130">Retornará 10.</span><span class="sxs-lookup"><span data-stu-id="f90d5-130">Returns 10.</span></span>
  

