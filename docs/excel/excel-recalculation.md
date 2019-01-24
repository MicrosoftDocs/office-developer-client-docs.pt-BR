---
title: Recálculo do Excel
manager: kelbow
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- cálculo forçado [excel 2007],recálculo seletivo [Excel 2007],funções [Excel 2007], volátil,modos de cálculo,células recalculadas [Excel 2007],dependência [Excel 2007],cálculo especificado de planilha [Excel 2007],recálculo [Excel 2007],reconstrução de árvore de pasta de trabalho [Excel 2007],cálculo de intervalo [Excel 2007],recálculo do Excel,funções voláteis [Excel 2007],funções [Excel 2007], não volátil,cálculo de planilha ativa [Excel 2007],células sujas [Excel 2007],funções não voláteis [Excel 2007],recálculo forçado [Excel 2007]
ms.assetid: b4c38442-42e6-4fd2-a1b0-97cfa3300379
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 07deec5ad104c59074567725d6abf9b66711e351
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703346"
---
# <a name="excel-recalculation"></a><span data-ttu-id="9b5d9-104">Recálculo do Excel</span><span class="sxs-lookup"><span data-stu-id="9b5d9-104">Excel Recalculation</span></span>

<span data-ttu-id="9b5d9-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9b5d9-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9b5d9-106">O usuário pode acionar o recálculo no Microsoft Excel de várias maneiras, por exemplo:</span><span class="sxs-lookup"><span data-stu-id="9b5d9-106">The user can trigger recalculation in Microsoft Excel in several ways, for example:</span></span>
  
- <span data-ttu-id="9b5d9-107">Inserindo novos dados (se o Excel estiver no Modo de recálculo automático, descrito mais adiante neste tópico).</span><span class="sxs-lookup"><span data-stu-id="9b5d9-107">Entering new data (if Excel is in Automatic recalculation mode, described later in this topic).</span></span>
    
- <span data-ttu-id="9b5d9-108">Explicitamente instruindo o Excel a recalcular uma pasta de trabalho no todo ou em parte.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-108">Explicitly instructing Excel to recalculate all or part of a workbook.</span></span>
    
- <span data-ttu-id="9b5d9-109">Excluindo ou inserindo uma linha ou coluna.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-109">Deleting or inserting a row or column.</span></span>
    
- <span data-ttu-id="9b5d9-110">Salvando uma pasta de trabalho enquanto a opção **Recalcular antes de salvar** está definida.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-110">Saving a workbook while the **Recalculate before save** option is set.</span></span> 
    
- <span data-ttu-id="9b5d9-111">Executando determinadas ações de Filtro Automático.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-111">Performing certain Autofilter actions.</span></span>
    
- <span data-ttu-id="9b5d9-112">Clicando duas vezes em um divisor de linha ou coluna (no modo de Cálculo automático).</span><span class="sxs-lookup"><span data-stu-id="9b5d9-112">Double-clicking a row or column divider (in Automatic calculation mode).</span></span>
    
- <span data-ttu-id="9b5d9-113">Adicionando, editando ou excluindo um nome definido.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-113">Adding, editing, or deleting a defined name.</span></span>
    
- <span data-ttu-id="9b5d9-114">Renomeando uma planilha.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-114">Renaming a worksheet.</span></span>
    
- <span data-ttu-id="9b5d9-115">Alterando a posição de uma planilha em relação a outras planilhas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-115">Changing the position of a worksheet in relation to other worksheets.</span></span>
    
- <span data-ttu-id="9b5d9-116">Ocultando ou como reexibindo linhas, mas não colunas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-116">Hiding or unhiding rows, but not columns.</span></span>
    
> [!NOTE]
> <span data-ttu-id="9b5d9-117">Este tópico não faz distinção entre o usuário que pressiona diretamente uma tecla ou clica no mouse e as tarefas que estão sendo executadas por um comando ou macro.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-117">This topic does not distinguish between the user directly pressing a key or clicking the mouse, and those tasks being done by a command or macro.</span></span> <span data-ttu-id="9b5d9-118">O usuário executa o comando ou faz algo para que o comando seja executado para que isso ainda seja considerado uma ação do usuário.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-118">The user runs the command, or does something to cause the command to run so that it is still considered a user action.</span></span> <span data-ttu-id="9b5d9-119">Portanto, a frase "o usuário" também significa "o usuário ou um comando ou processo iniciado pelo usuário".</span><span class="sxs-lookup"><span data-stu-id="9b5d9-119">Therefore the phrase "the user" also means "the user, or a command or process started by the user."</span></span> 
  
## <a name="dependence-dirty-cells-and-recalculated-cells"></a><span data-ttu-id="9b5d9-120">Dependência, Células Sujas e Células Recalculadas</span><span class="sxs-lookup"><span data-stu-id="9b5d9-120">Dependence, Dirty Cells, and Recalculated Cells</span></span>

