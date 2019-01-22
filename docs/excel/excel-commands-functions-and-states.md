---
title: Estados, funções e comandos do Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- estados [Excel 2007],comandos [Excel 2007],funções de planilha [Excel 2007],funções de planilha de macro [Excel 2007],estados do Excel
ms.assetid: 20f19aa4-f184-47be-bcdd-7ded78778974
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: c941ba7445f1f0598bf044b5f177ad576df0137c
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716233"
---
# <a name="excel-commands-functions-and-states"></a><span data-ttu-id="fb59e-104">Estados, funções e comandos do Excel</span><span class="sxs-lookup"><span data-stu-id="fb59e-104">Excel Commands, Functions, and States</span></span>

 <span data-ttu-id="fb59e-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="fb59e-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="fb59e-106">O Microsoft Excel reconhece dois tipos bem distintos de funcionalidade adicionada: comandos e funções.</span><span class="sxs-lookup"><span data-stu-id="fb59e-106">Microsoft Excel recognizes two very different types of added functionality: commands and functions.</span></span>
  
## <a name="commands"></a><span data-ttu-id="fb59e-107">Comandos</span><span class="sxs-lookup"><span data-stu-id="fb59e-107">Commands</span></span>

<span data-ttu-id="fb59e-108">No Excel, os comandos têm as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="fb59e-108">In Excel, commands have the following characteristics:</span></span>
  
- <span data-ttu-id="fb59e-109">Realizam ações da mesma forma que os usuários.</span><span class="sxs-lookup"><span data-stu-id="fb59e-109">They perform actions in the same way that users do.</span></span>
    
- <span data-ttu-id="fb59e-110">Podem realizar as mesmas ações que um usuário (sujeito aos limites da interface usada), como alterar as configurações do Excel, abrir, fechar e editar documentos, iniciar recálculos e muito mais.</span><span class="sxs-lookup"><span data-stu-id="fb59e-110">They can do anything a user can do (subject to the limits of the interface used), such as altering Excel settings, opening, closing, and editing documents, initiating recalculations, and so on.</span></span>
    
- <span data-ttu-id="fb59e-111">Podem ser configurados para ser chamados quando certos eventos interceptados ocorrerem.</span><span class="sxs-lookup"><span data-stu-id="fb59e-111">They can be set up to be called when certain trapped events occur.</span></span>
    
- <span data-ttu-id="fb59e-112">Podem exibir caixas de diálogo e interagir com o usuário.</span><span class="sxs-lookup"><span data-stu-id="fb59e-112">They can display dialog boxes and interact with the user.</span></span>
    
- <span data-ttu-id="fb59e-113">Podem ser vinculados a objetos de controle para que sejam chamados quando alguma ação for executada nesse objeto, como clicar com o botão esquerdo do mouse.</span><span class="sxs-lookup"><span data-stu-id="fb59e-113">They can be linked to control objects so that they are called when some action is taken on that object, such as left-clicking.</span></span>
    
- <span data-ttu-id="fb59e-114">Nunca são chamados pelo Excel durante um recálculo.</span><span class="sxs-lookup"><span data-stu-id="fb59e-114">They are never called by Excel during a recalculation.</span></span>
    
- <span data-ttu-id="fb59e-115">Não podem ser chamados pela funções durante o recálculo.</span><span class="sxs-lookup"><span data-stu-id="fb59e-115">They cannot be called by functions during a recalculation.</span></span>
    
## <a name="functions"></a><span data-ttu-id="fb59e-116">Funções</span><span class="sxs-lookup"><span data-stu-id="fb59e-116">Functions</span></span>

<span data-ttu-id="fb59e-117">As ações no Excel realizam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="fb59e-117">Functions in Excel do the following:</span></span>
  
- <span data-ttu-id="fb59e-118">Geralmente usam argumentos e sempre retornam um resultado.</span><span class="sxs-lookup"><span data-stu-id="fb59e-118">They usually take arguments and always return a result.</span></span>
    
