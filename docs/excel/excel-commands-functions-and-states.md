---
title: Comandos, funções e estados do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- estados [excel 2007], [Excel 2007] de comandos, funções de planilha [Excel 2007], funções de folha de macro [Excel 2007], Estados do Excel
localization_priority: Normal
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 60977216663fb2492f425a9b7c855b77815f0e7b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765294"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="2ecaf-104">Comandos, funções e estados do Excel</span><span class="sxs-lookup"><span data-stu-id="2ecaf-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="2ecaf-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2ecaf-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2ecaf-106">O Microsoft Excel reconhece dois tipos de funcionalidade adicionada muito diferentes: as funções e comandos.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="2ecaf-107">Comandos</span><span class="sxs-lookup"><span data-stu-id="2ecaf-107">Commands</span></span>

<span data-ttu-id="2ecaf-108">No Excel, comandos têm as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="2ecaf-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="2ecaf-109">Eles realizar ações da mesma forma que os usuários fazem.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="2ecaf-110">Eles podem fazer qualquer coisa que um usuário pode fazer (assunto para os limites da interface utilizados), como alterar as configurações do Excel, abertura, fechamento e editando documentos, iniciando recálculos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="2ecaf-111">Eles podem ser configurados para ser chamados quando ocorrerem determinados eventos capturados.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="2ecaf-112">Eles podem exibir caixas de diálogo e interagir com o usuário.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="2ecaf-113">Eles podem ser vinculados para controlar objetos para que eles são chamados quando alguma ação seja executada nesse objeto, como o mouse.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="2ecaf-114">Eles nunca são chamados pelo Excel durante um recálculo.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="2ecaf-115">Eles não podem ser chamados pelas funções durante um recálculo.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="2ecaf-116">Funções</span><span class="sxs-lookup"><span data-stu-id="2ecaf-116">Functions</span></span>

<span data-ttu-id="2ecaf-117">Funções do Excel faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2ecaf-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="2ecaf-118">Eles geralmente levam argumentos e sempre retornam um resultado.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="2ecaf-119">Eles podem ser inseridos em uma ou mais células como parte de uma fórmula do Excel.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="2ecaf-120">Eles podem ser usados em definições do nome definido.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="2ecaf-121">Eles podem ser usados em expressões de limite e de limite de formatação condicional.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="2ecaf-122">Eles podem ser chamados pelos comandos.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="2ecaf-123">Eles não é possível chamar comandos.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-123">They cannot call commands.</span></span>
    
<span data-ttu-id="2ecaf-124">Excel faz outra distinção entre funções de planilha definidas pelo usuário e as funções definidas pelo usuário são projetadas para trabalhar em folhas de macro.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-124">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets.</span></span> <span data-ttu-id="2ecaf-125">Excel não limitam as funções de planilha de macro definida pelo usuário apenas a que está sendo usado em folhas de macro: essas funções podem ser usadas em qualquer lugar, uma função de planilha normal pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-125">Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="2ecaf-126">Funções de Planilha</span><span class="sxs-lookup"><span data-stu-id="2ecaf-126">Worksheet Functions</span></span>

<span data-ttu-id="2ecaf-127">O exemplo a seguir for verdadeira das funções de planilha do Excel:</span><span class="sxs-lookup"><span data-stu-id="2ecaf-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="2ecaf-128">Eles não podem acessar as funções de informações de folha de macro.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="2ecaf-129">Eles não podem obter os valores das células não calculadas.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="2ecaf-130">Eles podem ser gravados e registrados como thread-safe iniciando no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="2ecaf-131">Funções de folha de macro</span><span class="sxs-lookup"><span data-stu-id="2ecaf-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="2ecaf-132">O exemplo a seguir for verdadeira das funções de folha de macro do Excel:</span><span class="sxs-lookup"><span data-stu-id="2ecaf-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="2ecaf-133">Eles podem acessar as funções de informações de folha de macro.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="2ecaf-134">Eles podem obter os valores das células não calculadas, incluindo os valores das células da chamada.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="2ecaf-135">Eles não são considerados thread seguros iniciada no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="2ecaf-136">Como o Excel trata uma função definida pelo usuário (UDF), o que permite a função fazer e como ele recalcula a função são determinados tudo ao registrar a função.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-136">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function.</span></span> <span data-ttu-id="2ecaf-137">Se uma função está registrada como uma função de planilha, mas tenta fazer algo que apenas uma função de folha de macro pode fazer, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-137">If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails.</span></span> <span data-ttu-id="2ecaf-138">Iniciando no Excel 2007, se uma função de planilha registrada como thread-safe tenta chamar uma função de folha de macro, novamente, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-138">Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="2ecaf-139">Excel trata do Microsoft Visual Basic for Applications (VBA) UDFs como funções equivalente a folha de macro, em que eles possam acessar informações de espaço de trabalho e o valor das células não calculadas e eles não são considerados como thread iniciando seguros no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="2ecaf-140">Estados do Excel</span><span class="sxs-lookup"><span data-stu-id="2ecaf-140">Excel States</span></span>