<span data-ttu-id="9b5d9-121">O cálculo de planilhas no Excel pode ser visto como um processo em três etapas:</span><span class="sxs-lookup"><span data-stu-id="9b5d9-121">The calculation of worksheets in Excel can be viewed as a three-stage process:</span></span>
  
1. <span data-ttu-id="9b5d9-122">Construção de uma árvore de dependência</span><span class="sxs-lookup"><span data-stu-id="9b5d9-122">Construction of a dependency tree</span></span>
    
2. <span data-ttu-id="9b5d9-123">Construção de uma cadeia de cálculo</span><span class="sxs-lookup"><span data-stu-id="9b5d9-123">Construction of a calculation chain</span></span>
    
3. <span data-ttu-id="9b5d9-124">Recálculo de células</span><span class="sxs-lookup"><span data-stu-id="9b5d9-124">Recalculation of cells</span></span>
    
<span data-ttu-id="9b5d9-125">A árvore de dependência informa ao Excel quais células dependem de quais outras ou, de forma equivalente, quais células são precedentes a quais outras.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-125">The dependency tree informs Excel about which cells depend on which others, or equivalently, which cells are precedents for which others.</span></span> <span data-ttu-id="9b5d9-126">Com base nessa árvore, o Excel cria uma cadeia de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-126">From this tree, Excel constructs a calculation chain.</span></span> <span data-ttu-id="9b5d9-127">A cadeia de cálculo lista todas as células que contêm fórmulas na ordem em que devem ser calculadas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-127">The calculation chain lists all the cells that contain formulas in the order in which they should be calculated.</span></span> <span data-ttu-id="9b5d9-128">Durante o recálculo, o Excel revisa essa cadeia se encontra uma fórmula que depende de uma célula que ainda não foi calculada.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-128">During recalculation, Excel revises this chain if it comes across a formula that depends on a cell that has not yet been calculated.</span></span> <span data-ttu-id="9b5d9-129">Nesse caso, a célula que está sendo calculada e seus dependentes são movidos para baixo na cadeia.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-129">In this case, the cell that is being calculated and its dependents are moved down the chain.</span></span> <span data-ttu-id="9b5d9-130">Por esse motivo, os tempos de cálculo geralmente podem melhorar em uma planilha que acaba de ser aberta nos primeiros ciclos de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-130">For this reason, calculation times can often improve in a worksheet that has just been opened in the first few calculation cycles.</span></span>
  
<span data-ttu-id="9b5d9-131">Quando uma alteração estrutural é feita em uma pasta de trabalho, por exemplo, quando uma nova fórmula é inserida, o Excel recria a árvore de dependência e a cadeia de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-131">When a structural change is made to a workbook, for example, when a new formula is entered, Excel reconstructs the dependency tree and calculation chain.</span></span> <span data-ttu-id="9b5d9-132">Quando novos dados ou novas fórmulas são inseridos, o Excel marca todas as células que dependem de novos dados como precisando de recálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-132">When new data or new formulas are entered, Excel marks all the cells that depend on that new data as needing recalculation.</span></span> <span data-ttu-id="9b5d9-133">As células marcadas dessa maneira são conhecidas como *sujas*.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-133">Cells that are marked in this way are known as  *dirty*  .</span></span> <span data-ttu-id="9b5d9-134">Todos os dependentes diretos e indiretos são marcados como sujos. Portanto, se B1 depender de A1, e C1 depender de B1, quando A1 for alterado, tanto B1 quanto C1 serão marcados como sujos.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-134">All direct and indirect dependents are marked as dirty so that if B1 depends on A1, and C1 depends on B1, when A1 is changed, both B1 and C1 are marked as dirty.</span></span> 
  
<span data-ttu-id="9b5d9-135">Se uma célula depender de si mesma, direta ou indiretamente, o Excel detectará a referência circular e avisará o usuário.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-135">If a cell depends, directly or indirectly, on itself, Excel detects the circular reference and warns the user.</span></span> <span data-ttu-id="9b5d9-136">Isso geralmente é uma condição de erro que o usuário deve corrigir, e o Excel fornece ferramentas gráficas e de navegação muito úteis para ajudar o usuário a encontrar a origem da dependência circular.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-136">This is usually an error condition that the user must fix, and Excel provides very helpful graphical and navigational tools to help the user to find the source of the circular dependency.</span></span> <span data-ttu-id="9b5d9-137">Em alguns casos, você pode querer deliberadamente que essa condição exista.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-137">In some cases, you might deliberately want this condition to exist.</span></span> <span data-ttu-id="9b5d9-138">Por exemplo, você pode querer executar um cálculo iterativo em que o ponto inicial da próxima iteração é o resultado da iteração anterior.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-138">For example, you might want to run an iterative calculation where the starting point for the next iteration is the result of the previous iteration.</span></span> <span data-ttu-id="9b5d9-139">O Excel dá suporte ao controle de cálculos iterativos por meio da caixa de diálogo de opções de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-139">Excel supports control of iterative calculations through the calculation options dialog box.</span></span>
  