- <span data-ttu-id="fb59e-119">Podem ser inseridas em uma ou mais células como parte de uma fórmula do Excel.</span><span class="sxs-lookup"><span data-stu-id="fb59e-119">They can be entered into one or more cells as part of an Excel formula.</span></span>
    
- <span data-ttu-id="fb59e-120">Podem ser usadas em definições de nome definido.</span><span class="sxs-lookup"><span data-stu-id="fb59e-120">They can be used in defined name definitions.</span></span>
    
- <span data-ttu-id="fb59e-121">Podem ser usadas ​​em expressões de limite e limite de formatação condicional.</span><span class="sxs-lookup"><span data-stu-id="fb59e-121">They can be used in conditional formatting limit and threshold expressions.</span></span>
    
- <span data-ttu-id="fb59e-122">Podem ser chamadas pelos comandos.</span><span class="sxs-lookup"><span data-stu-id="fb59e-122">They can be called by commands.</span></span>
    
- <span data-ttu-id="fb59e-123">Não podem chamar comandos.</span><span class="sxs-lookup"><span data-stu-id="fb59e-123">They cannot call commands.</span></span>
    
<span data-ttu-id="fb59e-124">O Excel faz uma distinção adicional entre funções de planilha definidas pelo usuário e funções definidas pelo usuário que são projetadas para trabalhar em planilhas de macro.</span><span class="sxs-lookup"><span data-stu-id="fb59e-124">Excel makes a further distinction between user-defined worksheet functions and user-defined functions that are designed to work on macro sheets.</span></span> <span data-ttu-id="fb59e-125">O Excel não limita as funções de planilha de macro definidas pelo usuário somente para uso em planilhas de macro: essas funções podem ser usadas em qualquer lugar que uma função de planilha normal pode ser usada.</span><span class="sxs-lookup"><span data-stu-id="fb59e-125">Excel does not limit user-defined macro sheet functions only to being used on macro sheets: these functions can be used anywhere a normal worksheet function can be used.</span></span>
  
### <a name="worksheet-functions"></a><span data-ttu-id="fb59e-126">Funções de planilha</span><span class="sxs-lookup"><span data-stu-id="fb59e-126">Worksheet Functions</span></span>

<span data-ttu-id="fb59e-127">As seguintes condições são verdadeiras para as funções de planilha do Excel:</span><span class="sxs-lookup"><span data-stu-id="fb59e-127">The following is true of Excel worksheet functions:</span></span>
  
- <span data-ttu-id="fb59e-128">Não podem acessar as funções de informação de planilha de macro.</span><span class="sxs-lookup"><span data-stu-id="fb59e-128">They cannot access macro sheet information functions.</span></span>
    
- <span data-ttu-id="fb59e-129">Não podem obter os valores de células não calculadas.</span><span class="sxs-lookup"><span data-stu-id="fb59e-129">They cannot obtain the values of uncalculated cells.</span></span>
    
- <span data-ttu-id="fb59e-130">Podem ser criadas e registradas como thread-safe, começando no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="fb59e-130">They can be written and registered as thread-safe starting in Excel 2007.</span></span>
    
### <a name="macro-sheet-functions"></a><span data-ttu-id="fb59e-131">Funções de planilha de macro</span><span class="sxs-lookup"><span data-stu-id="fb59e-131">Macro-Sheet Functions</span></span>

<span data-ttu-id="fb59e-132">As seguintes condições são verdadeiras para as funções de planilha de macro do Excel:</span><span class="sxs-lookup"><span data-stu-id="fb59e-132">The following is true of Excel macro-sheet functions:</span></span>
  
- <span data-ttu-id="fb59e-133">Podem acessar as funções de informação de planilha de macro.</span><span class="sxs-lookup"><span data-stu-id="fb59e-133">They can access macro sheet information functions.</span></span>
    
- <span data-ttu-id="fb59e-134">Podem obter os valores de células não calculadas, inclusive os valores das células chamadas.</span><span class="sxs-lookup"><span data-stu-id="fb59e-134">They can obtain the values of uncalculated cells including the values of the calling cells.</span></span>
    
