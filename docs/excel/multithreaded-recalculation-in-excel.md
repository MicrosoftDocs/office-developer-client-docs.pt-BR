---
title: Recálculo multithreaded no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- células thread-safe [excel 2007],multithreading no Excel,tarefas simultâneas [Excel 2007],funções thread-safe [Excel 2007],recálculo multithreaded [Excel 2007],MTR [Excel 2007],funções XLL [Excel 2007], registrar como thread safe,recálculo [Excel 2007], multithreaded,contenção de memória [Excel 2007],registro de funções XLL como thread safe [Excel 2007],funções não seguras [Excel 2007]
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: f0b6f3d7310cac6d141fc74652a3333f70bda8e9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28720706"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="1b9b5-104">Recálculo multithreaded no Excel</span><span class="sxs-lookup"><span data-stu-id="1b9b5-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="1b9b5-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="1b9b5-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="1b9b5-106">O Microsoft Office Excel 2007 foi a primeira versão do Excel a usar o MTR (recálculo multithread) de planilhas.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-106">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets.</span></span> <span data-ttu-id="1b9b5-107">Você pode configurar o Excel para usar até 1.024 threads simultâneos ao recalcular, independentemente do número de processadores ou núcleos de processador no computador.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-107">You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1b9b5-108">Há uma sobrecarga do sistema operacional associada a cada thread. Portanto, você não deve configurar o Excel para usar mais threads do que o número necessário.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="1b9b5-109">Se o computador tiver vários processadores ou núcleos de processador, o sistema operacional será responsável pela alocação dos threads para os processadores da maneira mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="1b9b5-110">Visão geral do MTR do Excel</span><span class="sxs-lookup"><span data-stu-id="1b9b5-110">Excel MTR overview</span></span>

<span data-ttu-id="1b9b5-111">O Excel tenta identificar partes da cadeia de cálculo que podem ser recalculadas ao mesmo tempo em threads diferentes.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-111">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads.</span></span> <span data-ttu-id="1b9b5-112">A árvore muito simples a seguir (em que x ← y significa que y só depende de x) mostra um exemplo disso.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-112">The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="1b9b5-113">**Figura 1. Cálculo simultâneo em diferentes threads**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-113">**Calculating concurrently on different threads**</span></span>

