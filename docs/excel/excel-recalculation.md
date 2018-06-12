---
title: Recálculo do Excel
manager: kelbow
ms.date: 03/09/2018
ms.audience: Developer
ms.topic: overview
keywords:
- cálculo de forçado [excel 2007], recálculo seletivo [Excel 2007], funções voláteis, cálculo de [Excel 2007], modos, células recalculadas [Excel 2007], [Excel 2007], a dependência especificado cálculo de planilha [Excel 2007], recálculo [Excel 2007 ], reconstrução de árvore da pasta de trabalho [Excel 2007], [Excel 2007], [de funções não voláteis de células de recálculo do Excel, funções voláteis [Excel 2007], funções de cálculo de planilha não voláteis, active [Excel 2007], [Excel 2007], dirty de cálculo de intervalo [Excel 2007] Excel 2007], forçado recálculo [Excel 2007]
localization_priority: Normal
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 9964f2c4282158e83891d82ba43fa19f23ab1eb6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765336"
---
# <a name="excel-recalculation"></a><span data-ttu-id="8fdb3-104">Recálculo do Excel</span><span class="sxs-lookup"><span data-stu-id="8fdb3-104">Excel Recalculation</span></span>

 <span data-ttu-id="8fdb3-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8fdb3-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8fdb3-106">O usuário pode disparar o recálculo no Microsoft Excel de várias maneiras, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="8fdb3-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="8fdb3-107">Inserir novos dados (se o Excel está no modo de recálculo automático, descrito mais adiante neste tópico).</span><span class="sxs-lookup"><span data-stu-id="8fdb3-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="8fdb3-108">Instruindo explicitamente Excel recalcule todo ou parte de uma pasta de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="8fdb3-109">A exclusão ou inserir uma linha ou coluna.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="8fdb3-110">Salvando uma pasta de trabalho enquanto o **Recalcular antes de salvar** a opção é definida.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="8fdb3-111">A execução de determinadas ações Autofilter.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="8fdb3-112">Clicando duas vezes em um divisor de coluna ou linha (no modo de cálculo automático).</span><span class="sxs-lookup"><span data-stu-id="8fdb3-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="8fdb3-113">Adicionando, editando ou excluindo um nome definido.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="8fdb3-114">Renomear uma planilha.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="8fdb3-115">Alterar a posição de uma planilha em relação a outras planilhas.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="8fdb3-116">Ocultar ou Mostrar linhas, mas não de colunas.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="8fdb3-117">Este tópico não faz distinção entre o usuário diretamente pressionando uma tecla ou clicando o mouse e essas tarefas que está sendo feitas por um comando ou uma macro.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-117">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro.</span></span> <span data-ttu-id="8fdb3-118">O usuário executa o comando ou faz algo para fazer com que o comando seja executado para que ela ainda será considerada uma ação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-118">The user runs the command, or does something to cause the command to run so that it is still considered a user action.</span></span> <span data-ttu-id="8fdb3-119">Portanto, a frase "usuário" significa também ", o usuário ou um comando ou processo iniciado pelo usuário."</span><span class="sxs-lookup"><span data-stu-id="8fdb3-119">Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="8fdb3-120">A dependência, células Dirty e células recalculadas</span><span class="sxs-lookup"><span data-stu-id="8fdb3-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="8fdb3-121">Cálculo de planilhas do Excel pode ser exibido como um processo de três estágios:</span><span class="sxs-lookup"><span data-stu-id="8fdb3-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="8fdb3-122">Construção de uma árvore de dependência</span><span class="sxs-lookup"><span data-stu-id="8fdb3-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="8fdb3-123">Construção de uma cadeia de cálculo</span><span class="sxs-lookup"><span data-stu-id="8fdb3-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="8fdb3-124">Recálculo de células</span><span class="sxs-lookup"><span data-stu-id="8fdb3-124">Recalculation of cells</span></span>
    