- <span data-ttu-id="fb59e-135">Não são consideradas thread-safe, começando no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="fb59e-135">They are not considered thread safe starting in Excel 2007.</span></span>
    
<span data-ttu-id="fb59e-136">Quando você registra a função, determina como o Excel trata uma UDF (função definida pelo usuário), o que permite que a função faça e como ela recalcula a função.</span><span class="sxs-lookup"><span data-stu-id="fb59e-136">How Excel treats a user-defined function (UDF), what it permits the function to do, and how it recalculates the function are all determined when you register the function.</span></span> <span data-ttu-id="fb59e-137">Se uma função for registrada como uma função de planilha, mas tenta fazer algo que somente uma função de planilha de macro pode fazer, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="fb59e-137">If a function is registered as a worksheet function but tries to do something that only a macro-sheet function can do, the operation fails.</span></span> <span data-ttu-id="fb59e-138">Desde o Excel 2007, se uma função de planilha registrada como thread-safe tentar chamar uma função de planilha de macro, novamente, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="fb59e-138">Starting in Excel 2007, if a worksheet function registered as thread safe tries to call a macro sheet function, again, the operation fails.</span></span>
  
<span data-ttu-id="fb59e-139">O Excel trata as UDFs do VBA (Microsoft Visual Basic for Applications) como funções equivalentes a planilhas de macro, pois elas podem acessar informações de espaço de trabalho e o valor de células não calculadas, e não são consideradas como thread-safe desde o Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="fb59e-139">Excel treats Microsoft Visual Basic for Applications (VBA) UDFs as macro sheet-equivalent functions, in that they can access workspace information and the value of uncalculated cells, and they are not considered as thread safe starting in Excel 2007.</span></span>
  
## <a name="excel-states"></a><span data-ttu-id="fb59e-140">Estados do Excel</span><span class="sxs-lookup"><span data-stu-id="fb59e-140">Excel States</span></span>

<span data-ttu-id="fb59e-141">O Excel pode estar em um dos vários estados a qualquer momento, dependendo das ações do usuário, de um processo externo, de um evento interceptado executando uma macro ou de um evento de manutenção do Excel, como **Salvamento Automático**.</span><span class="sxs-lookup"><span data-stu-id="fb59e-141">Excel can be in one of a number of states at any given time depending on the actions of the user, an external process, a trapped event running a macro, or a timed Excel housekeeping event such as **Autosave**.</span></span>
  
<span data-ttu-id="fb59e-142">Os estados experimentados pelo usuário são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="fb59e-142">The states that the user experiences are as follows:</span></span>
  
- <span data-ttu-id="fb59e-143">**Estado Pronto:** nenhum comando ou macro está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="fb59e-143">**Ready state:** No commands or macros are being run.</span></span> <span data-ttu-id="fb59e-144">Nenhuma caixa de diálogo está sendo exibida.</span><span class="sxs-lookup"><span data-stu-id="fb59e-144">No dialog boxes are being displayed.</span></span> <span data-ttu-id="fb59e-145">Nenhuma célula está sendo editada e o usuário não está no meio de uma operação de recortar/copiar e colar.</span><span class="sxs-lookup"><span data-stu-id="fb59e-145">No cells are being edited and the user is not in the middle of a cut/copy and paste operation.</span></span> <span data-ttu-id="fb59e-146">Nenhum objeto inserido está focado.</span><span class="sxs-lookup"><span data-stu-id="fb59e-146">No embedded object has focus.</span></span> 
    
- <span data-ttu-id="fb59e-147">**Modo Editar:** o usuário começou a digitar caracteres de entrada válidos em uma célula desbloqueada ou desprotegida, ou pressionou **F2** em uma ou mais células desbloqueadas ou desprotegidas.</span><span class="sxs-lookup"><span data-stu-id="fb59e-147">**Edit mode:** The user has started to type valid input characters into an unlocked or unprotected cell, or has pressed **F2** on one or more unlocked or unprotected cells.</span></span> 
    