<span data-ttu-id="1b9b5-114">![Cálculo simultâneo em diferentes threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Cálculo simultâneo em diferentes threads")</span><span class="sxs-lookup"><span data-stu-id="1b9b5-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="1b9b5-115">Após o cálculo de A1, A2 e A3 podem ser calculados em um thread, enquanto B1 e C1 podem ser calculados em outro, presumindo que as células sejam thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1b9b5-116">O termo célula thread-safe significa uma célula que contém apenas funções thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-116">The term thread-safe cell means a cell that only contains thread-safe functions.</span></span> <span data-ttu-id="1b9b5-117">O que é ou não thread-safe é detalhado em [O que é ou não considerado thread-safe pelo Excel](#xl2007xllsdk_threadsafe).</span><span class="sxs-lookup"><span data-stu-id="1b9b5-117">What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="1b9b5-118">A maioria das pastas de trabalho contém árvores de dependência bem mais complexas do que esse exemplo.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-118">Most practical workbooks contain far more complex dependency trees than this example.</span></span> <span data-ttu-id="1b9b5-119">Além disso, o momento do recálculo de uma célula não pode ser conhecido até um cálculo ser feito e pode variar muito, dependendo dos argumentos das funções.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-119">Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments.</span></span> <span data-ttu-id="1b9b5-120">Para obter os melhores resultados, o Excel tenta melhorar a ordem de cálculo em cada cálculo até que nenhuma otimização seja mais possível.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-120">To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="1b9b5-121">O Excel usa um único thread principal para executar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1b9b5-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="1b9b5-122">Comandos internos</span><span class="sxs-lookup"><span data-stu-id="1b9b5-122">Built-in commands</span></span>
    
- <span data-ttu-id="1b9b5-123">Comandos XLL</span><span class="sxs-lookup"><span data-stu-id="1b9b5-123">XLL commands</span></span>
    
- <span data-ttu-id="1b9b5-124">Funções da interface do Gerenciador de Suplementos XLL (função **xlAutoOpen** e assim por diante)</span><span class="sxs-lookup"><span data-stu-id="1b9b5-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="1b9b5-125">Comandos definidos pelo usuário (muitas vezes chamados de macros) do Microsoft VBA (Visual Basic for Applications)</span><span class="sxs-lookup"><span data-stu-id="1b9b5-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="1b9b5-126">Funções definidas pelo usuário do VBA</span><span class="sxs-lookup"><span data-stu-id="1b9b5-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="1b9b5-127">Funções de planilha thread-unsafe internas (confira a próxima seção para obter uma lista)</span><span class="sxs-lookup"><span data-stu-id="1b9b5-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="1b9b5-128">Funções e comandos definidos pelo usuário de planilha de macro XLM</span><span class="sxs-lookup"><span data-stu-id="1b9b5-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="1b9b5-129">Funções e comandos de suplemento COM</span><span class="sxs-lookup"><span data-stu-id="1b9b5-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="1b9b5-130">Funções e operadores em expressões de formatação condicional</span><span class="sxs-lookup"><span data-stu-id="1b9b5-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="1b9b5-131">Funções e operadores em definições de nome definido usadas em fórmulas de planilha</span><span class="sxs-lookup"><span data-stu-id="1b9b5-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="1b9b5-132">A avaliação forçada de uma expressão na caixa de edição de fórmula usando a tecla **F9**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="1b9b5-133">Todas as fórmulas de planilha, independentemente de as funções serem thread-safe ou não, são avaliadas no thread principal, a menos que o Excel esteja configurado para usar mais de um thread.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-133">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread.</span></span> <span data-ttu-id="1b9b5-134">Quando o usuário especifica que mais de um thread deve ser usado, os threads adicionais são usados para células thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-134">When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells.</span></span> <span data-ttu-id="1b9b5-135">O thread principal ainda pode ser usado para células thread-safe quando isso faz sentido do ponto de vista do balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-135">Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="1b9b5-136">Vale ressaltar que o Excel não executa mais de um comando de cada vez. Portanto, você não precisa adotar as mesmas precauções necessárias ao escrever funções thread-safe, como o uso de memória thread-local e seções críticas.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="1b9b5-137">O que é ou não considerado thread-safe pelo Excel</span><span class="sxs-lookup"><span data-stu-id="1b9b5-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="1b9b5-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="1b9b5-138"></span></span>

<span data-ttu-id="1b9b5-139">O Excel considera apenas o seguinte como thread-safe:</span><span class="sxs-lookup"><span data-stu-id="1b9b5-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="1b9b5-140">Todos os operadores unários e binários no Excel.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="1b9b5-141">Quase todas as funções de planilha internas, a partir do Excel 2007 (confira a lista de exceções)</span><span class="sxs-lookup"><span data-stu-id="1b9b5-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="1b9b5-142">Funções de suplemento XLL registradas explicitamente como thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="1b9b5-143">As funções de planilha internas que não são thread-safe são:</span><span class="sxs-lookup"><span data-stu-id="1b9b5-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="1b9b5-144">**FONÉTICA**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-144">**Phonetic**</span></span>
    
- <span data-ttu-id="1b9b5-145">**CÉL** quando o argumento "formato" ou "endereço" é usado</span><span class="sxs-lookup"><span data-stu-id="1b9b5-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="1b9b5-146">**INDIRETO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="1b9b5-147">**INFODADOSTABELADINÂMICA**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-147">**GetPivotData**</span></span>
    
- <span data-ttu-id="1b9b5-148">**MEMBROCUBO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="1b9b5-149">**VALORCUBO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="1b9b5-150">**PROPRIEDADEMEMBROCUBO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="1b9b5-151">**CONJUNTOCUBO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-151">**CUBESET**</span></span>
    
- <span data-ttu-id="1b9b5-152">**MEMBROCLASSIFICADOCUBO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="1b9b5-153">**MEMBROKPICUBO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="1b9b5-154">**CONTAGEMCONJUNTOCUBO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="1b9b5-155">**ENDEREÇO** quando o quinto parâmetro (nome_da_planilha) é fornecido</span><span class="sxs-lookup"><span data-stu-id="1b9b5-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="1b9b5-156">Qualquer função de banco de dados (**BDSOMA**, **BDMÉDIA** e assim por diante) que se refere a uma tabela dinâmica</span><span class="sxs-lookup"><span data-stu-id="1b9b5-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="1b9b5-157">**TIPO.ERRO**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-157">**ErrorType**</span></span>
    
- <span data-ttu-id="1b9b5-158">**HIPERLINK**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-158">**Hyperlink**</span></span>
    
<span data-ttu-id="1b9b5-159">Em termos explícitos, os seguintes itens são considerados não seguros:</span><span class="sxs-lookup"><span data-stu-id="1b9b5-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="1b9b5-160">Funções definidas pelo usuário do VBA</span><span class="sxs-lookup"><span data-stu-id="1b9b5-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="1b9b5-161">Funções definidas pelo usuário de suplemento COM</span><span class="sxs-lookup"><span data-stu-id="1b9b5-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="1b9b5-162">Funções definidas pelo usuário de planilha de macro XLM</span><span class="sxs-lookup"><span data-stu-id="1b9b5-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="1b9b5-163">Funções de suplementos XLL não explicitamente registradas como thread-safe</span><span class="sxs-lookup"><span data-stu-id="1b9b5-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="1b9b5-164">As implicações são que as operações e funções a seguir não são thread-safe e falham se são chamadas de uma função XLL registrada como thread-safe:</span><span class="sxs-lookup"><span data-stu-id="1b9b5-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="1b9b5-165">Chamadas para funções de informações XLM; por exemplo, **xlfGetCell** (**OBTER.CÉLULA**).</span><span class="sxs-lookup"><span data-stu-id="1b9b5-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="1b9b5-166">Chamadas para **xlfSetName** (**DEF.NOME**) para definir ou excluir nomes internos XLL.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="1b9b5-167">Chamadas para funções definidas pelo usuário thread-unsafe usando **xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="1b9b5-168">Chamadas para a função [xlfEvaluate](xlfevaluate.md) para expressões que contenham funções thread-unsafe ou que contenham nomes definidos cujas definições contenham funções thread-unsafe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="1b9b5-169">Chamadas para a função [xlAbort](xlabort.md) para limpar uma condição de interrupção.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="1b9b5-170">Chamadas para a função [xlCoerce](xlcoerce.md) para obter o valor de uma referência de célula não calculada.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="1b9b5-171">Funções de planilha XLL não podem chamar comandos da API de C, por exemplo, **xlcSave**, independentemente de terem sido registradas como thread-safe ou não.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="1b9b5-172">Considerando que funções XLL declaradas como thread-safe não podem chamar funções de informações XLM ou referenciar células não calculadas, o Excel não permite que funções XLL registradas como equivalentes de planilha de macro também sejam registradas como thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-172">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe.</span></span> <span data-ttu-id="1b9b5-173">Portanto, a tentativa de obter o valor de uma referência de célula não calculada usando **xlCoerce** falha com um erro **xlretUncalced**.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-173">Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error.</span></span> <span data-ttu-id="1b9b5-174">A chamada de uma função de informações XLM falha com um erro **xlretFailed**.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-174">Calling an XLM information function fails with an **xlretFailed** error.</span></span> <span data-ttu-id="1b9b5-175">Os outros pontos listados anteriormente falham com um código de erro introduzido na API de C do Excel: **xlretNotThreadSafe**.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-175">The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="1b9b5-176">Todas as funções de retorno de chamada somente de API de C são thread-safe:</span><span class="sxs-lookup"><span data-stu-id="1b9b5-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="1b9b5-177">**xlCoerce** (exceto se a coerção de referências de célula não calculada falhar)</span><span class="sxs-lookup"><span data-stu-id="1b9b5-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="1b9b5-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-178">**xlFree**</span></span>
    
- <span data-ttu-id="1b9b5-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-179">**xlStack**</span></span>
    
- <span data-ttu-id="1b9b5-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="1b9b5-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="1b9b5-182">**xlAbort** (exceto quando usada para limpar uma condição de interrupção)</span><span class="sxs-lookup"><span data-stu-id="1b9b5-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="1b9b5-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="1b9b5-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="1b9b5-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="1b9b5-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="1b9b5-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="1b9b5-187">A única exceção é a função **xlSet** que, de qualquer forma, é um equivalente de comando e, portanto, não pode ser chamada de nenhuma função de planilha.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="1b9b5-188">Uma função de planilha XLL pode ser registrada no Excel como thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-188">An XLL worksheet function can be registered with Excel as thread safe.</span></span> <span data-ttu-id="1b9b5-189">Isso informa ao Excel que a função pode ser chamada com segurança e simultaneamente em vários threads, embora você deva verificar se esse realmente é o caso.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-189">This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case.</span></span> <span data-ttu-id="1b9b5-190">Você poderá possivelmente desestabilizar o Excel se uma função registrada como thread-safe se comportar de forma não segura.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-190">You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="1b9b5-191">Registrar funções XLL como thread-safe</span><span class="sxs-lookup"><span data-stu-id="1b9b5-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="1b9b5-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="1b9b5-192"></span></span>

<span data-ttu-id="1b9b5-193">As regras que um desenvolvedor deve cumprir ao escrever funções thread-safe são:</span><span class="sxs-lookup"><span data-stu-id="1b9b5-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="1b9b5-194">Não chamar recursos em outras DLLs que possam não ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="1b9b5-195">Não fazer chamadas thread-unsafe por meio da API de C ou COM.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="1b9b5-196">Proteger os recursos que podem ser usados simultaneamente por mais de um thread usando seções críticas.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="1b9b5-197">Usar memória local de thread para armazenamento específico de thread e substituir variáveis estáticas em funções por variáveis locais de thread.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="1b9b5-198">O Excel impõe uma restrição adicional: funções thread-safe não podem ser registradas como equivalentes de planilha de macro e, assim, não podem chamar funções de informações XLM nem obter os valores de células não recalculadas.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="1b9b5-199">Contenção de memória</span><span class="sxs-lookup"><span data-stu-id="1b9b5-199">Memory contention</span></span>
<span data-ttu-id="1b9b5-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="1b9b5-200"></span></span>

<span data-ttu-id="1b9b5-201">Sistemas multi-threaded devem resolver dois problemas fundamentais:</span><span class="sxs-lookup"><span data-stu-id="1b9b5-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="1b9b5-202">Como proteger a memória que deve ser lida ou gravada por mais de um thread.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="1b9b5-203">Como criar e acessar a memória que é associada e, assim, privada para o thread de execução.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="1b9b5-204">O sistema operacional Windows e o SDK (Software Development Kit) do Windows oferecem ferramentas para ambos os itens: seções críticas e a API de TLS (armazenamento local de thread), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-204">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively.</span></span> <span data-ttu-id="1b9b5-205">Saiba mais em [Gerenciamento de Memória no Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="1b9b5-205">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="1b9b5-206">O primeiro problema pode ocorrer, por exemplo, quando duas funções de planilha (ou duas instâncias de execução simultânea da mesma função) precisam acessar ou modificar uma variável global em um projeto de DLL.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-206">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project.</span></span> <span data-ttu-id="1b9b5-207">Essa variável global pode estar oculta em uma instância globalmente acessível de um objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-207">Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="1b9b5-208">O segundo problema pode ocorrer, por exemplo, quando uma função de planilha declara uma variável estática ou um objeto no código do corpo da função.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-208">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code.</span></span> <span data-ttu-id="1b9b5-209">O compilador de C/C++ apenas cria uma única cópia que todos os threads usam.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-209">The C/C++ compiler only creates a single copy that all threads use.</span></span> <span data-ttu-id="1b9b5-210">Isso significa que uma instância da função pode alterar o valor, enquanto outra em um thread diferente pode supor que o valor é o que estava definido antes.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-210">This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="1b9b5-211">Exemplos de aplicações de MTR</span><span class="sxs-lookup"><span data-stu-id="1b9b5-211">Example applications of MTR</span></span>
<span data-ttu-id="1b9b5-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="1b9b5-212"></span></span>

<span data-ttu-id="1b9b5-213">Qualquer XLL que exporta funções de planilha pode aproveitar o MTR (recálculo multi-threaded) no Excel, desde que essas funções não precisem executar ações thread-unsafe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-213">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions.</span></span> <span data-ttu-id="1b9b5-214">Isso habilita o Excel a recalcular pastas de trabalho que dependem delas o mais reapidamente possível e, portanto, desejável, seja qual for o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-214">This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="1b9b5-215">Especificamente, o MTR tem enorme impacto em relação ao tempo de recálculo de pastas de trabalho que chamam UDFs (funções definidas pelo usuário) que, por sua vez, chamam processos externos para obter o resultado desejado.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-215">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result.</span></span> <span data-ttu-id="1b9b5-216">Em particular, considere uma UDF que chama um servidor remoto que pode processar várias solicitações ao mesmo tempo e uma pasta de trabalho que contém muitas chamadas para essa função.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-216">In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function.</span></span> <span data-ttu-id="1b9b5-217">Se o recálculo da pasta de trabalho for single-threaded, cada chamada à UDF e, assim, ao servidor remoto, deverá ser concluída para que a chamada seguinte possa ser feita.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-217">If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made.</span></span> <span data-ttu-id="1b9b5-218">Isso desperdiça a capacidade do servidor de processar várias chamadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-218">This wastes the server's ability to process many calls at once.</span></span> <span data-ttu-id="1b9b5-219">Se o recálculo da pasta de trabalho for multi-threaded, o Excel poderá fazer várias chamadas ao mesmo tempo ou em sequência rápida.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-219">If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="1b9b5-220">Se o Excel estiver configurado para usar o mesmo número de threads que o servidor (vamos chamar isso de N) e a topologia da árvore de dependência da pasta de trabalho o permitir, o tempo total de recálculo poderá ser reduzido para algo próximo de 1/N do tempo de cálculo single-threaded.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-220">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time.</span></span> <span data-ttu-id="1b9b5-221">Isso pode ocorrer até mesmo quando o computador cliente (em que a pasta de trabalho está sendo executada) tem apenas um processador, especialmente quando o tempo necessário para fazer a chamada ao servidor é pequeno em relação ao tempo necessário para o servidor processar a chamada.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-221">This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="1b9b5-222">Há sobrecarga do sistema operacional para cada thread adicional.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-222">There is operating system overhead for each additional thread.</span></span> <span data-ttu-id="1b9b5-223">Portanto, pode ser necessário testar um pouco para que determinada pasta de trabalho, servidor e computador cliente encontrem o número ideal de threads que o Excel deve ser instruído a usar.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-223">Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="1b9b5-224">Por exemplo, considere um computador com processador único que esteja executando o Excel e uma pasta de trabalho que contenha 1.000 células.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-224">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells.</span></span> <span data-ttu-id="1b9b5-225">Ele chama uma UDF que, por sua vez, chama um ou mais servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-225">It calls a UDF, which in turn calls one or more remote servers.</span></span> <span data-ttu-id="1b9b5-226">Suponha que as 1.000 células não dependam umas das outras. Portanto, o Excel não precisa esperar até que uma chamada seja concluída antes de chamar a próxima.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-226">Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next.</span></span> <span data-ttu-id="1b9b5-227">É possível ter alguma flexibilidade para essa restrição sem afetar esse exemplo. Se os servidores podem processar 100 solicitações simultaneamente, e o Excel está configurado para usar 100 threads, o tempo de execução pode ser reduzido para apenas 1/100 disso, em que apenas um thread é usado.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-227">(Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used.</span></span> <span data-ttu-id="1b9b5-228">A sobrecarga que ocorre quando o Excel aloca chamadas para cada thread e o sistema operacional gerencia 100 threads significa que, na prática, a redução não será tão elevada.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-228">The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great.</span></span> <span data-ttu-id="1b9b5-229">Também existe a suposição implícita de que o servidor é bem dimensionado e, se for solicitado a processar 100 tarefas ao mesmo tempo, isso não afetará os tempos de conclusão de tarefas individuais significativamente.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-229">There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="1b9b5-230">Uma aplicação prática em que essa técnica pode oferecer uma vantagem importante refere-se aos métodos Monte Carlo, bem como a outras tarefas com grande volume de números, que podem ser divididas em subtarefas menores que podem ser delegadas a servidores.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="1b9b5-231">Considerações sobre os Serviços do Excel</span><span class="sxs-lookup"><span data-stu-id="1b9b5-231">Excel Services considerations</span></span>
<span data-ttu-id="1b9b5-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="1b9b5-232"></span></span>

<span data-ttu-id="1b9b5-233">Os Serviços do Excel dão suporte ao carregamento, ao cálculo e à renderização de planilhas do Excel em um servidor.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-233">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server.</span></span> <span data-ttu-id="1b9b5-234">Os usuários podem acessar e interagir com as planilhas usando ferramentas de navegador padrão.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-234">Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="1b9b5-235">UDFs dos Serviços do Excel são criadas usando o código gerenciado do Microsoft .NET Framework e disponibilizados por meio de um assembly do .NET.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-235">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly.</span></span> <span data-ttu-id="1b9b5-236">XLLs não têm suporte nos Serviços do Excel.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-236">XLLs are not supported by Excel Services.</span></span> <span data-ttu-id="1b9b5-237">Um recurso de UDF de servidor de código gerenciado pode chamar um XLL para acessar sua funcionalidade, para que o usuário possa ter a mesma funcionalidade com uma pasta de trabalho carregada servidor no servidor que obteria com uma pasta de trabalho carregada no cliente.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-237">A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="1b9b5-238">Para disponibilizar as funções XLL dessa maneira, elas devem ser encapsuladas em um assembly do .NET que converta argumentos e retorne valores dos tipos de dados nativos para os tipos de dados gerenciados do .NET Framework e chame as funções XLL.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-238">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions.</span></span> <span data-ttu-id="1b9b5-239">O wrapper do .NET deve exportar uma UDF de servidor para cada função XLL que é acessada.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-239">The .NET wrapper would export one server UDF for each XLL function being accessed.</span></span> <span data-ttu-id="1b9b5-240">Um requisito adicional é que as funções XLL chamadas dessa maneira devem ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-240">An additional requirement is that any XLL functions called in this way must be thread safe.</span></span> <span data-ttu-id="1b9b5-241">Como as funções XLL não são registradas como ocorre no cliente Excel, o servidor e o wrapper do .NET não têm nenhuma maneira de impor que elas sejam thread-safe.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-241">Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe.</span></span> <span data-ttu-id="1b9b5-242">É responsabilidade do desenvolvedor de XLL garantir isso.</span><span class="sxs-lookup"><span data-stu-id="1b9b5-242">It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1b9b5-243">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b9b5-243">See also</span></span>

- [<span data-ttu-id="1b9b5-244">Recálculo do Excel</span><span class="sxs-lookup"><span data-stu-id="1b9b5-244">Excel recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="1b9b5-245">Gerenciamento de Memória no Excel</span><span class="sxs-lookup"><span data-stu-id="1b9b5-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- [<span data-ttu-id="1b9b5-246">Acessar o código de XLL no Excel</span><span class="sxs-lookup"><span data-stu-id="1b9b5-246">Accessing XLL code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="1b9b5-247">Conceitos de programação do Excel</span><span class="sxs-lookup"><span data-stu-id="1b9b5-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="1b9b5-248">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="1b9b5-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

