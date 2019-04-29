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
description: Armazena um valor definido por meio de uma ação na interface do usuário ou automação.
ms.openlocfilehash: 5ca7b59d0ced9c3da346c416826ac89e6b4001da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439048"
---
# <a name="setatrefexpr-function"></a><span data-ttu-id="6465d-103">Função SETATREFEXPR</span><span class="sxs-lookup"><span data-stu-id="6465d-103">SETATREFEXPR Function</span></span>

<span data-ttu-id="6465d-104">Armazena um valor definido por meio de uma ação na interface do usuário ou automação.</span><span class="sxs-lookup"><span data-stu-id="6465d-104">Stores a value that is set through an action in the user interface (UI) or Automation.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6465d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6465d-105">Syntax</span></span>

<span data-ttu-id="6465d-106">SETATREFEXPR ([\* \* *expr_opt* \* \*])</span><span class="sxs-lookup"><span data-stu-id="6465d-106">SETATREFEXPR ([ \*\* *expr_opt* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6465d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6465d-107">Parameters</span></span>

|<span data-ttu-id="6465d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="6465d-108">**Name**</span></span>|<span data-ttu-id="6465d-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="6465d-109">**Required/Optional**</span></span>|<span data-ttu-id="6465d-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="6465d-110">**Data Type**</span></span>|<span data-ttu-id="6465d-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6465d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6465d-112">_expr_opt_</span><span class="sxs-lookup"><span data-stu-id="6465d-112">_expr_opt_</span></span> <br/> |<span data-ttu-id="6465d-113">Opcional</span><span class="sxs-lookup"><span data-stu-id="6465d-113">Optional</span></span>  <br/> |<span data-ttu-id="6465d-114">**Vai**</span><span class="sxs-lookup"><span data-stu-id="6465d-114">**Varies**</span></span> <br/> |<span data-ttu-id="6465d-115">Uma expressão substituída pelo valor ou expressão atribuída à célula referenciada na função SETATREF.</span><span class="sxs-lookup"><span data-stu-id="6465d-115">An expression that is replaced by the value or expression being assigned to the referenced cell in the SETATREF function.</span></span> <span data-ttu-id="6465d-116">Se não for indicado, seu valor inicial será 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6465d-116">If not indicated, its initial value is 0 (zero).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6465d-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="6465d-117">Remarks</span></span>

<span data-ttu-id="6465d-118">O valor de uma expressão SETATREFEXPR também pode ser definido a partir de uma função SETATREF em outra célula que faça referência à célula que contém a expressão SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="6465d-118">The value of a SETATREFEXPR expression can also be set from a SETATREF function in another cell that references the cell containing the SETATREFEXPR expression.</span></span> 
  
<span data-ttu-id="6465d-119">Você não está limitado a usar a função SETATREFEXPR como um parâmetro para a função SETATREF.</span><span class="sxs-lookup"><span data-stu-id="6465d-119">You are not limited to using the SETATREFEXPR function as a parameter to the SETATREF function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6465d-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6465d-120">Example 1</span></span>

<span data-ttu-id="6465d-121">O seguinte exemplo usa a função SETATREFEXPR para garantir que uma forma seja tão grande quanto seu texto.</span><span class="sxs-lookup"><span data-stu-id="6465d-121">The following example uses the SETATREFEXPR function to ensure that a shape is as wide as its text.</span></span>
  
<span data-ttu-id="6465d-122">Largura =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span><span class="sxs-lookup"><span data-stu-id="6465d-122">Width =MAX(TEXTWIDTH(TheText),SETATREFEXPR())</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6465d-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6465d-123">Example 2</span></span>

<span data-ttu-id="6465d-p102">O seguinte exemplo mostra como você pode usar a função SETATREFEXPR para fazer com que sua forma se encaixe a uma grade personalizada. As fórmulas SETATREFEXPR são colocadas nas células PinX e PinY, fazendo com que o pino da forma se encaixe na grade definida em User.GridX e User.GridY.</span><span class="sxs-lookup"><span data-stu-id="6465d-p102">The following example shows how you can use the SETATREFEXPR function to cause your shapes to snap to a custom grid. The SETATREFEXPR formulas are placed in the PinX and PinY cells, causing the shape's pin to snap to the grid defined in User.GridX and User.GridY.</span></span> 
  
<span data-ttu-id="6465d-126">User.GridX =2 pol</span><span class="sxs-lookup"><span data-stu-id="6465d-126">User.GridX =2 in</span></span>
  
<span data-ttu-id="6465d-127">User.GridY =2 pol</span><span class="sxs-lookup"><span data-stu-id="6465d-127">User.GridY =2 in</span></span>
  
<span data-ttu-id="6465d-128">PinX = INT (SETATREFEXPR ()/User.GridX + 0,5)\*User. gradex</span><span class="sxs-lookup"><span data-stu-id="6465d-128">PinX =INT(SETATREFEXPR()/User.GridX + .5)\*User.GridX</span></span>
  
<span data-ttu-id="6465d-129">PinY = INT (SETATREFEXPR ()/User.GridY + 0,5)\*User. GridY</span><span class="sxs-lookup"><span data-stu-id="6465d-129">PinY =INT(SETATREFEXPR()/User.GridY + .5)\*User.GridY</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6465d-130">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6465d-130">Example 3</span></span>

<span data-ttu-id="6465d-131">Para um exemplo usando a função SETATREFEXPR com a função SETATREF, consulte a função [SETATREF](setatref-function.md).</span><span class="sxs-lookup"><span data-stu-id="6465d-131">For an example using the SETATREFEXPR function with the SETATREF function, see the [SETATREF](setatref-function.md) function.</span></span> 
  

