---
title: Função GUARD
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251435
localization_priority: Normal
ms.assetid: 6c85414c-9fb6-cdc5-f5b6-8eb13c9608af
description: Protege a expressão contra exclusão e alteração por ações executadas na janela de desenho, por exemplo, mover, dimensionamento, agrupar ou desagrupar as formas.
ms.openlocfilehash: fd5fcfbe11eb054dfa625834640c0280cae96c3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771985"
---
# <a name="guard-function"></a><span data-ttu-id="b0d05-103">Função GUARD</span><span class="sxs-lookup"><span data-stu-id="b0d05-103">GUARD Function</span></span>

<span data-ttu-id="b0d05-104">Protege a *expressão* contra exclusão e alteração por ações executadas na janela de desenho, por exemplo, mover, dimensionamento, agrupar ou desagrupar as formas.</span><span class="sxs-lookup"><span data-stu-id="b0d05-104">Protects  *expression*  from deletion and change by actions performed in the drawing window, for example, moving, sizing, grouping, or ungrouping shapes.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b0d05-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0d05-105">Syntax</span></span>

<span data-ttu-id="b0d05-106">GUARD (* * *expressão* * *)</span><span class="sxs-lookup"><span data-stu-id="b0d05-106">GUARD(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b0d05-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b0d05-107">Parameters</span></span>

|<span data-ttu-id="b0d05-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b0d05-108">**Name**</span></span>|<span data-ttu-id="b0d05-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="b0d05-109">**Required/Optional**</span></span>|<span data-ttu-id="b0d05-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="b0d05-110">**Data Type**</span></span>|<span data-ttu-id="b0d05-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b0d05-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b0d05-112">_expressão_</span><span class="sxs-lookup"><span data-stu-id="b0d05-112">_expression_</span></span> <br/> |<span data-ttu-id="b0d05-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b0d05-113">Required</span></span>  <br/> |<span data-ttu-id="b0d05-114">**String**</span><span class="sxs-lookup"><span data-stu-id="b0d05-114">**String**</span></span> <br/> |<span data-ttu-id="b0d05-115">Uma combinação de constantes, operadores, funções e referências a células ShapeSheet que resulta em um valor.</span><span class="sxs-lookup"><span data-stu-id="b0d05-115">A combination of constants, operators, functions, and references to ShapeSheet cells that results in a value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b0d05-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b0d05-116">Remarks</span></span>

<span data-ttu-id="b0d05-117">As células normalmente afetadas pela função GUARD são Width, Height, PinX e PinY.</span><span class="sxs-lookup"><span data-stu-id="b0d05-117">The cells most often affected by the GUARD function are Width, Height, PinX, and PinY.</span></span> 
  
<span data-ttu-id="b0d05-p101">Proteger uma fórmula em qualquer célula evita que o valor da célula seja alterado por ações executadas na janela de desenho. No entanto, uma ação na janela de desenho pode afetar diversas células e cada uma dessas células deve estar protegida caso você deseje evitar alterações inesperadas na aparência da forma.</span><span class="sxs-lookup"><span data-stu-id="b0d05-p101">Guarding a formula in any cell prevents that cell's value from being changed by actions in the drawing window. However, one action in the drawing window can affect several cells, and each of these cells must be guarded if you want to prevent unexpected changes to the shape's appearance.</span></span> 
  
## <a name="example"></a><span data-ttu-id="b0d05-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="b0d05-120">Example</span></span>

<span data-ttu-id="b0d05-121">GUARD(TEXTWIDTH(TheText) + 0,5 pol.)</span><span class="sxs-lookup"><span data-stu-id="b0d05-121">GUARD(TEXTWIDTH(TheText) + 0.5 in)</span></span> 
  
<span data-ttu-id="b0d05-p102">Esta expressão na célula Width de uma seção Shape Transform de uma forma impede que a expressão (TEXTWIDTH(TheText) + 0,5 pol.) seja substituída por outro valor quando a largura da forma for alterada na janela de desenho. TheText é uma célula disparada quando a composição do texto da forma associada é alterada.</span><span class="sxs-lookup"><span data-stu-id="b0d05-p102">This expression in the Width cell of a shape's Shape Transform section prevents the expression (TEXTWIDTH(TheText) + 0.5 in) from being replaced with another value when the shape's width is changed in the drawing window. TheText is a cell that gets triggered when the associated shape's text composition changes.</span></span> 
  

