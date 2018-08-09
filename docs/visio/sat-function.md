---
title: Função SAT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: Retorna o valor de componente de saturação de uma cor.
ms.openlocfilehash: 54f3fa68c567c2a32e8cfd37c406387cd6973ce3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772837"
---
# <a name="sat-function"></a><span data-ttu-id="c75a0-103">Função SAT</span><span class="sxs-lookup"><span data-stu-id="c75a0-103">SAT Function</span></span>

<span data-ttu-id="c75a0-104">Retorna o valor de componente de saturação de uma cor.</span><span class="sxs-lookup"><span data-stu-id="c75a0-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c75a0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c75a0-105">Syntax</span></span>

<span data-ttu-id="c75a0-106">SAT (* * *expressão* * *)</span><span class="sxs-lookup"><span data-stu-id="c75a0-106">SAT(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c75a0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c75a0-107">Parameters</span></span>

|<span data-ttu-id="c75a0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c75a0-108">**Name**</span></span>|<span data-ttu-id="c75a0-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c75a0-109">**Required/Optional**</span></span>|<span data-ttu-id="c75a0-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c75a0-110">**Data Type**</span></span>|<span data-ttu-id="c75a0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c75a0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c75a0-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="c75a0-112">_expression_</span></span> <br/> |<span data-ttu-id="c75a0-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c75a0-113">Required</span></span>  <br/> |<span data-ttu-id="c75a0-114">**Varia**</span><span class="sxs-lookup"><span data-stu-id="c75a0-114">**Varies**</span></span> <br/> |<span data-ttu-id="c75a0-115">Um índice de uma cor na tabela de cores do documento, uma expressão que resulta em uma cor personalizada (como RGB ou HSL) ou uma referência a uma célula que contém um índice de cores ou um resultado de cores.</span><span class="sxs-lookup"><span data-stu-id="c75a0-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c75a0-116">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c75a0-116">Return value</span></span>

<span data-ttu-id="c75a0-117">Numérico</span><span class="sxs-lookup"><span data-stu-id="c75a0-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c75a0-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="c75a0-118">Remarks</span></span>

<span data-ttu-id="c75a0-p101">O valor retornado é um número no intervalo de 0 a 240, inclusive. A função retornará 0 para uma entrada inválida.</span><span class="sxs-lookup"><span data-stu-id="c75a0-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="c75a0-121">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c75a0-121">Example 1</span></span>

<span data-ttu-id="c75a0-122">SAT (Sheet.4! FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="c75a0-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="c75a0-123">Retornará a saturação da cor de preenchimento de primeiro plano de Sheet.4.</span><span class="sxs-lookup"><span data-stu-id="c75a0-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c75a0-124">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c75a0-124">Example 2</span></span>

<span data-ttu-id="c75a0-125">SAT(8)</span><span class="sxs-lookup"><span data-stu-id="c75a0-125">SAT(8)</span></span>
  
<span data-ttu-id="c75a0-126">Retornará 240 se o documento utilizar a paleta de cores padrão do Visio, sendo vermelho escuro a cor do índice 8.</span><span class="sxs-lookup"><span data-stu-id="c75a0-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c75a0-127">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c75a0-127">Example 3</span></span>

<span data-ttu-id="c75a0-128">SAT(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="c75a0-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="c75a0-129">Retornará 20.</span><span class="sxs-lookup"><span data-stu-id="c75a0-129">Returns 20.</span></span>
  

