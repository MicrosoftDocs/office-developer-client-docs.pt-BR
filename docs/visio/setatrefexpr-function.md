---
title: Função SETATREFEXPR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027317
localization_priority: Normal
ms.assetid: c1bd7819-b53b-bff1-69c1-6d78e8fb278b
description: Armazena um valor que é definido por meio de uma ação na interface do usuário (UI) ou automação.
ms.openlocfilehash: c664717afcc2b81e55495fd1957a86ef1b021d0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772880"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="29ab1-103">Função SETATREFEXPR</span><span class="sxs-lookup"><span data-stu-id="29ab1-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="29ab1-104">Armazena um valor que é definido por meio de uma ação na interface do usuário (UI) ou automação.</span><span class="sxs-lookup"><span data-stu-id="29ab1-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="29ab1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29ab1-105">Syntax</span></span>

<span data-ttu-id="29ab1-106">SETATREFEXPR ([* * *expr_opt* * *])</span><span class="sxs-lookup"><span data-stu-id="29ab1-106">SETATREFEXPR ([ ** *expr_opt* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="29ab1-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29ab1-107">Parameters</span></span>

|<span data-ttu-id="29ab1-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="29ab1-108">**Name**</span></span>|<span data-ttu-id="29ab1-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="29ab1-109">**Required/Optional**</span></span>|<span data-ttu-id="29ab1-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="29ab1-110">**Data Type**</span></span>|<span data-ttu-id="29ab1-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="29ab1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="29ab1-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="29ab1-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="29ab1-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="29ab1-113">Optional</span></span>  <br/> |<span data-ttu-id="29ab1-114">**Varia**</span><span class="sxs-lookup"><span data-stu-id="29ab1-114">**Varies**</span></span> <br/> |<span data-ttu-id="29ab1-115">Uma expressão que é substituída pelo valor ou expressão que está sendo atribuído à célula referenciada na função SETATREF.</span><span class="sxs-lookup"><span data-stu-id="29ab1-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="29ab1-116">Se não foi indicado, seu valor inicial é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="29ab1-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29ab1-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="29ab1-117">Remarks</span></span>

<span data-ttu-id="29ab1-118">O valor de uma expressão SETATREFEXPR também pode ser definido a partir de uma função SETATREF em outra célula que faça referência à célula que contém a expressão SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="29ab1-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="29ab1-119">Você não está limitado a usar a função SETATREFEXPR como um parâmetro para a função SETATREF.</span><span class="sxs-lookup"><span data-stu-id="29ab1-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="29ab1-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="29ab1-120">Example 1</span></span>

<span data-ttu-id="29ab1-121">O seguinte exemplo usa a função SETATREFEXPR para garantir que uma forma seja tão grande quanto seu texto.</span><span class="sxs-lookup"><span data-stu-id="29ab1-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="29ab1-122">Largura =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="29ab1-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="29ab1-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="29ab1-123">Example 2</span></span>

<span data-ttu-id="29ab1-p102">O seguinte exemplo mostra como você pode usar a função SETATREFEXPR para fazer com que sua forma se encaixe a uma grade personalizada. As fórmulas SETATREFEXPR são colocadas nas células PinX e PinY, fazendo com que o pino da forma se encaixe na grade definida em User.GridX e User.GridY.</span><span class="sxs-lookup"><span data-stu-id="29ab1-p102">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid. The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="29ab1-126">User.GridX =2 pol</span><span class="sxs-lookup"><span data-stu-id="29ab1-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="29ab1-127">User.GridY =2 pol</span><span class="sxs-lookup"><span data-stu-id="29ab1-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="29ab1-128">PinX = INT (SETATREFEXPR () /User.GridX +.5)\*User. GridX</span><span class="sxs-lookup"><span data-stu-id="29ab1-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="29ab1-129">PinY = INT (SETATREFEXPR () /User.GridY +.5)\*User. GridY</span><span class="sxs-lookup"><span data-stu-id="29ab1-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="29ab1-130">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="29ab1-130">Example 3</span></span>

<span data-ttu-id="29ab1-131">Para um exemplo usando a função SETATREFEXPR com a função SETATREF, consulte a função [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="29ab1-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