<span data-ttu-id="9b5d9-140">Depois de marcar as células como sujas, quando um recálculo é feito em seguida, o Excel reavalia o conteúdo de cada célula suja na ordem ditada pela cadeia de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-140">After marking cells as dirty, when a recalculation is next done, Excel reevaluates the contents of each dirty cell in the order dictated by the calculation chain.</span></span> <span data-ttu-id="9b5d9-141">No exemplo fornecido anteriormente, isso significa que B1 vem primeiro e, em seguida, C1.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-141">In the example given earlier, this means B1 is first, and then C1.</span></span> <span data-ttu-id="9b5d9-142">Esse recálculo ocorrerá imediatamente após o Excel terminar de marcar as células como sujas se o modo de recálculo for automático. Caso contrário, ocorrerá mais tarde.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-142">This recalculation occurs immediately after Excel finishes marking cells as dirty if the recalculation mode is automatic; otherwise, it occurs later.</span></span>
  
<span data-ttu-id="9b5d9-143">A partir do Microsoft Excel 2002, o objeto **Range** no VBA (Visual Basic for Applications) dá suporte a um método, **Range.Dirty**, que marca células como precisando de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-143">Starting in Microsoft Excel 2002, the **Range** object in Microsoft Visual Basic for Applications (VBA) supports a method, **Range.Dirty**, which marks cells as needing calculation.</span></span> <span data-ttu-id="9b5d9-144">Quando usado em conjunto com o método **Range.Calculate** (veja a próxima seção), ele permite o recálculo forçado de células em determinado intervalo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-144">When it is used together with the **Range.Calculate** method (see next section), it enables forced recalculation of cells in a given range.</span></span> <span data-ttu-id="9b5d9-145">Isso é útil quando você está executando um cálculo limitado durante uma macro, em que o modo de cálculo é definido como manual, para evitar a sobrecarga de cálculo de células não relacionadas à função de macro.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-145">This is useful when you are performing a limited calculation during a macro, where the calculation mode is set to manual, to avoid the overhead of calculating cells unrelated to the macro function.</span></span> <span data-ttu-id="9b5d9-146">Os métodos de cálculo de intervalo não estão disponíveis por meio da API de C.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-146">Range calculation methods are not available through the C API.</span></span> 
  
<span data-ttu-id="9b5d9-147">No Excel 2002 e versões anteriores, o Excel criava uma cadeia de cálculo para cada planilha em cada pasta de trabalho aberta.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-147">In Excel 2002 and earlier versions, Excel built a calculation chain for each worksheet in each open workbook.</span></span> <span data-ttu-id="9b5d9-148">Isso gerava alguma complexidade na forma como os vínculos entre as planilhas eram tratados e exigia algum cuidado para garantir que o recálculo fosse eficiente.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-148">This resulted in some complexity in the way links between worksheets were handled, and required some care to ensure efficient recalculation.</span></span> <span data-ttu-id="9b5d9-149">Em particular, no Excel 2000, você deve minimizar as dependências de planilha cruzada e nomear as planilhas em ordem alfabética, para que as planilhas que dependem de outras planilhas venham em ordem alfabética após as planilhas das quais dependem.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-149">In particular, in Excel 2000, you should minimize cross-worksheet dependencies and name worksheets in alphabetical order so that sheets that depend on other sheets come alphabetically after the sheets they depend on.</span></span>
  
<span data-ttu-id="9b5d9-150">No Excel 2007, a lógica foi aprimorada para habilitar o recálculo em vários threads, de forma que as seções da cadeia de cálculo não sejam interdependentes e possam ser calculadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-150">In Excel 2007, the logic was improved to enable recalculation on multiple threads so that sections of the calculation chain are not interdependent and can be calculated at the same time.</span></span> <span data-ttu-id="9b5d9-151">Você pode configurar o Excel para usar vários threads em um computador com processador único ou um único thread em um computador com vários processadores ou vários núcleos.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-151">You can configure Excel to use multiple threads on a single processor computer, or a single thread on a multi-processor or multi-core computer.</span></span> 
  
## <a name="asynchronous-user-defined-functions-udfs"></a><span data-ttu-id="9b5d9-152">UDFs (Funções Assíncronas Definidas pelo Usuário)</span><span class="sxs-lookup"><span data-stu-id="9b5d9-152">Asynchronous User Defined Functions (UDFs)</span></span>

