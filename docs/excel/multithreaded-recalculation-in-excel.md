---
title: Recálculo multithreaded no Excel
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
keywords:
- células de thread-safe [excel 2007], multithreading no Excel, tarefas simultâneas [Excel 2007], funções thread-safe [Excel 2007], recálculo multithreaded [Excel 2007], MTR [Excel 2007], funções XLL [Excel 2007], registrando como thread-safe, [recálculo Excel 2007], memória multithreaded, contenção [Excel 2007], registrando XLL funciona como thread seguras funções inseguras [Excel 2007], [Excel 2007]
localization_priority: Normal
ms.assetid: c6c831f1-4be1-4dcc-a0fa-c26052ec53c9
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 010a1029e0bf5ba1a36b324ebd402f6e90603fb9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765425"
---
# <a name="multithreaded-recalculation-in-excel"></a><span data-ttu-id="2a979-104">Recálculo multithreaded no Excel</span><span class="sxs-lookup"><span data-stu-id="2a979-104">Multithreaded recalculation in Excel</span></span>

<span data-ttu-id="2a979-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2a979-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2a979-106">Microsoft Office Excel 2007 era a primeira versão do Excel use o recálculo multithreaded (MTR) das planilhas.</span><span class="sxs-lookup"><span data-stu-id="2a979-106">Microsoft Office Excel 2007 was the first version of Excel to use multithreaded recalculation (MTR) of worksheets.</span></span> <span data-ttu-id="2a979-107">Você pode configurar o Excel use até segmentos simultâneos de 1024 quando recalcular, independentemente do número de processadores ou núcleos de processador no computador.</span><span class="sxs-lookup"><span data-stu-id="2a979-107">You can configure Excel to use up to 1024 concurrent threads when recalculating, regardless of the number of processors or processor cores on the computer.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2a979-108">Há um sistema operacional sobrecarga associado com cada segmento, portanto você não deve configurar o Excel para usar mais threads do que você precisa.</span><span class="sxs-lookup"><span data-stu-id="2a979-108">There is an operating system overhead associated with each thread, so you should not configure Excel to use more threads than you need.</span></span> 
  
<span data-ttu-id="2a979-109">Se o computador tiver vários processadores ou núcleos de processador, o sistema operacional leva a responsabilidade para alocar os threads aos processadores da maneira mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="2a979-109">If the computer has multiple processors or processor cores, the operating system takes responsibility for allocating the threads to the processors in the most efficient way.</span></span>
  
## <a name="excel-mtr-overview"></a><span data-ttu-id="2a979-110">Visão geral do Excel MTR</span><span class="sxs-lookup"><span data-stu-id="2a979-110">Excel MTR overview</span></span>

<span data-ttu-id="2a979-111">Excel tenta identificar partes da cadeia de cálculo que podem ser recalculadas simultaneamente em threads diferentes.</span><span class="sxs-lookup"><span data-stu-id="2a979-111">Excel tries to identify parts of the calculation chain that can be recalculated concurrently on different threads.</span></span> <span data-ttu-id="2a979-112">A seguinte árvore muito simple (onde y x ← significa y depende somente x) mostra um exemplo disso.</span><span class="sxs-lookup"><span data-stu-id="2a979-112">The following very simple tree (where x ← y means y only depends on x) shows an example of this.</span></span>
  
<span data-ttu-id="2a979-113">**Figura 1. Calculando simultaneamente em threads diferentes**</span><span class="sxs-lookup"><span data-stu-id="2a979-113">**Figure 1. Calculating concurrently on different threads**</span></span>