<span data-ttu-id="8fdb3-125">A árvore de dependência informa sobre quais células dependem do que outros recursos do Excel ou maneira equivalente, quais células são precedentes para que outros recursos.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-125">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others.</span></span> <span data-ttu-id="8fdb3-126">Na árvore de, Excel constrói uma cadeia de cálculo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-126">From this tree, Excel constructs a calculation chain.</span></span> <span data-ttu-id="8fdb3-127">A cadeia de cálculo lista todas as células que contêm fórmulas na ordem na qual deve ser calculados.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-127">The calculation chain lists all the cells that contain formulas in the order in which they should be calculated.</span></span> <span data-ttu-id="8fdb3-128">Durante o recálculo, o Excel revisa essa cadeia se encontrar uma fórmula que depende de uma célula que ainda não foi calculada.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-128">During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated.</span></span> <span data-ttu-id="8fdb3-129">Nesse caso, a célula que está sendo calculada e seus dependentes são movidos para baixo a cadeia.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-129">In this case, the cell that is being calculated and its dependents are moved down the chain.</span></span> <span data-ttu-id="8fdb3-130">Por esse motivo, os tempos de cálculo geralmente podem melhorar em uma planilha que acabou foi aberta em alguns ciclos de cálculo da primeiro.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-130">For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="8fdb3-131">Quando uma alteração estrutural é feita de uma pasta de trabalho, por exemplo, quando uma nova fórmula é inserida, o Excel reconstrói a cadeia de cálculo e a árvore de dependência.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-131">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain.</span></span> <span data-ttu-id="8fdb3-132">Quando novos dados ou novas fórmulas são inseridas, Excel marcará todas as células que dependem de novos dados como precisam de recálculo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-132">When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation.</span></span> <span data-ttu-id="8fdb3-133">As células que são marcadas dessa forma são conhecidas como *sujo* .</span><span class="sxs-lookup"><span data-stu-id="8fdb3-133">Cells that are marked in this way are known as  *dirty*  .</span></span> <span data-ttu-id="8fdb3-134">Todos os dependentes diretos e indiretos são marcados como sujo para que se B1 depende A1 e C1 depende B1, quando A1 é alterada, B1 e C1 estão marcado como sujo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-134">All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="8fdb3-135">Se uma célula depende, direta ou indiretamente, em si, o Excel detecta a referência circular e avisa o usuário.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-135">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user.</span></span> <span data-ttu-id="8fdb3-136">Normalmente, isso é uma condição de erro que o usuário deve corrigir e Excel fornece ferramentas muito úteis de gráficas e de navegação para ajudar o usuário para localizar a origem da dependência circular.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-136">This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency.</span></span> <span data-ttu-id="8fdb3-137">Em alguns casos, você pode querer deliberadamente essa condição de existir.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-137">In some cases, you might deliberately want this condition to exist.</span></span> <span data-ttu-id="8fdb3-138">Por exemplo, talvez você queira executar um cálculo repetitivo onde o ponto de partida para a próxima iteração é o resultado da iteração anterior.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-138">For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration.</span></span> <span data-ttu-id="8fdb3-139">Excel suporta controle de cálculos repetitivo através da caixa de diálogo de opções de cálculo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-139">Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="8fdb3-140">Depois de marcar células como sujo, quando um recálculo é feito em seguida, o Excel revê o conteúdo de cada célula dirty na ordem ditada pela cadeia de cálculo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-140">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain.</span></span> <span data-ttu-id="8fdb3-141">No exemplo fornecido anteriormente, isso significa que B1 é o primeiro e, em seguida, C1.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-141">In the example given earlier, this means B1 is first, and then C1.</span></span> <span data-ttu-id="8fdb3-142">Este recálculo ocorre imediatamente após o Excel concluir a marcação de células como sujo se o modo de recálculo é automático; Caso contrário, ele ocorre posteriormente.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-142">This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="8fdb3-143">O objeto de **intervalo** no Microsoft Visual Basic for Applications (VBA) a partir do Microsoft Excel 2002, oferece suporte a um método, **Range.Dirty**, que marca células como precisando de cálculo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-143">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation.</span></span> <span data-ttu-id="8fdb3-144">Quando ele é usado em conjunto com o método **intervalo** . (consulte a próxima seção), ele permite que o recálculo forçado de células em um determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-144">When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range.</span></span> <span data-ttu-id="8fdb3-145">Isso é útil quando você executa um cálculo limitadas durante uma macro, onde o modo de cálculo é definido como manual, para evitar a sobrecarga de cálculo de células não relacionadas para a função de macro.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-145">This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function.</span></span> <span data-ttu-id="8fdb3-146">Métodos de cálculo do intervalo não estão disponíveis por meio da API C.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-146">Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="8fdb3-147">No Excel 2002 e versões anteriores, o Excel embutido uma cadeia de cálculo para cada planilha em cada pasta de trabalho aberta.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-147">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook.</span></span> <span data-ttu-id="8fdb3-148">Isso resultou em alguma complexidade da maneira links entre planilhas foram tratadas e necessárias algumas cuidado para garantir o recálculo eficiente.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-148">This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation.</span></span> <span data-ttu-id="8fdb3-149">Em particular, no Excel 2000, você deve minimizar dependências entre-planilha e planilhas de nome em ordem alfabética para que as folhas que dependem de outras folhas em ordem alfabética vêm após as planilhas que eles dependem.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-149">In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="8fdb3-150">No Excel 2007, a lógica foi aprimorada para habilitar o recálculo em vários segmentos para que não sejam interdependentes de seções da cadeia de cálculo e podem ser calculadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-150">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time.</span></span> <span data-ttu-id="8fdb3-151">Você pode configurar o Excel para usar vários threads em um computador de processador único ou um único segmento em um computador com vários processadores ou vários núcleo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-151">You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="8fdb3-152">Funções (UDFs) definidas pelo usuário assíncrono</span><span class="sxs-lookup"><span data-stu-id="8fdb3-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="8fdb3-153">Quando um cálculo encontra uma UDF assíncrona, salva o estado da fórmula atual, inicia o UDF e continua a avaliar o restante das células.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-153">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells.</span></span> <span data-ttu-id="8fdb3-154">Quando o cálculo termina avaliando as células aguarda Excel as funções assíncronas concluir se houver funções ainda assíncronas em execução.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-154">When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running.</span></span> <span data-ttu-id="8fdb3-155">Como resultados de relatórios cada função assíncrono, Excel termina a fórmula e, em seguida, executa uma nova passagem de cálculo para recalcule em células que usam a célula com a referência para a função assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-155">As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="8fdb3-156">Funções voláteis e não voláteis</span><span class="sxs-lookup"><span data-stu-id="8fdb3-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="8fdb3-157">Excel suporta o conceito de uma função volátil, ou seja, uma cujo valor não é assumido para ser o mesmo de um dado momento para o próximo, mesmo se nenhum dos seus argumentos (se levará qualquer) foi alterada.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-157">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed.</span></span> <span data-ttu-id="8fdb3-158">Excel revê células que contêm funções voláteis, juntamente com todos os dependentes, toda vez que for recalcula.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-158">Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates.</span></span> <span data-ttu-id="8fdb3-159">Por esse motivo, uma quantidade excessiva a dependência de funções voláteis pode fazer o recálculo tempo lento.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-159">For this reason, too much reliance on volatile functions can make recalculation times slow.</span></span> <span data-ttu-id="8fdb3-160">Usá-los com moderação.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-160">Use them sparingly.</span></span>
  