<span data-ttu-id="9b5d9-153">Quando um cálculo encontra uma UDF assíncrona, ele salva o estado da fórmula atual, inicia a UDF e continua avaliando o restante das células.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-153">When a calculation encounters an asynchronous UDF, it saves the state of the current formula, starts the UDF and continues evaluating the rest of the cells.</span></span> <span data-ttu-id="9b5d9-154">Quando o cálculo termina de avaliar as células, o Excel aguarda a conclusão das funções assíncronas, se ainda há funções assíncronas em execução.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-154">When the calculation finishes evaluating the cells Excel waits for the asynchronous functions to complete if there are still asynchronous functions running.</span></span> <span data-ttu-id="9b5d9-155">À medida que cada função assíncrona relata resultados, o Excel conclui a fórmula e, em seguida, executa uma nova passagem de cálculo para recalcular células que usam a célula com a referência à função assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-155">As each asynchronous function reports results, Excel finishes the formula, and then runs a new calculation pass to re-compute cells that use the cell with the reference to the asynchronous function.</span></span>
  
## <a name="volatile-and-non-volatile-functions"></a><span data-ttu-id="9b5d9-156">Funções voláteis e não voláteis</span><span class="sxs-lookup"><span data-stu-id="9b5d9-156">Volatile and Non-Volatile Functions</span></span>

<span data-ttu-id="9b5d9-157">O Excel dá suporte ao conceito de uma função volátil, ou seja, uma cujo valor não pode ser presumido como sendo o mesmo de um momento para o outro, mesmo que nenhum de seus argumentos tenha sido alterado.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-157">Excel supports the concept of a volatile function, that is, one whose value cannot be assumed to be the same from one moment to the next even if none of its arguments (if it takes any) has changed.</span></span> <span data-ttu-id="9b5d9-158">O Excel reavalia células que contêm funções voláteis, juntamente com todos os dependentes, sempre que realiza o recálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-158">Excel reevaluates cells that contain volatile functions, together with all dependents, every time that it recalculates.</span></span> <span data-ttu-id="9b5d9-159">Por essa razão, a dependência excessiva de funções voláteis pode aumentar o tempo de recálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-159">For this reason, too much reliance on volatile functions can make recalculation times slow.</span></span> <span data-ttu-id="9b5d9-160">Use-as com moderação.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-160">Use them sparingly.</span></span>
  
<span data-ttu-id="9b5d9-161">As seguintes funções do Excel são voláteis:</span><span class="sxs-lookup"><span data-stu-id="9b5d9-161">The following Excel functions are volatile:</span></span>
  
- <span data-ttu-id="9b5d9-162">**AGORA**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-162">**Now**</span></span>
    
- <span data-ttu-id="9b5d9-163">**HOJE**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-163">**today.**</span></span>
    
- <span data-ttu-id="9b5d9-164">**ALEATÓRIOENTRE**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-164">**RandBetween**</span></span>
    
- <span data-ttu-id="9b5d9-165">**DESLOCAMENTO**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-165">**Offset**</span></span>
    
- <span data-ttu-id="9b5d9-166">**INDIRETO**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-166">**INDIRECT**</span></span>
    
- <span data-ttu-id="9b5d9-167">**INFORMAÇÕES** (dependendo de seus argumentos)</span><span class="sxs-lookup"><span data-stu-id="9b5d9-167">**INFO** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="9b5d9-168">**CÉLULA** (dependendo de seus argumentos)</span><span class="sxs-lookup"><span data-stu-id="9b5d9-168">**CELL** (depending on its arguments)</span></span> 
    
- <span data-ttu-id="9b5d9-169">**SOMASE** (dependendo de seus argumentos)</span><span class="sxs-lookup"><span data-stu-id="9b5d9-169">**SUMIF** (depending on its arguments)</span></span> 
    
<span data-ttu-id="9b5d9-170">Tanto o VBA quanto a API de C dão suporte a maneiras de informar ao Excel que uma UDF (função definida pelo usuário) deve ser tratada como volátil.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-170">Both the VBA and C API support ways to inform Excel that a user-defined function (UDF) should be handled as volatile.</span></span> <span data-ttu-id="9b5d9-171">Usando o VBA, a UDF é declarada como volátil da maneira a seguir.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-171">By using VBA, the UDF is declared as volatile as follows.</span></span>
  
```vb
Function MyUDF(MakeMeVolatile As Boolean) As Double
   ' Good practice to call this on the first line.
   Application.Volatile (MakeMeVolatile)
   MyUDF = Now
End Function

```

<span data-ttu-id="9b5d9-172">Por padrão, o Excel presume que as UDFs do VBA não são voláteis.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-172">By default, Excel assumes that VBA UDFs are not volatile.</span></span> <span data-ttu-id="9b5d9-173">O Excel só descobre que uma UDF é volátil quando a chama pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-173">Excel only learns that a UDF is volatile when it first calls it.</span></span> <span data-ttu-id="9b5d9-174">Uma UDF volátil pode ser alterada de volta para não volátil, como neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-174">A volatile UDF can be changed back to non-volatile as in this example.</span></span>
  
