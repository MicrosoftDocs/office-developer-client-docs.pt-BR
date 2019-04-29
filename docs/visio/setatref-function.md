---
title: Função SETATREF
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60113
localization_priority: Normal
ms.assetid: 1ecfdb05-2533-470a-006b-e554026944d8
description: Redireciona valores atualizados resultantes de ações na interface do usuário ou automação para outra célula.
ms.openlocfilehash: c4f5fe94aba90ce0a69983d6637a5399b6e42707
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416801"
---
# <a name="setatref-function"></a><span data-ttu-id="9646d-103">Função SETATREF</span><span class="sxs-lookup"><span data-stu-id="9646d-103">SETATREF Function</span></span>

<span data-ttu-id="9646d-104">Redireciona valores atualizados resultantes de ações na interface do usuário ou automação para outra célula.</span><span class="sxs-lookup"><span data-stu-id="9646d-104">Redirects updated values resulting from actions in the user interface (UI) or Automation to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9646d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9646d-105">Syntax</span></span>

<span data-ttu-id="9646d-106">SETATREF (\* \* *referência* \* \* [, \* \* *def_expressão* \* \* [, \* \* *ignore_eval* \* \*]])</span><span class="sxs-lookup"><span data-stu-id="9646d-106">SETATREF(\*\* *reference* \*\* [, \*\* *set_expression* \*\* [, \*\* *ignore_eval* \*\* ]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9646d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9646d-107">Parameters</span></span>

|<span data-ttu-id="9646d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="9646d-108">**Name**</span></span>|<span data-ttu-id="9646d-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="9646d-109">**Required/Optional**</span></span>|<span data-ttu-id="9646d-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="9646d-110">**Data Type**</span></span>|<span data-ttu-id="9646d-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9646d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9646d-112">_reference_</span><span class="sxs-lookup"><span data-stu-id="9646d-112">_reference_</span></span> <br/> |<span data-ttu-id="9646d-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9646d-113">Required</span></span>  <br/> |<span data-ttu-id="9646d-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9646d-114">**String**</span></span> <br/> |<span data-ttu-id="9646d-115">Uma referência à célula para a qual as atualizações são redirecionadas.</span><span class="sxs-lookup"><span data-stu-id="9646d-115">A reference to the cell where updates are redirected.</span></span>  <br/> |
| <span data-ttu-id="9646d-116">_def_expressão_</span><span class="sxs-lookup"><span data-stu-id="9646d-116">_set_expression_</span></span> <br/> |<span data-ttu-id="9646d-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="9646d-117">Optional</span></span>  <br/> |<span data-ttu-id="9646d-118">**String**</span><span class="sxs-lookup"><span data-stu-id="9646d-118">**String**</span></span> <br/> |<span data-ttu-id="9646d-119">Uma expressão que é atribuída à _referência_.</span><span class="sxs-lookup"><span data-stu-id="9646d-119">An expression that is assigned to  _reference_.</span></span>  <br/> |
| <span data-ttu-id="9646d-120">_ignore_eval_</span><span class="sxs-lookup"><span data-stu-id="9646d-120">_ignore_eval_</span></span> <br/> |<span data-ttu-id="9646d-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="9646d-121">Optional</span></span>  <br/> |<span data-ttu-id="9646d-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="9646d-122">**Boolean**</span></span> <br/> |<span data-ttu-id="9646d-123">Se TRUE, a função SETATREF avalia como (0) zero; Se FALSE (o padrão), a função SETATREF será avaliada como o valor de _referência_.</span><span class="sxs-lookup"><span data-stu-id="9646d-123">If TRUE, the SETATREF function evaluates to (0) zero; if FALSE (the default) the SETATREF function evaluates to the value of  _reference_.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9646d-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9646d-124">Remarks</span></span>

<span data-ttu-id="9646d-125">Quando uma ação do usuário na janela de desenho ou um método de automação faz com que o Microsoft Visio atualize uma célula que contém uma fórmula SETATREF, o valor é redirecionado para a célula referenciada pela fórmula SETATREF ( _referência_).</span><span class="sxs-lookup"><span data-stu-id="9646d-125">When a user action in the drawing window, or an Automation method, causes Microsoft Visio to update a cell containing a SETATREF formula, the value is instead redirected to the cell referenced by the SETATREF formula ( _reference_).</span></span> <span data-ttu-id="9646d-126">A fórmula da célula que contém a função SETATREF permanece intacta.</span><span class="sxs-lookup"><span data-stu-id="9646d-126">The formula in the cell containing the SETATREF function remains intact.</span></span>
  
<span data-ttu-id="9646d-127">Se _def_expressão_ for omitido, o valor definido na interface do usuário ou usando a automação será atribuído à célula referenciada; caso contrário, o conteúdo de _def_expressão_ é atribuído à célula referenciada.</span><span class="sxs-lookup"><span data-stu-id="9646d-127">If  _set_expression_ is omitted, the value set in the UI or by using Automation is assigned to the referenced cell; otherwise, the contents of  _set_expression_ are assigned to the referenced cell.</span></span> <span data-ttu-id="9646d-128">Isso permite que o novo valor seja modificado ou transformado antes de ser atribuído à célula referenciada.</span><span class="sxs-lookup"><span data-stu-id="9646d-128">This allows the new value to be modified or transformed before being assigned to the referenced cell.</span></span> 
  
<span data-ttu-id="9646d-129">A função SETATREF possui duas funções relacionadas:</span><span class="sxs-lookup"><span data-stu-id="9646d-129">The SETATREF function has two related functions:</span></span> 
  
- <span data-ttu-id="9646d-130">A função SETATREFEXPR, que você pode usar para representar o novo valor dentro de _def_expressão_.</span><span class="sxs-lookup"><span data-stu-id="9646d-130">The SETATREFEXPR function, which you can use to represent the new value within  _set_expression_.</span></span> <span data-ttu-id="9646d-131">Por exemplo, uma _def_expressão_ de SETATREFEXPR ()-2 em.</span><span class="sxs-lookup"><span data-stu-id="9646d-131">For example, a  _set_expression_ of SETATREFEXPR()-2 in.</span></span> <span data-ttu-id="9646d-132">pode ser usado para subtrair 2 polegadas do resultado SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="9646d-132">could be used to subtract 2 inches from the SETATREFEXPR result.</span></span> 
    
- <span data-ttu-id="9646d-133">A função SETATREFEVAL, que você pode usar para indicar que alguma parte de _def_expressão_ deve ser avaliada e substituída por seu resultado.</span><span class="sxs-lookup"><span data-stu-id="9646d-133">The SETATREFEVAL function, which you can use to indicate that some portion of  _set_expression_ should be evaluated and replaced by its result.</span></span> 
    
<span data-ttu-id="9646d-134">A função SETATREF é projetada para ser usada em células que podem ser alteradas por ações do usuário na janela de desenho.</span><span class="sxs-lookup"><span data-stu-id="9646d-134">The SETATREF function is designed for use in cells that can be changed by user actions in the drawing window.</span></span> <span data-ttu-id="9646d-135">Há suporte para as seguintes células:</span><span class="sxs-lookup"><span data-stu-id="9646d-135">The following cells are supported:</span></span>
  
- <span data-ttu-id="9646d-136">seção ShapeTransform — células Width, Height, Angle, PinX e PinY</span><span class="sxs-lookup"><span data-stu-id="9646d-136">ShapeTransform section—Width, Height, Angle, PinX, and PinY cells</span></span>
    
- <span data-ttu-id="9646d-137">seção Text Transform — células TxtWidth, TxtHeight, TxtAngle, TxtPinX e TxtPinY</span><span class="sxs-lookup"><span data-stu-id="9646d-137">Text Transform section—TxtWidth, TxtHeight, TxtAngle, TxtPinX, and TxtPinY cells</span></span>
    
- <span data-ttu-id="9646d-138">seção 1-D Endpoints  — células BeginX, BeginY, EndX e EndY</span><span class="sxs-lookup"><span data-stu-id="9646d-138">1-D Endpoints section—BeginX, BeginY, EndX, and EndY cells</span></span>
    
- <span data-ttu-id="9646d-139">seção Controls — células Controls.X e Controls.Y</span><span class="sxs-lookup"><span data-stu-id="9646d-139">Controls section—Controls.X and Controls.Y cells</span></span>
    
- <span data-ttu-id="9646d-140">Seção Shape Data</span><span class="sxs-lookup"><span data-stu-id="9646d-140">Shape Data section</span></span>
    
<span data-ttu-id="9646d-141">Como SETATREF altera o local onde os valores das células mudam, ela afeta a emissão de eventos.</span><span class="sxs-lookup"><span data-stu-id="9646d-141">Because SETATREF changes the location where cell values change, it affects event firing.</span></span> <span data-ttu-id="9646d-142">Se uma célula contém SETATREF, os eventos **FormulaChanged** e **CellChanged** são emitidos para a célula referenciada por SETATREF, e não para a célula contendo SETATREF.</span><span class="sxs-lookup"><span data-stu-id="9646d-142">If a cell contains SETATREF, the **FormulaChanged** and **CellChanged** events fire for the cell that is referenced by SETATREF, not the cell containing SETATREF.</span></span> <span data-ttu-id="9646d-143">Se uma célula contendo SETATREF também contiver SETATREFEXPR, \*\*\*\* o evento formulachanged também será acionado para a célula que contém SETATREF porque um parâmetro de função é alterado.</span><span class="sxs-lookup"><span data-stu-id="9646d-143">If a cell containing SETATREF also contains SETATREFEXPR, the **FormulaChanged** event also fires for the cell containing SETATREF because a function parameter is changed.</span></span> 
  
<span data-ttu-id="9646d-144">Outros pontos importantes a serem observados sobre a função SETATREF são:</span><span class="sxs-lookup"><span data-stu-id="9646d-144">Other important points to note about the SETATREF function include the following:</span></span>
  
- <span data-ttu-id="9646d-145">As funções SETATREF podem encadear até 10 referências a outras funções SETATREF.</span><span class="sxs-lookup"><span data-stu-id="9646d-145">SETATREF functions can chain up to 10 references to other SETATREF functions.</span></span> 
    
- <span data-ttu-id="9646d-146">As células podem conter outras expressões além da função SETATREF, inclusive várias ocorrências de SETATREF em uma única célula.</span><span class="sxs-lookup"><span data-stu-id="9646d-146">Cells can contain other expressions in addition to the SETATREF function, including multiple occurrences of SETATREF in a single cell.</span></span>
    
- <span data-ttu-id="9646d-147">Se as formas estiverem coladas, o Visio segue a cadeia de referência SETATREF dentro da mesma planilha e coloca fórmulas de cola na célula referenciada.</span><span class="sxs-lookup"><span data-stu-id="9646d-147">If shapes are glued, Visio follows the SETATREF reference chain within the same sheet and places glue formulas in the referenced cell.</span></span> 
    
- <span data-ttu-id="9646d-148">A automação reconhece a função SETATREF e segue a cadeia de células referenciadas.</span><span class="sxs-lookup"><span data-stu-id="9646d-148">Automation recognizes the SETATREF function and follows the chain of referenced cells.</span></span> 
    
- <span data-ttu-id="9646d-149">Assim como GUARD, SETATREF não protege as células contra alterações feitas usando a função SETF na ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="9646d-149">Like GUARD, SETATREF does not protect cells from changes made by using the SETF function in the ShapeSheet.</span></span>
    
## <a name="example1"></a><span data-ttu-id="9646d-150">Example1</span><span class="sxs-lookup"><span data-stu-id="9646d-150">Example1</span></span>

<span data-ttu-id="9646d-151">Digamos que uma forma tem uma propriedade personalizada chamada Width, e a célula Width da seção Shape Transform contém a seguinte fórmula:</span><span class="sxs-lookup"><span data-stu-id="9646d-151">Let's say that a shape has a custom property called Width, and that the Width cell in the Shape Transform section contains the following formula:</span></span>
  
<span data-ttu-id="9646d-152">= SETATREF (prop. Width)</span><span class="sxs-lookup"><span data-stu-id="9646d-152">=SETATREF(Prop.Width)</span></span>
  
<span data-ttu-id="9646d-153">Se um usuário alterar a largura da forma na interface do usuário, o novo valor é atribuído à célula prop. Width, e não à célula Width na seção ShapeTransform; a fórmula na célula Width permanecerá inalterada.</span><span class="sxs-lookup"><span data-stu-id="9646d-153">If a user were to change the shape's width in the UI, the new value is assigned to the Prop.Width cell, not to the Width cell in the ShapeTransform section; the formula in the Width cell remains unchanged.</span></span> <span data-ttu-id="9646d-154">Você também pode definir a largura da forma usando os dados da forma.</span><span class="sxs-lookup"><span data-stu-id="9646d-154">You can also set the shape's width by using shape data.</span></span>
  
## <a name="example2"></a><span data-ttu-id="9646d-155">Example2</span><span class="sxs-lookup"><span data-stu-id="9646d-155">Example2</span></span>

<span data-ttu-id="9646d-p107">As soluções do Visio geralmente têm formas com uma relação hierárquica, o que faz com que as formas filhas movam quando uma forma pai é movida. A seguir, um exemplo de como você poderia gerenciar essa relação usando a função SETATREF na ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="9646d-p107">Visio solutions often have shapes that have a hierarchical relationship, requiring child shapes to move when a parent shape is moved. Following is an example of how you might manage this relationship using the SETATREF function in the ShapeSheet.</span></span> 
  
<span data-ttu-id="9646d-p108">As fórmulas a seguir estão na seção Shape Transform da forma filha. Além disso, definimos células do usuário chamadas User.DeltaX e User.DeltaY, que rastreiam a dimensão de deslocamento de ParentShape. Isso permite que a forma filha mova quando a forma pai é movida e também preserva a relação hierárquica se a forma filha é movida.</span><span class="sxs-lookup"><span data-stu-id="9646d-p108">The following formulas are contained in the Shape Transform section of the child shape. Also, we define user cells called User.DeltaX and User.DeltaY, which track the offset dimension from ParentShape. This allows the child shape to move when the parent shape is moved, and also to preserve the hierarchical relationship if the child shape is moved.</span></span>
  
<span data-ttu-id="9646d-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span><span class="sxs-lookup"><span data-stu-id="9646d-161">PinX =SETATREF(User.DeltaX, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinX)) + ParentShape!PinX</span></span>
  
<span data-ttu-id="9646d-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span><span class="sxs-lookup"><span data-stu-id="9646d-162">PinY =SETATREF(User.DeltaY, SETATREFEVAL(SETATREFEXPR() - ParentShape!PinY)) + ParentShape!PinY</span></span>
  
<span data-ttu-id="9646d-163">Quando a forma filha é movida usando a interface do usuário, os novos valores PinX e PinY são definidos como o parâmetro na função SETATREFEXPR.</span><span class="sxs-lookup"><span data-stu-id="9646d-163">When the child shape is moved using the UI, the new PinX and PinY values are set as the parameter in the SETATREFEXPR function.</span></span> <span data-ttu-id="9646d-164">A função SETATREF avalia a fórmula incluída no SETATREFEVAL e substitui PinX e PinY por seus resultados e, em seguida, a fórmula resultante é atribuída às células do usuário referenciadas na função SETATREF, User. DeltaX e User. DeltaY.</span><span class="sxs-lookup"><span data-stu-id="9646d-164">The SETATREF function evaluates the formula enclosed in SETATREFEVAL and replaces PinX and PinY with their results, and then the resulting formula is assigned to the user cells referenced in the SETATREF function—User.DeltaX and User.DeltaY.</span></span> <span data-ttu-id="9646d-165">Finalmente, os valores retornados por SETATREF (User.DeltaX ou User.DeltaY) são adicionados ao local do pino de ParentShape para calcular o local do pino da forma filha.</span><span class="sxs-lookup"><span data-stu-id="9646d-165">Lastly, the values returned by SETATREF (User.DeltaX or User.DeltaY) are added to the pin location of ParentShape to calculate the child shape's pin location.</span></span>
  