- <span data-ttu-id="fb59e-148">**Modo Recortar/copiar e colar:** o usuário recortou ou copiou uma célula ou um intervalo de células e ainda não colou, ou colou usando a caixa de diálogo especial de colagem, que permite várias operações de colagem.</span><span class="sxs-lookup"><span data-stu-id="fb59e-148">**Cut/copy and paste mode:** The user has cut or copied a cell or range of cells and has not yet pasted them, or has pasted them using the paste-special dialog box, which enables multiple paste operations.</span></span> 
    
- <span data-ttu-id="fb59e-149">**Modo Apontar:** o usuário está editando uma fórmula e selecionando células cujos endereços são adicionados à fórmula que está sendo editada.</span><span class="sxs-lookup"><span data-stu-id="fb59e-149">**Point mode:** The user is editing a formula and is selecting cells whose addresses are added to the formula being edited.</span></span> 
    
<span data-ttu-id="fb59e-150">O usuário pode limpar os modos Editar, Apontar e Recortar/copiar pressionando a tecla **ESC**, que retorna o Excel ao estado pronto.</span><span class="sxs-lookup"><span data-stu-id="fb59e-150">The user can clear the edit, point, and cut/copy modes by pressing the **ESC** key, which returns Excel to its ready state.</span></span> <span data-ttu-id="fb59e-151">Outros eventos podem limpar esses estados, como:</span><span class="sxs-lookup"><span data-stu-id="fb59e-151">Other events can clear these states, such as the following:</span></span> 
  
- <span data-ttu-id="fb59e-152">O usuário abre uma caixa de diálogo interna.</span><span class="sxs-lookup"><span data-stu-id="fb59e-152">The user opens a built-in dialog box.</span></span>
    
- <span data-ttu-id="fb59e-153">O usuário inicia um recálculo.</span><span class="sxs-lookup"><span data-stu-id="fb59e-153">The user initiates sharing a Sway.</span></span>
    
- <span data-ttu-id="fb59e-154">O usuário executa um comando.</span><span class="sxs-lookup"><span data-stu-id="fb59e-154">The user runs a command.</span></span>
    
- <span data-ttu-id="fb59e-155">O Excel executa uma operação de **Salvamento Automático**.</span><span class="sxs-lookup"><span data-stu-id="fb59e-155">Excel performs an **Autosave** operation.</span></span> 
    
- <span data-ttu-id="fb59e-156">Um evento de temporizador é interceptado.</span><span class="sxs-lookup"><span data-stu-id="fb59e-156">A timer event is trapped.</span></span>
    
<span data-ttu-id="fb59e-157">O último exemplo é importante para os desenvolvedores de suplementos.</span><span class="sxs-lookup"><span data-stu-id="fb59e-157">The last example is of importance to add-in developers.</span></span> <span data-ttu-id="fb59e-158">Você deve considerar o impacto da usabilidade normal do Excel, em que as interceptações de eventos de temporizador frequentes estão sendo definidas e executadas.</span><span class="sxs-lookup"><span data-stu-id="fb59e-158">You should consider the impact of the normal usability of Excel where frequent timer event traps are being set and executed.</span></span> <span data-ttu-id="fb59e-159">Quando essa for uma parte importante da funcionalidade de seu suplemento, ofereça aos usuários uma forma facilmente acessível de suspendê-la, para que eles possam recortar/copiar e colar normalmente quando precisarem.</span><span class="sxs-lookup"><span data-stu-id="fb59e-159">When this is an important part of your add-in's functionality, you should provide users with an easily accessible way of suspending it, so that they can cut/copy and paste normally when they need to.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fb59e-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb59e-160">See also</span></span>



[<span data-ttu-id="fb59e-161">Conceitos de programação do Excel</span><span class="sxs-lookup"><span data-stu-id="fb59e-161">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
  
[<span data-ttu-id="fb59e-162">Permitir intervenções de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="fb59e-162">Permitting user breaks in lengthy operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)