<span data-ttu-id="9b5d9-175">Usando a API de C, você pode registrar uma função XLL como volátil antes de sua primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-175">Using the C API, you can register an XLL function as volatile before its first call.</span></span> <span data-ttu-id="9b5d9-176">Isso também permite que você ative e desative o status volátil de uma função de planilha.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-176">It also enables you to switch on and off the volatile status of a worksheet function.</span></span>
  
<span data-ttu-id="9b5d9-177">Por padrão, o Excel lida com UDFs XLL que aceitam argumentos de intervalo e que são declaradas como equivalentes de planilha de macro como voláteis.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-177">By default, Excel handles XLL UDFs that take range arguments and that are declared as macro-sheet equivalents as volatile.</span></span> <span data-ttu-id="9b5d9-178">Você pode desativar esse estado padrão usando a função **xlfVolatile** quando a UDF é chamada pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-178">You can turn this default state off using the **xlfVolatile** function when the UDF is first called.</span></span> 
  
## <a name="calculation-modes-commands-selective-recalculation-and-data-tables"></a><span data-ttu-id="9b5d9-179">Modos de Cálculo, Comandos, Recálculo Seletivo e Tabelas de Dados</span><span class="sxs-lookup"><span data-stu-id="9b5d9-179">Calculation Modes, Commands, Selective Recalculation, and Data Tables</span></span>

<span data-ttu-id="9b5d9-180">O Excel tem três modos de cálculo:</span><span class="sxs-lookup"><span data-stu-id="9b5d9-180">Excel has three calculation modes:</span></span>
  
- <span data-ttu-id="9b5d9-181">Automático</span><span class="sxs-lookup"><span data-stu-id="9b5d9-181">Automatic</span></span>
    
- <span data-ttu-id="9b5d9-182">Automático, Exceto Tabelas</span><span class="sxs-lookup"><span data-stu-id="9b5d9-182">Automatic Except Tables</span></span>
    
- <span data-ttu-id="9b5d9-183">Manual</span><span class="sxs-lookup"><span data-stu-id="9b5d9-183">Manual</span></span>
    
<span data-ttu-id="9b5d9-184">Quando o cálculo é definido como automático, o recálculo ocorre após cada entrada de dados e após certos eventos, como os exemplos fornecidos na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-184">When calculation is set to automatic, recalculation occurs after every data input and after certain events such as the examples given in the previous section.</span></span> <span data-ttu-id="9b5d9-185">Para pastas de trabalho muito grandes, o tempo de recálculo pode ser tão longo que os usuários devem limitar quando isso ocorre, ou seja, recalcular somente quando necessário.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-185">For very large workbooks, recalculation time might be so long that users must limit when this happens, that is, only recalculating when they need to.</span></span> <span data-ttu-id="9b5d9-186">Para habilitar isso, o Excel dá suporte ao modo manual.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-186">To enable this, Excel supports the manual mode.</span></span> <span data-ttu-id="9b5d9-187">O usuário pode selecionar o modo por meio do sistema de menu do Excel ou programaticamente usando VBA, COM ou a API de C.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-187">The user can select the mode through the Excel menu system, or programmatically using VBA, COM, or the C API.</span></span>
  
<span data-ttu-id="9b5d9-188">Tabelas de dados são estruturas especiais em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-188">Data tables are special structures in a worksheet.</span></span> <span data-ttu-id="9b5d9-189">Primeiro, o usuário configura o cálculo de um resultado em uma planilha.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-189">First, the user sets up the calculation of a result on a worksheet.</span></span> <span data-ttu-id="9b5d9-190">Isso depende de uma ou duas entradas variáveis e outros parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-190">This depends on one or two key changeable inputs and other parameters.</span></span> <span data-ttu-id="9b5d9-191">O usuário pode então criar uma tabela de resultados para um conjunto de valores para uma das entradas principais ou ambas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-191">The user can then create a table of results for a set of values for one or both of the key inputs.</span></span> <span data-ttu-id="9b5d9-192">A tabela é criada usando o **Assistente de Tabela de Dados**.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-192">The table is created by using the **Data Table Wizard**.</span></span> <span data-ttu-id="9b5d9-193">Depois que a tabela é configurada, o Excel conecta as entradas uma a uma no cálculo e copia o valor resultante na tabela.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-193">After the table is set up, Excel plugs the inputs one-by-one into the calculation and copies the resulting value into the table.</span></span> <span data-ttu-id="9b5d9-194">Como uma ou duas entradas podem ser usadas, as tabelas de dados podem ser unidimensionais ou bidimensionais.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-194">As one or two inputs can be used, data tables can be one- or two-dimensional.</span></span> 
  
<span data-ttu-id="9b5d9-195">O recálculo de tabelas de dados é tratado de forma ligeiramente diferente:</span><span class="sxs-lookup"><span data-stu-id="9b5d9-195">Recalculation of data tables is handled slightly differently:</span></span>
  