<span data-ttu-id="8fdb3-161">As seguintes funções do Excel são voláteis:</span><span class="sxs-lookup"><span data-stu-id="8fdb3-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="8fdb3-162">**AGORA**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-162">**NOW**</span></span>
    
- <span data-ttu-id="8fdb3-163">**HOJE**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-163">**TODAY**</span></span>
    
- <span data-ttu-id="8fdb3-164">**ALEATÓRIOENTRE**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-164">**RANDBETWEEN**</span></span>
    
- <span data-ttu-id="8fdb3-165">**DESLOCAMENTO**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-165">**OFFSET**</span></span>
    
- <span data-ttu-id="8fdb3-166">**INDIRETAS**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="8fdb3-167">**INFO** (dependendo de seus argumentos)</span><span class="sxs-lookup"><span data-stu-id="8fdb3-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="8fdb3-168">**CÉLULA** (dependendo de seus argumentos)</span><span class="sxs-lookup"><span data-stu-id="8fdb3-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="8fdb3-169">**SOMASE** (dependendo de seus argumentos)</span><span class="sxs-lookup"><span data-stu-id="8fdb3-169">**SUMIF** (depending on its arguments)</span></span> 
    
<span data-ttu-id="8fdb3-170">O VBA e a API C suportam maneiras para informar aos Excel que uma função definida pelo usuário (UDF) deve ser tratada como volátil.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-170">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile.</span></span> <span data-ttu-id="8fdb3-171">Usando o VBA, UDF é declarada como volátil, da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-171">By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="8fdb3-172">Por padrão, o Excel assume que não sejam voláteis UDFs VBA.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-172">By default, Excel assumes that VBA UDFs are not volatile.</span></span> <span data-ttu-id="8fdb3-173">Excel apenas aprende que um UDF é volátil quando ela primeiro chama.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-173">Excel only learns that a UDF is volatile when it first calls it.</span></span> <span data-ttu-id="8fdb3-174">Um UDF volátil pode ser alterado para não voláteis como no exemplo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-174">A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="8fdb3-175">Usando a API C, você pode registrar uma função XLL como volátil antes de sua primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-175">Using the C API, you can register an XLL function as volatile before its first call.</span></span> <span data-ttu-id="8fdb3-176">Ele também permite ativar e desativar o status voláteis de uma função de planilha.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-176">It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="8fdb3-177">Por padrão, o Excel trata XLL UDFs que tem o argumento de intervalo e que são declarados como equivalentes de folha de macro como volátil.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-177">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile.</span></span> <span data-ttu-id="8fdb3-178">Você pode desativar esse estado padrão usando a função de **xlfVolatile** quando o UDF é chamado primeiro.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-178">You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="8fdb3-179">Modos de cálculo, comandos, recálculo seletivo e tabelas de dados</span><span class="sxs-lookup"><span data-stu-id="8fdb3-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="8fdb3-180">O Excel tem três modos de cálculo:</span><span class="sxs-lookup"><span data-stu-id="8fdb3-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="8fdb3-181">Automático</span><span class="sxs-lookup"><span data-stu-id="8fdb3-181">Automatic</span></span>
    