<span data-ttu-id="2a979-114">![Calculando simultaneamente em threads diferentes] (media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculando simultaneamente em threads diferentes")</span><span class="sxs-lookup"><span data-stu-id="2a979-114">![Calculating concurrently on different threads](media/12b5a52b-6308-420c-b6cf-492bd1f195ce.gif "Calculating concurrently on different threads")</span></span>
  
<span data-ttu-id="2a979-115">Depois que é calculado A1, A2 e, em seguida, A3 podem ser calculado em um segmento, enquanto B1 e, em seguida, C1 podem ser calculado em outro, supondo que todas as células são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-115">After A1 is calculated, A2 and then A3 can be calculated on one thread, while B1 and then C1 can be calculated on another, assuming all the cells are thread safe.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="2a979-116">A célula de thread-safe termo significa que uma célula que contém apenas as funções thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-116">The term thread-safe cell means a cell that only contains thread-safe functions.</span></span> <span data-ttu-id="2a979-117">O que é e não é thread-safe são detalhados [What ' s e é não considerado Thread seguros pelo Excel](#xl2007xllsdk_threadsafe).</span><span class="sxs-lookup"><span data-stu-id="2a979-117">What is and is not thread-safe is detailed [What Is and Is Not Considered Thread Safe by Excel](#xl2007xllsdk_threadsafe).</span></span> 
  
<span data-ttu-id="2a979-118">Pastas de trabalho mais práticas contêm árvores de dependência muito mais complexas do que esse exemplo.</span><span class="sxs-lookup"><span data-stu-id="2a979-118">Most practical workbooks contain far more complex dependency trees than this example.</span></span> <span data-ttu-id="2a979-119">Além disso, o tempo de recálculo de uma célula não pode ser conhecido até que um cálculo é feito e pode variar bastante dependendo argumentos das funções.</span><span class="sxs-lookup"><span data-stu-id="2a979-119">Moreover, the recalculation time of a cell cannot be known until a calculation is done and can vary greatly depending on the functions' arguments.</span></span> <span data-ttu-id="2a979-120">Para obter os melhores resultados, o Excel tenta melhorar a ordem de cálculo em cada cálculo até sem otimização adicional é possível.</span><span class="sxs-lookup"><span data-stu-id="2a979-120">To obtain the best results, Excel tries to improve the calculation order on every calculation until no further optimization is possible.</span></span>
  
<span data-ttu-id="2a979-121">Excel usa um único segmento principal para executar ou executar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2a979-121">Excel uses a single main thread to run or execute the following:</span></span>
  
- <span data-ttu-id="2a979-122">Comandos internos</span><span class="sxs-lookup"><span data-stu-id="2a979-122">Built-in commands</span></span>
    
- <span data-ttu-id="2a979-123">Comandos XLL</span><span class="sxs-lookup"><span data-stu-id="2a979-123">XLL commands</span></span>
    
- <span data-ttu-id="2a979-124">Funções de interface do Gerenciador de suplementos XLL (função**xlAutoOpen** e assim por diante)</span><span class="sxs-lookup"><span data-stu-id="2a979-124">XLL Add-in Manager interface functions (**xlAutoOpen** function, and so on)</span></span> 
    
- <span data-ttu-id="2a979-125">Microsoft Visual Basic para comandos definida pelo usuário de Applications (VBA) (geralmente conhecidos como macros)</span><span class="sxs-lookup"><span data-stu-id="2a979-125">Microsoft Visual Basic for Applications (VBA) user-defined commands (often referred to as macros)</span></span>
    
- <span data-ttu-id="2a979-126">Funções definidas pelo usuário do VBA</span><span class="sxs-lookup"><span data-stu-id="2a979-126">VBA user-defined functions</span></span>
    
- <span data-ttu-id="2a979-127">Funções de planilha não seguros thread internas (consulte a próxima seção para obter uma lista)</span><span class="sxs-lookup"><span data-stu-id="2a979-127">Built-in thread-unsafe worksheet functions (see the next section for a list)</span></span>
    
- <span data-ttu-id="2a979-128">Funções e definidas pelo usuário comandos de folha de macro XLM</span><span class="sxs-lookup"><span data-stu-id="2a979-128">XLM macro sheet user-defined commands and functions</span></span>
    
- <span data-ttu-id="2a979-129">Funções e comandos do suplemento de COM</span><span class="sxs-lookup"><span data-stu-id="2a979-129">COM add-in commands and functions</span></span>
    
- <span data-ttu-id="2a979-130">Funções e operadores em expressões de formatação condicionais</span><span class="sxs-lookup"><span data-stu-id="2a979-130">Functions and operators within conditional formatting expressions</span></span>
    
- <span data-ttu-id="2a979-131">Funções e operadores dentro das definições de nome definido usadas em fórmulas de planilha</span><span class="sxs-lookup"><span data-stu-id="2a979-131">Functions and operators within defined name definitions used in worksheet formulas</span></span>
    
- <span data-ttu-id="2a979-132">Avaliação de uma expressão na caixa Editar fórmula usando a tecla **F9** forçada</span><span class="sxs-lookup"><span data-stu-id="2a979-132">The forced evaluation of an expression in the formula-edit box using the **F9** key</span></span> 
    
<span data-ttu-id="2a979-133">Todas as fórmulas de planilha, independentemente se as funções estão thread-safe ou não, são avaliadas no thread principal, a menos que o Excel está configurado para usar mais de um segmento.</span><span class="sxs-lookup"><span data-stu-id="2a979-133">All worksheet formulas, regardless of whether the functions are thread safe or not, are evaluated on the main thread unless Excel is configured to use more than one thread.</span></span> <span data-ttu-id="2a979-134">Quando o usuário Especifica o que mais de um segmento deve ser usado, os threads adicionais são usados para as células de thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-134">When the user specifies that more than one thread should be used, the additional threads are used for thread-safe cells.</span></span> <span data-ttu-id="2a979-135">Observe que o thread principal ainda pode ser usado para as células de thread-safe quando fizer sentido do ponto de vista balanceamento de carga.</span><span class="sxs-lookup"><span data-stu-id="2a979-135">Note that the main thread may still be used for thread-safe cells when it makes sense from a load-balancing point of view.</span></span>
  
<span data-ttu-id="2a979-136">Vale precisar reiniciar que Excel não fique mais de um comando ao mesmo tempo, portanto você não precisa empregar as mesmas precauções como quando você estiver escrevendo funções thread-safe, como o uso de memória local de segmento e seções críticas.</span><span class="sxs-lookup"><span data-stu-id="2a979-136">It is worth restating that Excel does not run more than one command at once, so you do not need to employ the same precautions as when you are writing thread-safe functions, such as the use of thread-local memory and critical sections.</span></span>
  
## <a name="what-is-and-is-not-considered-thread-safe-by-excel"></a><span data-ttu-id="2a979-137">O que é e não é considerado thread seguros pelo Excel</span><span class="sxs-lookup"><span data-stu-id="2a979-137">What is and is not considered thread safe by Excel</span></span>
<span data-ttu-id="2a979-138"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="2a979-138"></span></span>

<span data-ttu-id="2a979-139">Excel considera apenas o seguinte procedimento ao thread seguro:</span><span class="sxs-lookup"><span data-stu-id="2a979-139">Excel only considers the following as thread safe:</span></span>
  
- <span data-ttu-id="2a979-140">Todos os operadores unário e binário no Excel.</span><span class="sxs-lookup"><span data-stu-id="2a979-140">All unary and binary operators in Excel.</span></span>
    
- <span data-ttu-id="2a979-141">Quase todas as funções de planilha internas iniciada no Excel 2007 (consulte a lista de exceções)</span><span class="sxs-lookup"><span data-stu-id="2a979-141">Almost all built-in worksheet functions starting in Excel 2007 (see exceptions list)</span></span>
    
- <span data-ttu-id="2a979-142">Suplemento funções XLL que foram registradas explicitamente como thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-142">XLL add-in functions that have been explicitly registered as thread-safe.</span></span>
    
<span data-ttu-id="2a979-143">As funções de planilha internas que não são thread-safe são:</span><span class="sxs-lookup"><span data-stu-id="2a979-143">The built-in worksheet functions that are not thread safe are:</span></span>
  
- <span data-ttu-id="2a979-144">**FONÉTICO**</span><span class="sxs-lookup"><span data-stu-id="2a979-144">**PHONETIC**</span></span>
    
- <span data-ttu-id="2a979-145">**CÉLULA** quando o argumento do "formato" ou "address" é usado</span><span class="sxs-lookup"><span data-stu-id="2a979-145">**CELL** when either the "format" or "address" argument is used</span></span> 
    
- <span data-ttu-id="2a979-146">**INDIRETAS**</span><span class="sxs-lookup"><span data-stu-id="2a979-146">**INDIRECT**</span></span>
    
- <span data-ttu-id="2a979-147">**GETPIVOTDATA**</span><span class="sxs-lookup"><span data-stu-id="2a979-147">**GETPIVOTDATA**</span></span>
    
- <span data-ttu-id="2a979-148">**CUBEMEMBER**</span><span class="sxs-lookup"><span data-stu-id="2a979-148">**CUBEMEMBER**</span></span>
    
- <span data-ttu-id="2a979-149">**CUBEVALUE**</span><span class="sxs-lookup"><span data-stu-id="2a979-149">**CUBEVALUE**</span></span>
    
- <span data-ttu-id="2a979-150">**CUBEMEMBERPROPERTY**</span><span class="sxs-lookup"><span data-stu-id="2a979-150">**CUBEMEMBERPROPERTY**</span></span>
    
- <span data-ttu-id="2a979-151">**CUBESET**</span><span class="sxs-lookup"><span data-stu-id="2a979-151">**CUBESET**</span></span>
    
- <span data-ttu-id="2a979-152">**CUBERANKEDMEMBER**</span><span class="sxs-lookup"><span data-stu-id="2a979-152">**CUBERANKEDMEMBER**</span></span>
    
- <span data-ttu-id="2a979-153">**CUBEKPIMEMBER**</span><span class="sxs-lookup"><span data-stu-id="2a979-153">**CUBEKPIMEMBER**</span></span>
    
- <span data-ttu-id="2a979-154">**CUBESETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="2a979-154">**CUBESETCOUNT**</span></span>
    
- <span data-ttu-id="2a979-155">**Endereço** onde o quinto parâmetro (o sheet_name) é fornecido</span><span class="sxs-lookup"><span data-stu-id="2a979-155">**ADDRESS** where the fifth parameter (the sheet_name) is given</span></span> 
    
- <span data-ttu-id="2a979-156">Qualquer função de banco de dados (**DSUM**, **BDMÉDIA**e assim por diante) que se refere a uma tabela dinâmica</span><span class="sxs-lookup"><span data-stu-id="2a979-156">Any database function (**DSUM**, **DAVERAGE**, and so on) that refers to a pivot table</span></span>
    
- <span data-ttu-id="2a979-157">**ERRO. TIPO**</span><span class="sxs-lookup"><span data-stu-id="2a979-157">**ERROR.TYPE**</span></span>
    
- <span data-ttu-id="2a979-158">**HIPERLINK**</span><span class="sxs-lookup"><span data-stu-id="2a979-158">**HYPERLINK**</span></span>
    
<span data-ttu-id="2a979-159">Para ser explícitas, a seguir é considerada inseguros:</span><span class="sxs-lookup"><span data-stu-id="2a979-159">To be explicit, the following are considered to be unsafe:</span></span>
  
- <span data-ttu-id="2a979-160">Funções definidas pelo usuário do VBA</span><span class="sxs-lookup"><span data-stu-id="2a979-160">VBA user-defined functions</span></span>
    
- <span data-ttu-id="2a979-161">COM suplemento-funções definidas pelo usuário</span><span class="sxs-lookup"><span data-stu-id="2a979-161">COM add-in user-defined functions</span></span>
    
- <span data-ttu-id="2a979-162">Funções definidas pelo usuário de folha de macro XLM</span><span class="sxs-lookup"><span data-stu-id="2a979-162">XLM macro-sheet user-defined functions</span></span>
    
- <span data-ttu-id="2a979-163">Funções de Suplemento XLL não explicitamente registrado como thread-safe</span><span class="sxs-lookup"><span data-stu-id="2a979-163">XLL add-in functions not explicitly registered as thread safe</span></span>
    
<span data-ttu-id="2a979-164">As implicações são que as operações e funções a seguir não são thread-safe e falharem se eles forem chamados de uma função XLL registrada como thread-safe:</span><span class="sxs-lookup"><span data-stu-id="2a979-164">The implications are that the following operations and functions are not thread-safe, and fail if they are called from an XLL function registered as thread safe:</span></span>
  
- <span data-ttu-id="2a979-165">Chamadas para funções de informações XLM, por exemplo, **xlfGetCell** (**GET. CÉLULA**).</span><span class="sxs-lookup"><span data-stu-id="2a979-165">Calls to XLM information functions, for example, **xlfGetCell** (**GET.CELL**).</span></span>
    
- <span data-ttu-id="2a979-166">Chamadas para **xlfSetName** (**SET.NAME**) para definir ou excluir os nomes internos XLL.</span><span class="sxs-lookup"><span data-stu-id="2a979-166">Calls to **xlfSetName** (**SET.NAME**) to define or delete XLL-internal names.</span></span>
    
- <span data-ttu-id="2a979-167">Chamadas para funções definidas pelo usuário de thread-inseguras usando **xlUDF**.</span><span class="sxs-lookup"><span data-stu-id="2a979-167">Calls to thread-unsafe user-defined functions using **xlUDF**.</span></span>
    
- <span data-ttu-id="2a979-168">Chamadas para a função [xlfEvaluate](xlfevaluate.md) para expressões que contêm funções thread-inseguras ou que contêm nomes definidos cujas definições contêm funções thread-inseguros.</span><span class="sxs-lookup"><span data-stu-id="2a979-168">Calls to the [xlfEvaluate](xlfevaluate.md) function for expressions that contain thread-unsafe functions or that contain defined names whose definitions contain thread-unsafe functions.</span></span> 
    
- <span data-ttu-id="2a979-169">Chamadas para a função [xlAbort](xlabort.md) para limpar uma condição de quebra.</span><span class="sxs-lookup"><span data-stu-id="2a979-169">Calls to the [xlAbort](xlabort.md) function to clear a break condition.</span></span> 
    
- <span data-ttu-id="2a979-170">Chamadas para a função [xlCoerce](xlcoerce.md) para obter o valor de uma referência de célula não calculadas.</span><span class="sxs-lookup"><span data-stu-id="2a979-170">Calls to the [xlCoerce](xlcoerce.md) function to get the value of an uncalculated cell reference.</span></span> 
    
> [!NOTE]
> <span data-ttu-id="2a979-171">Funções de planilha XLL não têm permissão para chamar os comandos do C API, por exemplo, **xlcSave**, independentemente se eles tiverem sido registrados como thread-safe ou não.</span><span class="sxs-lookup"><span data-stu-id="2a979-171">XLL worksheet functions are not permitted to call C API commands, for example, **xlcSave**, regardless of whether they have been registered as thread safe or not.</span></span> 
  
<span data-ttu-id="2a979-172">Visto que as funções XLL declaradas como thread-safe não é possível chamar funções de informações XLM ou referência a células não calculadas, Excel não permite que as funções XLL registrados como equivalentes de folha de macro para também ser registrada como thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-172">Given that XLL functions declared as thread safe cannot call XLM information functions or reference uncalculated cells, Excel does not permit XLL functions that are registered as macro sheet equivalents to also be registered as thread safe.</span></span> <span data-ttu-id="2a979-173">Portanto, a tentativa de obter o valor de uma referência de célula não calculadas usando **xlCoerce** falha com um erro de **xlretUncalced** .</span><span class="sxs-lookup"><span data-stu-id="2a979-173">Therefore attempting to get the value of an uncalculated cell reference using **xlCoerce** fails with an **xlretUncalced** error.</span></span> <span data-ttu-id="2a979-174">Função de informações chamar um XLM falhará com um erro **xlretFailed** .</span><span class="sxs-lookup"><span data-stu-id="2a979-174">Calling an XLM information function fails with an **xlretFailed** error.</span></span> <span data-ttu-id="2a979-175">Os outros pontos listados anteriormente falharem com um código de erro introduzido do C API do Excel: **xlretNotThreadSafe**.</span><span class="sxs-lookup"><span data-stu-id="2a979-175">The other points listed previously fail with an error code introduced in the Excel C API: **xlretNotThreadSafe**.</span></span> 
  
<span data-ttu-id="2a979-176">As funções de retorno de chamada do C API somente são todas thread-safe:</span><span class="sxs-lookup"><span data-stu-id="2a979-176">The C API-only call-back functions are all thread safe:</span></span>
  
- <span data-ttu-id="2a979-177">**xlCoerce** (exceto embora coerção da célula não calculada referencia falhar)</span><span class="sxs-lookup"><span data-stu-id="2a979-177">**xlCoerce** (except although coercion of uncalculated cell references fails)</span></span> 
    
- <span data-ttu-id="2a979-178">**xlFree**</span><span class="sxs-lookup"><span data-stu-id="2a979-178">**xlFree**</span></span>
    
- <span data-ttu-id="2a979-179">**xlStack**</span><span class="sxs-lookup"><span data-stu-id="2a979-179">**xlStack**</span></span>
    
- <span data-ttu-id="2a979-180">**xlSheetId**</span><span class="sxs-lookup"><span data-stu-id="2a979-180">**xlSheetId**</span></span>
    
- <span data-ttu-id="2a979-181">**xlSheetNm**</span><span class="sxs-lookup"><span data-stu-id="2a979-181">**xlSheetNm**</span></span>
    
- <span data-ttu-id="2a979-182">**xlAbort** (exceto quando usado para limpar uma condição de quebra)</span><span class="sxs-lookup"><span data-stu-id="2a979-182">**xlAbort** (except when used to clear a break condition)</span></span> 
    
- <span data-ttu-id="2a979-183">**xlGetInst**</span><span class="sxs-lookup"><span data-stu-id="2a979-183">**xlGetInst**</span></span>
    
- <span data-ttu-id="2a979-184">**xlGetHwnd**</span><span class="sxs-lookup"><span data-stu-id="2a979-184">**xlGetHwnd**</span></span>
    
- <span data-ttu-id="2a979-185">**xlGetBinaryName**</span><span class="sxs-lookup"><span data-stu-id="2a979-185">**xlGetBinaryName**</span></span>
    
- <span data-ttu-id="2a979-186">**xlDefineBinaryName**</span><span class="sxs-lookup"><span data-stu-id="2a979-186">**xlDefineBinaryName**</span></span>
    
<span data-ttu-id="2a979-187">A única exceção é a função **xlSet** , que é, em qualquer caso, um equivalente de comando e, portanto não podem ser chamados a partir de qualquer função de planilha.</span><span class="sxs-lookup"><span data-stu-id="2a979-187">The one exception is the **xlSet** function, which is, in any case, a command-equivalent and so cannot be called from any worksheet function.</span></span> 
  
<span data-ttu-id="2a979-188">Uma função de planilha XLL pode ser registrada com o Excel como thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-188">An XLL worksheet function can be registered with Excel as thread safe.</span></span> <span data-ttu-id="2a979-189">Isso informa ao Excel que a função pode ser chamada com segurança e simultaneamente em vários threads, embora você deve garantir isso é realmente o caso.</span><span class="sxs-lookup"><span data-stu-id="2a979-189">This tells Excel that the function can be called safely and simultaneously on multiple threads, although you must make sure this is really the case.</span></span> <span data-ttu-id="2a979-190">Você possivelmente pode desestabilizar Excel se uma função registrada como thread-safe, em seguida, se comporta de forma não segura.</span><span class="sxs-lookup"><span data-stu-id="2a979-190">You can possibly destabilize Excel if a function registered as thread safe then behaves unsafely.</span></span>
  
## <a name="registering-xll-functions-as-thread-safe"></a><span data-ttu-id="2a979-191">Registrando as funções XLL como thread-safe</span><span class="sxs-lookup"><span data-stu-id="2a979-191">Registering XLL functions as thread safe</span></span>
<span data-ttu-id="2a979-192"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="2a979-192"></span></span>

<span data-ttu-id="2a979-193">As regras que um desenvolvedor deve cumprir ao escrever funções thread-safe são:</span><span class="sxs-lookup"><span data-stu-id="2a979-193">The rules that a developer must obey when writing thread-safe functions are as follows:</span></span>
  
- <span data-ttu-id="2a979-194">Não chame recursos de outras DLLs que podem não ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-194">Do not call resources in other DLLs that may not be thread safe.</span></span>
    
- <span data-ttu-id="2a979-195">Não faça qualquer não seguros thread chamadas através do C API ou COM.</span><span class="sxs-lookup"><span data-stu-id="2a979-195">Do not make any thread-unsafe calls via the C API or COM.</span></span>
    
- <span data-ttu-id="2a979-196">Protege os recursos que poderiam ser usados simultaneamente por mais de um segmento usando as seções críticas.</span><span class="sxs-lookup"><span data-stu-id="2a979-196">Protect resources that could be used simultaneously by more than one thread using critical sections.</span></span>
    
- <span data-ttu-id="2a979-197">Use memória local de segmento para armazenamento específicos de segmento e substituir as variáveis estáticas dentro das funções com variáveis de segmento locais.</span><span class="sxs-lookup"><span data-stu-id="2a979-197">Use thread-local memory for thread-specific storage, and replace static variables within functions with thread-local variables.</span></span>
    
<span data-ttu-id="2a979-198">Excel impõe uma restrição adicional: funções thread-safe não pode ser registradas como equivalentes de folha de macro e, portanto, não é possível chamar as funções de informações ou obter os valores de células não recalculadas.</span><span class="sxs-lookup"><span data-stu-id="2a979-198">Excel imposes an additional restriction: thread-safe functions cannot be registered as macro-sheet equivalents, and therefore cannot call XLM information functions or get the values of un-recalculated cells.</span></span>
  
## <a name="memory-contention"></a><span data-ttu-id="2a979-199">Contenção de memória</span><span class="sxs-lookup"><span data-stu-id="2a979-199">Memory contention</span></span>
<span data-ttu-id="2a979-200"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="2a979-200"></span></span>

<span data-ttu-id="2a979-201">Sistemas multithread devem atender duas questões fundamentais:</span><span class="sxs-lookup"><span data-stu-id="2a979-201">Multithreaded systems must address two fundamental issues:</span></span>
  
- <span data-ttu-id="2a979-202">Como proteger a memória que deve ser lido ou gravada por mais de um segmento.</span><span class="sxs-lookup"><span data-stu-id="2a979-202">How to protect memory that must be read from, or written to, by more than one thread.</span></span>
    
- <span data-ttu-id="2a979-203">Como criar e memória de acesso que está associado e então particulares para, a execução do thread.</span><span class="sxs-lookup"><span data-stu-id="2a979-203">How to create and access memory that is associated with, and so private to, the executing thread.</span></span>
    
<span data-ttu-id="2a979-204">O sistema operacional Windows e Windows Software Development Kit (SDK) fornecem ferramentas para ambos dessas: seções críticas e a API de armazenamento de thread local (TLS) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2a979-204">The Windows operating system and Windows Software Development Kit (SDK) provide tools for both of these: critical sections and the thread-local storage (TLS) API respectively.</span></span> <span data-ttu-id="2a979-205">Para saber mais, consulte [Memory Management in Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="2a979-205">For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
<span data-ttu-id="2a979-206">O primeiro problema pode surgir, por exemplo, quando duas funções de planilha (ou duas instâncias simultaneamente a execução da mesma função) precisam acessar ou modificar uma variável global em um projeto DLL.</span><span class="sxs-lookup"><span data-stu-id="2a979-206">The first issue can arise, for example, when two worksheet functions (or two simultaneously running instances of the same function) need to access or modify a global variable in a DLL project.</span></span> <span data-ttu-id="2a979-207">Lembre-se de que tal variável global pode estar ocultos em uma instância de um objeto de classe do acessível globalmente.</span><span class="sxs-lookup"><span data-stu-id="2a979-207">Remember that such a global variable might be hidden in a globally accessible instance of a class object.</span></span>
  
<span data-ttu-id="2a979-208">O segundo problema pode surgir, por exemplo, quando uma função de planilha declara uma variável estática ou um objeto no código do corpo da função.</span><span class="sxs-lookup"><span data-stu-id="2a979-208">The second issue can arise, for example, when a worksheet function declares a static variable or object within the function body code.</span></span> <span data-ttu-id="2a979-209">O compilador C/C++ cria apenas uma única cópia que usam todos os threads.</span><span class="sxs-lookup"><span data-stu-id="2a979-209">The C/C++ compiler only creates a single copy that all threads use.</span></span> <span data-ttu-id="2a979-210">Isso significa que uma instância da função poderia alterar o valor, enquanto a outra em um segmento diferente pode supondo que o valor é o que ele anteriormente definido.</span><span class="sxs-lookup"><span data-stu-id="2a979-210">This means one instance of the function could change the value, while another on a different thread might be assuming the value is what it previously set.</span></span>
  
## <a name="example-applications-of-mtr"></a><span data-ttu-id="2a979-211">Aplicativos de exemplo de MTR</span><span class="sxs-lookup"><span data-stu-id="2a979-211">Example applications of MTR</span></span>
<span data-ttu-id="2a979-212"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="2a979-212"></span></span>

<span data-ttu-id="2a979-213">Qualquer XLL que exporta as funções de planilha pode tirar proveito de recálculo multithreaded (MTR) no Excel, desde que essas funções não é necessário realizar ações não seguros thread.</span><span class="sxs-lookup"><span data-stu-id="2a979-213">Any XLL that exports worksheet functions can take advantage of multithreaded recalculation (MTR) in Excel provided that those functions do not need to perform thread-unsafe actions.</span></span> <span data-ttu-id="2a979-214">Isso permite que o Excel recalcule pastas de trabalho que dependem deles mais rápido possível e, portanto, é desejável que for o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2a979-214">This enables Excel to recalculate workbooks that depend on them as quickly as possible and is therefore desirable whatever the application.</span></span>
  
<span data-ttu-id="2a979-215">Especificamente, MTR tem um enorme impacto sobre o tempo de recálculo das pastas de trabalho que chamam funções definidas pelo usuário (UDFs) que sozinhos chamar processos externos para obter o resultado desejado.</span><span class="sxs-lookup"><span data-stu-id="2a979-215">Specifically, MTR has an enormous impact on the recalculation time of workbooks that call user-defined functions (UDFs) that themselves call external processes to obtain the desired result.</span></span> <span data-ttu-id="2a979-216">Em particular, considere um UDF que chame um servidor remoto que pode processar muitas solicitações simultaneamente e uma pasta de trabalho que contém o número de chamadas para essa função.</span><span class="sxs-lookup"><span data-stu-id="2a979-216">In particular, consider a UDF that calls a remote server that can process many requests simultaneously and a workbook containing many calls to that function.</span></span> <span data-ttu-id="2a979-217">Se o recálculo da pasta de trabalho for single-threaded, cada chamada UDF e, portanto com o servidor remoto, deve concluir antes de seguir uma pode ser feita.</span><span class="sxs-lookup"><span data-stu-id="2a979-217">If recalculation of the workbook is single-threaded, each call to the UDF, and so to the remote server, must complete before the next one can be made.</span></span> <span data-ttu-id="2a979-218">Isso desperdiça a capacidade do servidor para processar muitas chamadas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="2a979-218">This wastes the server's ability to process many calls at once.</span></span> <span data-ttu-id="2a979-219">Se não for multithreaded recálculo da pasta de trabalho, o Excel pode fazer várias chamadas ao mesmo tempo ou em sucessão rápida.</span><span class="sxs-lookup"><span data-stu-id="2a979-219">If recalculation of the workbook is multithreaded, Excel can make multiple calls at the same time or in rapid succession.</span></span>
  
<span data-ttu-id="2a979-220">Se o Excel está configurado para usar o mesmo número de threads como o servidor — chamá-lo N — e a topologia da árvore de dependência da pasta de trabalho permite que ele, o tempo total de recálculo poderia ser reduzido para algo se aproximando 1/N do tempo cálculo com um único segmento.</span><span class="sxs-lookup"><span data-stu-id="2a979-220">If Excel is configured to use the same number of threads as the server—call it N—and the topology of the dependency tree of the workbook permits it, the total recalculation time could be reduced to something approaching 1/N of the single-threaded calculation time.</span></span> <span data-ttu-id="2a979-221">Isso pode ser true, até mesmo, onde o computador cliente (em que a pasta de trabalho está sendo executado) tiver apenas um processador, especialmente onde o tempo necessário para fazer a chamada para o servidor é pequeno em relação ao tempo que leva o servidor ao processo a chamada.</span><span class="sxs-lookup"><span data-stu-id="2a979-221">This may be true even where the client computer (on which the workbook is running) only has one processor, especially where the time taken to make the call to the server is small relative to the time it takes the server to process the call.</span></span> 
  
<span data-ttu-id="2a979-222">Não há sobrecarga de sistema operacional para cada segmento adicional.</span><span class="sxs-lookup"><span data-stu-id="2a979-222">There is operating system overhead for each additional thread.</span></span> <span data-ttu-id="2a979-223">Portanto, alguns experimentação pode ser necessária para uma determinada pasta de trabalho e um determinado servidor e o computador cliente para localizar o número ideal de threads que Excel deve ser informado de usar.</span><span class="sxs-lookup"><span data-stu-id="2a979-223">Therefore some experimentation might be required for a given workbook and a given server and client computer to find the optimum number of threads Excel should be told to use.</span></span> 
  
<span data-ttu-id="2a979-224">Por exemplo, considere um processador único computador que está executando o Excel e uma pasta de trabalho que contém as 1.000 células.</span><span class="sxs-lookup"><span data-stu-id="2a979-224">For example, consider a single-processor computer that is running Excel and a workbook that contains 1,000 cells.</span></span> <span data-ttu-id="2a979-225">Ele chama um UDF, que por sua vez, chama um ou mais servidores remotos.</span><span class="sxs-lookup"><span data-stu-id="2a979-225">It calls a UDF, which in turn calls one or more remote servers.</span></span> <span data-ttu-id="2a979-226">Suponha que a 1.000 células não dependem uns dos outros, para que o Excel não tenha esperar por uma chamada concluir antes de chamar o próximo.</span><span class="sxs-lookup"><span data-stu-id="2a979-226">Assume that the 1,000 cells do not depend upon each other, so that Excel does not have to wait for one call to complete before calling the next.</span></span> <span data-ttu-id="2a979-227">(Alguns relaxamento desta restrição é possível sem afetar neste exemplo.) Se os servidores podem processar solicitações de 100 simultaneamente e Excel está configurado para usar a 100 segmentos, o tempo de execução pode ser reduzido ao mínimo 1/100th que onde apenas um segmento é usado.</span><span class="sxs-lookup"><span data-stu-id="2a979-227">(Some relaxation of this constraint is possible without affecting this example.) If the servers can process 100 requests simultaneously, and Excel is configured to use 100 threads, the execution time can be reduced to as little as 1/100th of that where only one thread is used.</span></span> <span data-ttu-id="2a979-228">A sobrecarga associada Excel alocar chamadas para cada segmento e o sistema operacional Gerenciando 100 segmentos significa que, na prática, a redução não será bastante nesse excelente.</span><span class="sxs-lookup"><span data-stu-id="2a979-228">The overhead that is associated with Excel allocating calls to each thread and the operating system managing 100 threads means that, in practice, the reduction will not be quite this great.</span></span> <span data-ttu-id="2a979-229">Há também uma pressuposição implícita aqui que o servidor é bem dimensionado e solicitando que ele processar 100 tarefas simultaneamente não afetará os tempos de conclusão de tarefa individual significativamente.</span><span class="sxs-lookup"><span data-stu-id="2a979-229">There is also an implicit assumption here that the server scales well, and asking it to process 100 tasks concurrently will not affect individual task completion times significantly.</span></span>
  
<span data-ttu-id="2a979-230">Um aplicativo prático nas quais essa técnica pode ter um importante benefício é de métodos Monte Carlo, assim como outras tarefas numericamente intensivas que podem ser divididas em subtarefas menores que podem ser delegadas aos servidores.</span><span class="sxs-lookup"><span data-stu-id="2a979-230">One practical application in which this technique can have an important benefit is that of Monte-Carlo methods, as well as other numerically intensive tasks that can be split into smaller sub-tasks that can be farmed out to servers.</span></span>
  
## <a name="excel-services-considerations"></a><span data-ttu-id="2a979-231">Considerações de serviços do Excel</span><span class="sxs-lookup"><span data-stu-id="2a979-231">Excel Services considerations</span></span>
<span data-ttu-id="2a979-232"><a name="xl2007xllsdk_threadsafe"> </a></span><span class="sxs-lookup"><span data-stu-id="2a979-232"></span></span>

<span data-ttu-id="2a979-233">Excel Services suporta o carregamento, calculando e renderização de planilhas do Excel em um servidor.</span><span class="sxs-lookup"><span data-stu-id="2a979-233">Excel Services supports the loading, calculating, and rendering of Excel spreadsheets on a server.</span></span> <span data-ttu-id="2a979-234">Os usuários podem então acessar e interagir com as planilhas, usando as ferramentas padrão do navegador.</span><span class="sxs-lookup"><span data-stu-id="2a979-234">Users can then access and interact with the spreadsheets by using standard browser tools.</span></span>
  
<span data-ttu-id="2a979-235">UDFs de serviços do Excel são criados usando código gerenciado do Microsoft .NET Framework e torná-los disponíveis, embora um assembly do .NET.</span><span class="sxs-lookup"><span data-stu-id="2a979-235">Excel Services UDFs are created using Microsoft .NET Framework managed code and made available though a .NET assembly.</span></span> <span data-ttu-id="2a979-236">XLLs não são suportados pelos serviços do Excel.</span><span class="sxs-lookup"><span data-stu-id="2a979-236">XLLs are not supported by Excel Services.</span></span> <span data-ttu-id="2a979-237">Um servidor de código gerenciado recurso UDF pode ligar para um XLL para acessar sua funcionalidade, para que o usuário pode ter a mesma funcionalidade com uma pasta de trabalho do servidor carregado, assim como acontece com uma pasta de trabalho carregados pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="2a979-237">A managed code server UDF resource can call into an XLL to access its functionality, so that the user can have the same functionality with a server-loaded workbook as with a client-loaded workbook.</span></span>
  
<span data-ttu-id="2a979-238">Para disponibilizar as funções de um XLL dessa maneira, eles, portanto, devem ser quebrados em um assembly do .NET que converte argumentos e valores de retorno de tipos de dados nativos para os tipos de dados do .NET Framework gerenciados e que chama as funções XLL.</span><span class="sxs-lookup"><span data-stu-id="2a979-238">To make an XLL's functions available in this way, they must therefore be wrapped in a .NET assembly that converts arguments and return values from the native data types to the .NET Framework managed data types, and that calls the XLL functions.</span></span> <span data-ttu-id="2a979-239">O wrapper .NET seria exportar um servidor UDF para cada função XLL sendo acessado.</span><span class="sxs-lookup"><span data-stu-id="2a979-239">The .NET wrapper would export one server UDF for each XLL function being accessed.</span></span> <span data-ttu-id="2a979-240">Um requisito adicional é que todas as funções XLL chamadas dessa forma devem ser thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-240">An additional requirement is that any XLL functions called in this way must be thread safe.</span></span> <span data-ttu-id="2a979-241">Como as funções XLL não são registradas da maneira que estão com o cliente do Excel, o servidor e o wrapper .NET não têm como impondo que eles são thread-safe.</span><span class="sxs-lookup"><span data-stu-id="2a979-241">Because the XLL functions are not registered in the way that they are with client Excel, the server and the .NET wrapper have no way of enforcing that they are thread safe.</span></span> <span data-ttu-id="2a979-242">É responsabilidade do desenvolvedor XLL garantir isso.</span><span class="sxs-lookup"><span data-stu-id="2a979-242">It is the responsibility of the XLL developer to ensure this.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2a979-243">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a979-243">See also</span></span>

- [<span data-ttu-id="2a979-244">Recálculo do Excel</span><span class="sxs-lookup"><span data-stu-id="2a979-244">Excel Recalculation</span></span>](excel-recalculation.md)  
- [<span data-ttu-id="2a979-245">Gerenciamento de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="2a979-245">Memory Management in Excel</span></span>](memory-management-in-excel.md) 
- [<span data-ttu-id="2a979-246">Acessando código XLL no Excel</span><span class="sxs-lookup"><span data-stu-id="2a979-246">Accessing XLL Code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="2a979-247">Excel Programming Concepts</span><span class="sxs-lookup"><span data-stu-id="2a979-247">Excel Programming Concepts</span></span>](excel-programming-concepts.md)  
- [<span data-ttu-id="2a979-248">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="2a979-248">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)

