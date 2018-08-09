---
title: Função CALLTHIS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251403
localization_priority: Normal
ms.assetid: 461abfc1-d2cc-2354-1c2f-395c9e351a78
description: Chama um procedimento em um Microsoft Visual Basic para o project Applications (VBA).
ms.openlocfilehash: 04065384453e55b745daa89273fb4c23b32fb90c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771432"
---
# <a name="callthis-function"></a><span data-ttu-id="c5ac0-103">Função CALLTHIS</span><span class="sxs-lookup"><span data-stu-id="c5ac0-103">CALLTHIS Function</span></span>

<span data-ttu-id="c5ac0-104">Chama um procedimento em um Microsoft Visual Basic para o project Applications (VBA).</span><span class="sxs-lookup"><span data-stu-id="c5ac0-104">Calls a procedure in a Microsoft Visual Basic for Applications (VBA) project.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c5ac0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5ac0-105">Syntax</span></span>

<span data-ttu-id="c5ac0-106">CALLTHIS ("* * *procedimento* * *", ["* * *project* * *"], [* * *arg1* * *, * * *arg2* * *,...])</span><span class="sxs-lookup"><span data-stu-id="c5ac0-106">CALLTHIS(" ** *procedure* ** ",[" ** *project* ** "],[ ** *arg1* **, ** *arg2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c5ac0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5ac0-107">Parameters</span></span>

|<span data-ttu-id="c5ac0-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c5ac0-108">**Name**</span></span>|<span data-ttu-id="c5ac0-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="c5ac0-109">**Required/Optional**</span></span>|<span data-ttu-id="c5ac0-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c5ac0-110">**Data Type**</span></span>|<span data-ttu-id="c5ac0-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c5ac0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c5ac0-112">_procedimento_</span><span class="sxs-lookup"><span data-stu-id="c5ac0-112">_procedure_</span></span> <br/> |<span data-ttu-id="c5ac0-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c5ac0-113">Required</span></span>  <br/> |<span data-ttu-id="c5ac0-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c5ac0-114">**String**</span></span> <br/> | <span data-ttu-id="c5ac0-115">O nome do procedimento a ser chamado.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-115">The name of the procedure to call.</span></span>  <br/> |
| <span data-ttu-id="c5ac0-116">_Project_</span><span class="sxs-lookup"><span data-stu-id="c5ac0-116">_project_</span></span> <br/> |<span data-ttu-id="c5ac0-117">Opcional</span><span class="sxs-lookup"><span data-stu-id="c5ac0-117">Optional</span></span>  <br/> |<span data-ttu-id="c5ac0-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c5ac0-118">**String**</span></span> <br/> |<span data-ttu-id="c5ac0-119">O projeto que contém o procedimento.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-119">The project that contains the procedure.</span></span>  <br/> |
| <span data-ttu-id="c5ac0-120">_arg_</span><span class="sxs-lookup"><span data-stu-id="c5ac0-120">_arg_</span></span> <br/> |<span data-ttu-id="c5ac0-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="c5ac0-121">Optional</span></span>  <br/> |<span data-ttu-id="c5ac0-122">**Número, Cadeia de Caracteres, Data ou Moeda**</span><span class="sxs-lookup"><span data-stu-id="c5ac0-122">**Number, String, Date, or Currency**</span></span> <br/> |<span data-ttu-id="c5ac0-123">Passados como parâmetros para o procedimento.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-123">Passed as parameters to the procedure.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c5ac0-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5ac0-124">Remarks</span></span>

<span data-ttu-id="c5ac0-125">No projeto VBA, o *procedimento* é definida da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="c5ac0-125">In the VBA project,  *procedure*  is defined as follows:</span></span> 
  
<span data-ttu-id="c5ac0-126">procedimento (*vsoshape as* Visio. Shape [arg1 As type, arg2 As type...])</span><span class="sxs-lookup"><span data-stu-id="c5ac0-126">procedure(*vsoShape*  As Visio.Shape [arg1 As type, arg2 As type...])</span></span> 
  
<span data-ttu-id="c5ac0-127">onde *vsoshape as* é uma referência ao objeto **Shape** que contém a fórmula CALLTHIS sendo avaliada e _arg1_, *arg2* ... são os argumentos especificados na fórmula.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-127">where  *vsoShape*  is a reference to the **Shape** object that contains the CALLTHIS formula being evaluated, and  _arg1_,  *arg2*  ... are the arguments specified in that formula.</span></span> 
  
<span data-ttu-id="c5ac0-128">Observe que *vsoshape as* é muito parecido com o argumento "this" passado a um procedimento de membro C++; daí o nome "CALLTHIS."</span><span class="sxs-lookup"><span data-stu-id="c5ac0-128">Notice that  *vsoShape*  is very much like the "this" argument passed to a C++ member procedure; hence the name "CALLTHIS."</span></span> <span data-ttu-id="c5ac0-129">Na verdade, uma célula que contém uma fórmula que inclui CALLTHIS pode ser lido como "Chamar esse procedimento e passe uma referência para a minha forma".</span><span class="sxs-lookup"><span data-stu-id="c5ac0-129">In effect, a cell that contains a formula that includes CALLTHIS can be read as, "Call this procedure and pass it a reference to my shape."</span></span> 
  
<span data-ttu-id="c5ac0-130">Se o _projeto_ for especificado, o Microsoft Visio verifica todos os documentos abertos para o um contendo _project_ e chamadas de _procedimento_ no projeto.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-130">If  _project_ is specified, Microsoft Visio scans all open documents for the one containing  _project_ and calls  _procedure_ in that project.</span></span> <span data-ttu-id="c5ac0-131">Se o _projeto_ for omitido ou nulo (""), Visio pressupõe que o _procedimento_ está no projeto VBA do documento que contém a fórmula CALLTHIS que está sendo avaliada.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-131">If  _project_ is omitted or null (""), Visio assumes  _procedure_ is in the VBA project of the document that contains the CALLTHIS formula that is being evaluated.</span></span> 
  
<span data-ttu-id="c5ac0-132">Números em _arg1_, _arg2 …_ são passados em unidades externas.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-132">Numbers in  _arg1_,  _arg2..._ are passed in external units.</span></span> <span data-ttu-id="c5ac0-133">Por exemplo, se você passar o valor da célula Height de uma forma que é 3 centímetros de altura, 3 é passado.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-133">For example, if you pass the value of the Height cell from a shape that is 3 cm tall, 3 is passed.</span></span> <span data-ttu-id="c5ac0-134">Para passar unidades diferentes com um número, use a função FORMATEX ou force explicitamente as unidades adicionando um par de unidade numérica nulo, por exemplo, 0 pés + altura.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-134">To pass different units with a number, use the FORMATEX function or explicitly coerce units by adding a null number-unit pair, for example, 0 ft + Height.</span></span> 
  
<span data-ttu-id="c5ac0-135">A segunda vírgula na função CALLTHIS é opcional.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-135">The second comma in the CALLTHIS function is optional.</span></span> <span data-ttu-id="c5ac0-136">Ela corresponde ao número de parâmetros adicionais adicionados ao procedimento.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-136">It corresponds to the number of additional parameters added to your procedure.</span></span> <span data-ttu-id="c5ac0-137">Se você não usa nenhum parâmetro adicional, exceto `(vsoShape as Visio.Shape)` , não adicione a segunda vírgula; Use CALLTHIS("",).</span><span class="sxs-lookup"><span data-stu-id="c5ac0-137">If you do not use any additional parameters, except  `(vsoShape as Visio.Shape)` , do not add the second comma; use CALLTHIS("",).</span></span> <span data-ttu-id="c5ac0-138">Se você adicionar dois parâmetros adicionais, por exemplo, use CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-138">If you add two additional parameters, for example, use CALLTHIS("",,,).</span></span> 
  
<span data-ttu-id="c5ac0-139">A função CALLTHIS sempre avalia como 0, e a chamada para o _procedimento_ ocorre durante o tempo ocioso após a conclusão do processo de recálculo.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-139">The CALLTHIS function always evaluates to 0, and the call to  _procedure_ occurs during idle time after the recalculation process finishes.</span></span>  <span data-ttu-id="c5ac0-140">_Procedimento_ pode retornar um valor, mas ignorado pelo Visio.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-140">_Procedure_ can return a value, but Visio ignores it.</span></span>  <span data-ttu-id="c5ac0-141">_Procedimento_ retorna um valor que o Visio pode reconhecer, definindo o resultado da outra célula ou uma fórmula no documento, mas não para a célula que chamou o _procedimento_, a menos que você deseja substituir a fórmula CALLTHIS.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-141">_Procedure_ returns a value that Visio can recognize by setting the formula or result of another cell in the document, but not the cell that called  _procedure_, unless you want to overwrite the CALLTHIS formula.</span></span>
  
<span data-ttu-id="c5ac0-142">A função CALLTHIS difere da função RUNADDON no sentido de que o projeto de um documento não precisa fazer referência a um outro projeto para chamar esse projeto.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-142">The CALLTHIS function differs from the RUNADDON function in that a document's project does not need to reference another project in order to call into that project.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="c5ac0-143">O código VBA, que é invocado quando a instância do Visio avalia uma função CALLTHIS em uma fórmula, não deve fechar o documento que contém a célula que está usando a função, uma vez que ocorrerá um erro de aplicativo e o Visio será fechado.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-143">VBA code that is invoked when the Visio instance evaluates a CALLTHIS function in a formula should not close the document containing the cell using the function because an application error results and Visio terminates.</span></span> 
  
<span data-ttu-id="c5ac0-144">Se você precisar fechar o documento que contém a célula que está utilizando a função CALLTHIS, utilize uma das técnicas a seguir:</span><span class="sxs-lookup"><span data-stu-id="c5ac0-144">If you need to close the document containing the cell that uses the CALLTHIS function, use one of the following techniques:</span></span> 
  
- <span data-ttu-id="c5ac0-145">Feche o documento a partir de um código que não seja VBA.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-145">Close the document from code that is not VBA.</span></span>
    
- <span data-ttu-id="c5ac0-146">Feche o documento a partir de um projeto diferente do que está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-146">Close the document from a project other than the one that is closing.</span></span>
    
- <span data-ttu-id="c5ac0-147">Envie mensagens de janela para fechar as janelas em vez de fechar o documento.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-147">Post window messages to close windows in the document rather than closing the document.</span></span>
    
<span data-ttu-id="c5ac0-148">Para obter mais informações sobre a execução de códigos no Visio, consulte [Sobre configurações de segurança e execução de códigos no Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) nesta Referência da ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-148">For more information about running code in Visio, see [About Security Settings and Running Code in Visio](about-security-settings-and-running-code-in-visio-shapesheet.md) in this ShapeSheet Reference.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c5ac0-149">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5ac0-149">Example 1</span></span>

<span data-ttu-id="c5ac0-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span><span class="sxs-lookup"><span data-stu-id="c5ac0-150">CALLTHIS("p",,FORMATEX(Height,"#.00 u",,"cm"))</span></span>
  
<span data-ttu-id="c5ac0-151">Chamará o procedimento p, localizado em um módulo, e passará o valor de altura em centímetros, como 7,62 cm.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-151">Calls the procedure named p located in a module and passes the value of Height in centimeters, such as 7.62 cm.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c5ac0-152">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c5ac0-152">Example 2</span></span>

<span data-ttu-id="c5ac0-153">CALLTHIS("q",,0 cm+Height,Width)</span><span class="sxs-lookup"><span data-stu-id="c5ac0-153">CALLTHIS("q",,0 cm+Height,Width)</span></span>
  
<span data-ttu-id="c5ac0-154">Chamará o procedimento q, localizado em um módulo, e passará a altura da célula em centímetros e a largura em unidades internas.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-154">Calls the procedure named q located in a module and passes the cell's height in centimeters and width in internal units.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c5ac0-155">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c5ac0-155">Example 3</span></span>

<span data-ttu-id="c5ac0-156">Use o procedimento a seguir no módulo de classe *ThisDocument* .</span><span class="sxs-lookup"><span data-stu-id="c5ac0-156">Use the following procedure in the  *ThisDocument*  class module.</span></span> 
  
<span data-ttu-id="c5ac0-157">Utilize uma das sintaxes a seguir na célula EventDblClick de uma forma com os procedimentos descritos anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c5ac0-157">Use any of the following syntax in a shape's EventDblClick cell with the preceding procedures.</span></span>
  
<span data-ttu-id="c5ac0-158">CALLTHIS("ThisDocument.A",)</span><span class="sxs-lookup"><span data-stu-id="c5ac0-158">CALLTHIS("ThisDocument.A",)</span></span>
  
<span data-ttu-id="c5ac0-159">CALLTHIS("ThisDocument.B",,"Click")</span><span class="sxs-lookup"><span data-stu-id="c5ac0-159">CALLTHIS("ThisDocument.B",,"Click")</span></span>
  
<span data-ttu-id="c5ac0-160">CALLTHIS("Este documento.C",,"Clique", " OK.")</span><span class="sxs-lookup"><span data-stu-id="c5ac0-160">CALLTHIS("ThisDocument.C",,"Click", " OK.")</span></span>
  