- <span data-ttu-id="8fdb3-182">Automático, exceto tabelas</span><span class="sxs-lookup"><span data-stu-id="8fdb3-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="8fdb3-183">Manual</span><span class="sxs-lookup"><span data-stu-id="8fdb3-183">Manual</span></span>
    
<span data-ttu-id="8fdb3-184">Quando o cálculo é definido como automático, o recálculo ocorre depois de cada entrada de dados e determinados eventos, como os exemplos fornecidos na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-184">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section.</span></span> <span data-ttu-id="8fdb3-185">Pastas de trabalho muito grande, o tempo de recálculo pode ser tão longa que os usuários devem limite quando isso acontece, ou seja, recalcular apenas quando eles precisam.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-185">For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to.</span></span> <span data-ttu-id="8fdb3-186">Para permitir isso, o Excel oferece suporte para o modo manual.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-186">To enable this, Excel supports the manual mode.</span></span> <span data-ttu-id="8fdb3-187">O usuário pode selecionar o modo por meio do sistema de menus do Excel ou programaticamente usando o VBA, COM ou a API C.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-187">The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="8fdb3-188">Tabelas de dados são estruturas especiais em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-188">Data tables are special structures in a worksheet.</span></span> <span data-ttu-id="8fdb3-189">Em primeiro lugar, o usuário configura o cálculo de um resultado em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-189">First, the user sets up the calculation of a result on a worksheet.</span></span> <span data-ttu-id="8fdb3-190">Isso depende de uma ou duas entradas podem ser alteradas principais e outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-190">This depends on one or two key changeable inputs and other parameters.</span></span> <span data-ttu-id="8fdb3-191">O usuário, em seguida, pode criar uma tabela dos resultados para um conjunto de valores para uma ou ambas as entradas de chave.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-191">The user can then create a table of results for a set of values for one or both of the key inputs.</span></span> <span data-ttu-id="8fdb3-192">A tabela é criada usando o **Assistente de tabela de dados**.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-192">The table is created by using the **Data Table Wizard**.</span></span> <span data-ttu-id="8fdb3-193">Depois que a tabela estiver configurada, o Excel conecta-se as entradas de um a um cálculo e copia o valor resultante para a tabela.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-193">After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table.</span></span> <span data-ttu-id="8fdb3-194">Como uma ou duas entradas podem ser usadas, tabelas de dados podem ser uma - ou bidimensional.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-194">As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="8fdb3-195">Recálculo das tabelas de dados é tratado ligeiramente diferente:</span><span class="sxs-lookup"><span data-stu-id="8fdb3-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="8fdb3-196">Recálculo é tratado de maneira assíncrona para o recálculo de pasta de trabalho normal para que tabelas grandes podem demorar mais recalcular do resto da pasta de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="8fdb3-197">Referências circulares são toleradas.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-197">Circular references are tolerated.</span></span> <span data-ttu-id="8fdb3-198">Se o cálculo que é usado para obter o resultado depende de um ou mais valores da tabela de dados, o Excel não retornará um erro quando a dependência circular.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-198">If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 
    