- <span data-ttu-id="9b5d9-196">O recálculo é tratado de forma assíncrona para o recálculo regular da pasta de trabalho, assim, as tabelas grandes demoram mais para serem recalculadas do que o restante da pasta de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-196">Recalculation is handled asynchronously to regular workbook recalculation so that large tables might take longer to recalculate than the rest of the workbook.</span></span>
    
- <span data-ttu-id="9b5d9-197">Referências circulares são toleradas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-197">Circular references are tolerated.</span></span> <span data-ttu-id="9b5d9-198">Se o cálculo usado para obter o resultado depender de um ou mais valores da tabela de dados, o Excel não retornará um erro para a dependência circular.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-198">If the calculation that is used to get the result depends on one or more values from the data table, Excel does not return an error for the circular dependency.</span></span> 

- <span data-ttu-id="9b5d9-199">Tabelas de dados não usam cálculo multi-threaded.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-199">Data tables do not use multi-threaded calculation.</span></span>
    
<span data-ttu-id="9b5d9-200">Dada a maneira diferente como o Excel lida com o recálculo de tabelas de dados e o fato de que tabelas grandes que dependem de cálculos complexos ou demorados podem levar muito tempo para serem calculadas, o Excel permite desabilitar o cálculo automático de tabelas de dados.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-200">Given the different way that Excel handles recalculation of data tables, and the fact that large tables that depend on complex or lengthy calculations can take a long time to calculate, Excel lets you disable the automatic calculation of data tables.</span></span> <span data-ttu-id="9b5d9-201">Para fazer isso, defina o modo de cálculo como Automático, exceto Tabelas de Dados.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-201">To do this, set the calculation mode to Automatic except Data Tables.</span></span> <span data-ttu-id="9b5d9-202">Quando o cálculo está neste modo, o usuário recalcula as tabelas de dados pressionando F9 ou usando alguma operação programática equivalente.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-202">When calculation is in this mode, the user recalculates the data tables by pressing F9 or some equivalent programmatic operation.</span></span>
  
<span data-ttu-id="9b5d9-203">O Excel expõe métodos pelos quais você pode alterar o modo de recálculo e controlar o recálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-203">Excel exposes methods through which you can alter the recalculation mode and control recalculation.</span></span> <span data-ttu-id="9b5d9-204">Esses métodos foram aprimorados de versão para versão para permitir controle mais preciso.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-204">These methods have been improved from version to version to allow for finer control.</span></span> <span data-ttu-id="9b5d9-205">Os recursos da API de C a esse respeito refletem os que estavam disponíveis na versão 5 do Excel e, assim, não fornecem o mesmo controle de que você dispõe ao usar o VBA em versões mais recentes.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-205">The capabilities of the C API in this regard reflect those that were available in Excel version 5, and so do not give you the same control that you have using VBA in more recent versions.</span></span> 
  
<span data-ttu-id="9b5d9-206">Usados com mais frequência quando o Excel está no modo de cálculo manual, esses métodos permitem o cálculo seletivo de pastas de trabalho, planilhas e intervalos, o recálculo completo de todas as pastas de trabalho abertas e até a reconstrução completa da árvore de dependência e da cadeia de cálculo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-206">Most frequently used when Excel is in manual calculation mode, these methods allow selective calculation of workbooks, worksheets, and ranges, complete recalculation of all open workbooks, and even complete rebuild of the dependency tree and calculation chain.</span></span>
  
### <a name="range-calculation"></a><span data-ttu-id="9b5d9-207">Cálculo de Intervalo</span><span class="sxs-lookup"><span data-stu-id="9b5d9-207">Range Calculation</span></span>

<span data-ttu-id="9b5d9-208">Pressionamento de teclas: nenhum</span><span class="sxs-lookup"><span data-stu-id="9b5d9-208">Keystroke: None</span></span>
  