<span data-ttu-id="2ecaf-141">Excel pode estar em um dos vários estados a qualquer momento determinado, dependendo das ações do usuário, um processo externo, um evento capturado executando uma macro ou um evento de manutenção do sistema do Excel cronometrado como **salvamento automático**.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="2ecaf-142">Os estados de experiências de usuário são:</span><span class="sxs-lookup"><span data-stu-id="2ecaf-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="2ecaf-143">**Estado está pronto:** Não há comandos ou macros estão sendo executadas.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-143">**Ready state:** No commands or macros are being run.</span></span> <span data-ttu-id="2ecaf-144">Sem caixas de diálogo estiver sendo exibidas.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-144">No dialog boxes are being displayed.</span></span> <span data-ttu-id="2ecaf-145">Nenhuma célula estiver sendo editada e o usuário não estiver no meio de uma operação de Recortar/copiar e colar.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-145">No cells are being edited and the user is not in the middle of a cut/copy and paste operation.</span></span> <span data-ttu-id="2ecaf-146">Nenhum objeto incorporado tem o foco.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-146">No embedded object has focus.</span></span> 
    
- <span data-ttu-id="2ecaf-147">**Modo de edição:** O usuário foi iniciada digitar caracteres válidos de entrada em uma célula desbloqueada ou desprotegida ou pressionou **F2** em uma ou mais células desbloqueadas ou desprotegidas.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="2ecaf-148">**Modo Recortar/copiar e colar:** O usuário tem recortado ou copiado de uma célula ou intervalo de células e tem não ainda coladas-los ou tem colado-los usando a caixa de diálogo Colar especial, que permite que várias operações de colagem.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="2ecaf-149">**Modo ponto:** O usuário está editando uma fórmula e está selecionando células cujos endereços são adicionados à fórmula está sendo editada.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="2ecaf-150">O usuário pode desmarcar a editar, ponto e modos de Recortar/copiar pressionando a tecla **ESC** , que retorna o Excel ao estado pronto.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-150">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state.</span></span> <span data-ttu-id="2ecaf-151">Outros eventos podem limpar desses estados, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2ecaf-151">Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="2ecaf-152">O usuário abre uma caixa de diálogo interna.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="2ecaf-153">O usuário inicia um recálculo.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-153">The user initiates a recalculation.</span></span>
    
- <span data-ttu-id="2ecaf-154">O usuário executa um comando.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-154">The user runs a command.</span></span>
    
- <span data-ttu-id="2ecaf-155">Excel executa uma operação de **salvamento automático** .</span><span class="sxs-lookup"><span data-stu-id="2ecaf-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="2ecaf-156">Um evento timer é interceptado.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="2ecaf-157">O exemplo a último é de importância ao suplemento desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-157">The last example is of importance to add-in developers.</span></span> <span data-ttu-id="2ecaf-158">Você deve considerar o impacto da usabilidade normal do Excel em que intercepta o evento timer frequente estão sendo definidos e executadas.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-158">You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed.</span></span> <span data-ttu-id="2ecaf-159">Quando isso é uma parte importante do funcionalidade da seu suplemento, você deve fornecer aos usuários uma maneira podem ser acessada facilmente de suspendendo, para que eles podem Recortar/copiar e colar, normalmente, quando eles precisam.</span><span class="sxs-lookup"><span data-stu-id="2ecaf-159">When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ecaf-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ecaf-160">See also</span></span>



[<span data-ttu-id="2ecaf-161">Excel Programming Concepts</span><span class="sxs-lookup"><span data-stu-id="2ecaf-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="2ecaf-162">Quebras de autorizações de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="2ecaf-162">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