<span data-ttu-id="8fdb3-199">Devido a maneira de diferente que Excel manipula o recálculo de tabelas de dados e o fato de que as tabelas grandes que dependem de cálculos de longos ou complexos podem levar muito tempo para calcular, o Excel permite que você desabilite o cálculo automático de tabelas de dados.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-199">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables.</span></span> <span data-ttu-id="8fdb3-200">Para fazer isso, defina o modo de cálculo para automático, exceto tabelas de dados.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-200">To do this, set the calculation mode to Automatic except Data Tables.</span></span> <span data-ttu-id="8fdb3-201">Quando o cálculo é neste modo, o usuário recalcula as tabelas de dados pressionando F9 ou alguma operação programática equivalente.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-201">When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="8fdb3-202">Excel expõe métodos através do qual você pode alterar o modo de recálculo e controlar o recálculo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-202">Excel exposes methods through which you can alter the recalculation mode and control recalculation.</span></span> <span data-ttu-id="8fdb3-203">Esses métodos foram aprimorados de versão para versão para permitir um controle mais preciso.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-203">These methods have been improved from version to version to allow for finer control.</span></span> <span data-ttu-id="8fdb3-204">Os recursos da API C sob este aspecto refletem aqueles que estavam disponíveis no Excel versão 5 e portanto não dê você mesmo controle que você tenha usando o VBA em versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-204">The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="8fdb3-205">Usados com mais frequência quando o Excel está no modo de cálculo manual, esses métodos permitem seletivo cálculo dos intervalos, planilhas e pastas de trabalho do recálculo completo de todas as pastas de trabalho abertas e até mesmo completo reconstrução de cadeia de cálculo e a árvore de dependência.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-205">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="8fdb3-206">Cálculo de intervalo</span><span class="sxs-lookup"><span data-stu-id="8fdb3-206">Range Calculation</span></span>