<span data-ttu-id="9b5d9-209">VBA: **Range.Calculate** (introduzido no Excel 2000; alterado no Excel 2007) e **Range.CalculateRowMajorOrder** (introduzido no Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="9b5d9-209">VBA: **Range.Calculate** (introduced in Excel 2000, changed in Excel 2007) and **Range.CalculateRowMajorOrder** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="9b5d9-210">API de C: sem suporte</span><span class="sxs-lookup"><span data-stu-id="9b5d9-210">C API: Not supported</span></span>
  
- <span data-ttu-id="9b5d9-211">**Modo manual**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-211">**Manual mode**</span></span>
    
    <span data-ttu-id="9b5d9-212">Recalcula apenas as células no intervalo determinado, independentemente de serem sujas ou não.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-212">Recalculates just the cells in the given range regardless of whether they are dirty or not.</span></span> <span data-ttu-id="9b5d9-213">O comportamento do método **Range.Calculate** foi alterado no Excel 2007; no entanto, o comportamento antigo ainda tem suporte no método **Range.CalculateRowMajorOrder**.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-213">Behavior of the **Range.Calculate** method changed in Excel 2007; however, the old behavior is still supported by the **Range.CalculateRowMajorOrder** method.</span></span> 
    
- <span data-ttu-id="9b5d9-214">**Automático Automático, Exceto Modos de Tabelas**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-214">**Automatic or Automatic Except Tables modes**</span></span>
    
    <span data-ttu-id="9b5d9-215">Recalcula a pasta de trabalho, mas não força o recálculo do intervalo nem de nenhuma célula no intervalo.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-215">Recalculates the workbook but does not force recalculation of the range or any cells in the range.</span></span>
    
### <a name="active-worksheet-calculation"></a><span data-ttu-id="9b5d9-216">Cálculo de Planilha Ativa</span><span class="sxs-lookup"><span data-stu-id="9b5d9-216">Active Worksheet Calculation</span></span>

<span data-ttu-id="9b5d9-217">Pressionamento de teclas: Shift+F9</span><span class="sxs-lookup"><span data-stu-id="9b5d9-217">Keystroke: SHIFT+F9</span></span>
  
<span data-ttu-id="9b5d9-218">VBA: **ActiveSheet.Calculate**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-218">VBA: **ActiveSheet.Calculate**</span></span>
  
<span data-ttu-id="9b5d9-219">API do C: **xlcCalculateDocument**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-219">C API: **xlcCalculateDocument**</span></span>
  
- <span data-ttu-id="9b5d9-220">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-220">**All modes**</span></span>
    
    <span data-ttu-id="9b5d9-221">Recalcula as células marcadas para cálculo somente na planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-221">Recalculates the cells marked for calculation in the active worksheet only.</span></span>
    
### <a name="specified-worksheet-calculation"></a><span data-ttu-id="9b5d9-222">Cálculo de Planilha Especificada</span><span class="sxs-lookup"><span data-stu-id="9b5d9-222">Specified Worksheet Calculation</span></span>

<span data-ttu-id="9b5d9-223">Pressionamento de teclas: nenhum</span><span class="sxs-lookup"><span data-stu-id="9b5d9-223">Keystroke: None</span></span>
  
<span data-ttu-id="9b5d9-224">VBA: **Worksheets(** reference **).Calculate**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-224">VBA: **Worksheets(** reference **).Calculate**</span></span>
  
<span data-ttu-id="9b5d9-225">API de C: sem suporte</span><span class="sxs-lookup"><span data-stu-id="9b5d9-225">C API: Not supported</span></span>
  
- <span data-ttu-id="9b5d9-226">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-226">**All modes**</span></span>
    
    <span data-ttu-id="9b5d9-227">Recalcula as células sujas e seus dependentes somente na planilha especificada.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-227">Recalculates the dirty cells and their dependents within the specified worksheet only.</span></span> <span data-ttu-id="9b5d9-228">Reference é o nome da planilha como uma cadeia de caracteres ou o número do índice na pasta de trabalho relevante.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-228">Reference is the name of the worksheet as a string or the index number in the relevant workbook.</span></span>
    
    <span data-ttu-id="9b5d9-229">O Excel 2000 e versões posteriores expõem uma propriedade de planilha **Boolean**, a propriedade **EnableCalculation**.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-229">Excel 2000 and later versions expose a **Boolean** worksheet property, the **EnableCalculation** property.</span></span> <span data-ttu-id="9b5d9-230">Configurar isso como **True** em vez de **False** faz com que todas as células na planilha especificada sejam sujas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-230">Setting this to **True** from **False** dirties all cells in the specified worksheet.</span></span> <span data-ttu-id="9b5d9-231">Nos modos automáticos, isso também dispara um recálculo de toda a pasta de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-231">In automatic modes, this also triggers a recalculation of the whole workbook.</span></span> 
    
    <span data-ttu-id="9b5d9-232">No modo manual, o código a seguir causa o recálculo somente da planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-232">In manual mode, the following code causes recalculation of the active sheet only.</span></span>
    
  ```vb
  With ActiveSheet
    .EnableCalculation = False
    .EnableCalculation = True
    .Calculate
  End With
  
  ```

### <a name="workbook-tree-rebuild-and-forced-recalculation"></a><span data-ttu-id="9b5d9-233">Reconstrução de Árvore de Pasta de Trabalho e Recálculo Forçado</span><span class="sxs-lookup"><span data-stu-id="9b5d9-233">Workbook Tree Rebuild and Forced Recalculation</span></span>

<span data-ttu-id="9b5d9-234">Pressionamento de teclas: Ctrl+Alt+Shift+F9 (introduzido no Excel 2002)</span><span class="sxs-lookup"><span data-stu-id="9b5d9-234">Keystroke: CTRL+ALT+SHIFT+F9 (introduced in Excel 2002)</span></span>
  
<span data-ttu-id="9b5d9-235">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduzido no Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="9b5d9-235">VBA: **Workbooks(** reference **).ForceFullCalculation** (introduced in Excel 2007)</span></span> 
  
<span data-ttu-id="9b5d9-236">API de C: sem suporte</span><span class="sxs-lookup"><span data-stu-id="9b5d9-236">C API: Not supported</span></span>
  
- <span data-ttu-id="9b5d9-237">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-237">**All modes**</span></span>
    
    <span data-ttu-id="9b5d9-238">Faz com que o Excel reconstrua a árvore de dependência e a cadeia de cálculo de determinada pasta de trabalho e força um recálculo de todas as células que contêm fórmulas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-238">Causes Excel to rebuild the dependency tree and the calculation chain for a given workbook and forces a recalculation of all cells that contain formulas.</span></span>
    
### <a name="all-open-workbooks"></a><span data-ttu-id="9b5d9-239">Todas as Pastas de Trabalho Abertas</span><span class="sxs-lookup"><span data-stu-id="9b5d9-239">All open workbooks</span></span>

<span data-ttu-id="9b5d9-240">Pressionamento de teclas: F9</span><span class="sxs-lookup"><span data-stu-id="9b5d9-240">Keystroke: F9</span></span>
  
<span data-ttu-id="9b5d9-241">VBA: **Application.Calculate**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-241">VBA: **Application.Calculate**</span></span>
  
<span data-ttu-id="9b5d9-242">API do C: **xlcCalculateNow**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-242">C API: **xlcCalculateNow**</span></span>
  
- <span data-ttu-id="9b5d9-243">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-243">**All modes**</span></span>
    
    <span data-ttu-id="9b5d9-244">Recalcula todas as células que o Excel marcou como sujas, isto é, dependentes de dados voláteis ou alterados e células programaticamente marcadas como sujas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-244">Specifies the calculation type to use. Possible values are:  This is a soft recalculation and is mainly for backwards compatibilty.  Recalculates all cells that Excel has marked as dirty, that is, dependents of volatile or changed data, and cells programmatically marked as dirty.  Recalculates all cells in all open workbooks.</span></span> <span data-ttu-id="9b5d9-245">Se o modo de cálculo é Automático, Exceto Tabelas, calcula as tabelas que exigem atualização e também todas as funções voláteis e seus dependentes.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-245">If the calculation mode is Automatic Except Tables, this calculates those tables that require updating and also all volatile functions and their dependents.</span></span>
    
### <a name="all-open-workbooks-tree-rebuild-and-forced-calculation"></a><span data-ttu-id="9b5d9-246">Reconstrução de Árvore de Todas as Pastas de Trabalho Abertas e Cálculo Forçado</span><span class="sxs-lookup"><span data-stu-id="9b5d9-246">All Open Workbooks Tree Rebuild and Forced Calculation</span></span>

<span data-ttu-id="9b5d9-247">Pressionamento de teclas: Ctrl+Alt+F9</span><span class="sxs-lookup"><span data-stu-id="9b5d9-247">Keystroke: CTRL+ALT+F9</span></span>
  
<span data-ttu-id="9b5d9-248">VBA: **Application.CalculateFull**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-248">VBA: **Application.CalculateFull**</span></span>
  
<span data-ttu-id="9b5d9-249">API de C: sem suporte</span><span class="sxs-lookup"><span data-stu-id="9b5d9-249">C API: Not supported</span></span>
  
- <span data-ttu-id="9b5d9-250">**Todos os modos**</span><span class="sxs-lookup"><span data-stu-id="9b5d9-250">**All modes**</span></span>
    
    <span data-ttu-id="9b5d9-251">Recalcula todas as células em todas as pastas de trabalho abertas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-251">Recalculates all cells in all open workbooks.</span></span> <span data-ttu-id="9b5d9-252">Se o modo de cálculo é Automático, Exceto Tabelas, força as tabelas a serem recalculadas.</span><span class="sxs-lookup"><span data-stu-id="9b5d9-252">If the calculation mode is Automatic Except Tables, it forces the tables to be recalculated.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9b5d9-253">Confira também</span><span class="sxs-lookup"><span data-stu-id="9b5d9-253">See also</span></span>



[<span data-ttu-id="9b5d9-254">Recálculo com vários threads no Excel</span><span class="sxs-lookup"><span data-stu-id="9b5d9-254">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="9b5d9-255">Tipos de dados usados pelo Excel</span><span class="sxs-lookup"><span data-stu-id="9b5d9-255">Data types used by Excel</span></span>](data-types-used-by-excel.md)
  
[<span data-ttu-id="9b5d9-256">Gerenciamento de Memória no Excel</span><span class="sxs-lookup"><span data-stu-id="9b5d9-256">Memory Management in Excel</span></span>](memory-management-in-excel.md)
  
[<span data-ttu-id="9b5d9-257">Conceitos de programação do Excel</span><span class="sxs-lookup"><span data-stu-id="9b5d9-257">Excel Programming Concepts</span></span>](excel-programming-concepts.md)