<span data-ttu-id="8fdb3-207">Pressionamento de tecla: nenhum</span><span class="sxs-lookup"><span data-stu-id="8fdb3-207">Keystroke: None</span></span>
  
<span data-ttu-id="8fdb3-208">VBA: **intervalo** (introduzida no Excel 2000, alterado no Excel 2007) e **Range.CalculateRowMajorOrder** (introduzida no Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="8fdb3-208">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="8fdb3-209">API C: Não suporte</span><span class="sxs-lookup"><span data-stu-id="8fdb3-209">C API: Not supported</span></span>
  
- <span data-ttu-id="8fdb3-210">**Modo manual**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-210">**Manual mode**</span></span>
    
    <span data-ttu-id="8fdb3-211">Recalcula apenas as células no intervalo determinado independentemente de estarem ou dirty ou não.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-211">Recalculates just the cells in the given range regardless of whether they are dirty or not.</span></span> <span data-ttu-id="8fdb3-212">Comportamento do método **intervalo** alterado no Excel 2007; No entanto, o comportamento antigo ainda é suportado pelo método **Range.CalculateRowMajorOrder** .</span><span class="sxs-lookup"><span data-stu-id="8fdb3-212">Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="8fdb3-213">**Modos de automático, exceto tabelas ou automático**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-213">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="8fdb3-214">Recalcula a pasta de trabalho, mas não forçar o recálculo do intervalo ou qualquer células do intervalo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-214">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="8fdb3-215">Cálculo da planilha ativa</span><span class="sxs-lookup"><span data-stu-id="8fdb3-215">Active Worksheet Calculation</span></span>

<span data-ttu-id="8fdb3-216">O pressionamento de tecla: SHIFT + F9</span><span class="sxs-lookup"><span data-stu-id="8fdb3-216">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="8fdb3-217">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-217">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="8fdb3-218">API C: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-218">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="8fdb3-219">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-219">**All modes**</span></span>
    
    <span data-ttu-id="8fdb3-220">Recalcula as células marcadas para cálculo na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-220">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="8fdb3-221">Cálculo da planilha especificada</span><span class="sxs-lookup"><span data-stu-id="8fdb3-221">Specified Worksheet Calculation</span></span>

<span data-ttu-id="8fdb3-222">Pressionamento de tecla: nenhum</span><span class="sxs-lookup"><span data-stu-id="8fdb3-222">Keystroke: None</span></span>
  
<span data-ttu-id="8fdb3-223">VBA: **planilhas (** referência **). Calcular**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-223">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="8fdb3-224">API C: Não suporte</span><span class="sxs-lookup"><span data-stu-id="8fdb3-224">C API: Not supported</span></span>
  
- <span data-ttu-id="8fdb3-225">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-225">**All modes**</span></span>
    
    <span data-ttu-id="8fdb3-226">Recalcula as células dirty e seus dependentes dentro apenas da planilha especificada.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-226">Recalculates the dirty cells and their dependents within the specified worksheet only.</span></span> <span data-ttu-id="8fdb3-227">Referência é o nome da planilha como uma cadeia de caracteres ou o número de índice na pasta de trabalho relevante.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-227">Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="8fdb3-228">Excel 2000 e versões posteriores exponham uma propriedade **Boolean** de planilha, a propriedade **EnableCalculation** .</span><span class="sxs-lookup"><span data-stu-id="8fdb3-228">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property.</span></span> <span data-ttu-id="8fdb3-229">Essa configuração como **True** de **False** dirties todas as células da planilha especificada.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-229">Setting this to **True** from **False** dirties all cells in the specified worksheet.</span></span> <span data-ttu-id="8fdb3-230">Nos modos automáticos, isso também dispara um recálculo da pasta de trabalho inteira.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-230">In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="8fdb3-231">No modo manual, o código a seguir faz com que o recálculo da planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-231">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="8fdb3-232">Árvore de pasta de trabalho reconstruir e forçada recálculo</span><span class="sxs-lookup"><span data-stu-id="8fdb3-232">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="8fdb3-233">O pressionamento de tecla: CTRL + ALT + SHIFT + F9 (introduzida no Excel 2002)</span><span class="sxs-lookup"><span data-stu-id="8fdb3-233">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="8fdb3-234">VBA: **pastas de trabalho (** referência **). ForceFullCalculation** (introduzida no Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="8fdb3-234">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="8fdb3-235">API C: Não suporte</span><span class="sxs-lookup"><span data-stu-id="8fdb3-235">C API: Not supported</span></span>
  
- <span data-ttu-id="8fdb3-236">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-236">**All modes**</span></span>
    
    <span data-ttu-id="8fdb3-237">Faz com que o Excel para reconstruir a árvore de dependência e a cadeia de cálculo para uma determinada pasta de trabalho e força um recálculo do todas as células que contêm fórmulas.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-237">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="8fdb3-238">Todas as pastas de trabalho</span><span class="sxs-lookup"><span data-stu-id="8fdb3-238">All Open Workbooks</span></span>

<span data-ttu-id="8fdb3-239">Pressionamento de tecla: F9</span><span class="sxs-lookup"><span data-stu-id="8fdb3-239">Keystroke: F9</span></span>
  
<span data-ttu-id="8fdb3-240">VBA: **Application. Calculate**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-240">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="8fdb3-241">API C: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-241">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="8fdb3-242">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-242">**All modes**</span></span>
    
    <span data-ttu-id="8fdb3-243">Recalcula todas as células que Excel tenha marcado como sujo, ou seja, dependentes da dados voláteis ou alterados e células programaticamente marcadas como sujas.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-243">Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty.</span></span> <span data-ttu-id="8fdb3-244">Se o modo de cálculo for automático, exceto tabelas, isso calcula nessas tabelas que requeiram a atualização e também todas as funções voláteis e seus dependentes.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-244">If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="8fdb3-245">Árvore de todas as pastas de trabalho abertas reconstruir e forçada de cálculo</span><span class="sxs-lookup"><span data-stu-id="8fdb3-245">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="8fdb3-246">Pressionamento de tecla: CTRL + ALT + F9</span><span class="sxs-lookup"><span data-stu-id="8fdb3-246">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="8fdb3-247">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-247">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="8fdb3-248">API C: Não suporte</span><span class="sxs-lookup"><span data-stu-id="8fdb3-248">C API: Not supported</span></span>
  
- <span data-ttu-id="8fdb3-249">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="8fdb3-249">**All modes**</span></span>
    
    <span data-ttu-id="8fdb3-250">Recalcula todas as células em pastas de trabalho abertas tudo.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-250">Recalculates all cells in all open workbooks.</span></span> <span data-ttu-id="8fdb3-251">Se o modo de cálculo for automático, exceto tabelas, ele força as tabelas a ser recalculado.</span><span class="sxs-lookup"><span data-stu-id="8fdb3-251">If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8fdb3-252">Confira também</span><span class="sxs-lookup"><span data-stu-id="8fdb3-252">See also</span></span>



[<span data-ttu-id="8fdb3-253">Recálculo multithreaded no Excel</span><span class="sxs-lookup"><span data-stu-id="8fdb3-253">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="8fdb3-254">Tipos de dados usados pelo Excel</span><span class="sxs-lookup"><span data-stu-id="8fdb3-254">Data Types Used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="8fdb3-255">Gerenciamento de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="8fdb3-255">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="8fdb3-256">Excel Programming Concepts</span><span class="sxs-lookup"><span data-stu-id="8fdb3-256">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

