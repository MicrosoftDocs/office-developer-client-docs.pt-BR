---
title: Gerenciamento de memória no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- memória XLOPER12 [Excel 2007], gerenciamento de memória no Excel, pilha do Excel, cadeias de caracteres [Excel 2007], gerenciamento de memória, gerenciamento de memória no Excel, memória XLOPER [Excel 2007], memória [Excel 2007], diretrizes de gerenciamento
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419538"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="8a268-104">Gerenciamento de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="8a268-104">Memory Management in Excel</span></span>

 <span data-ttu-id="8a268-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8a268-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8a268-106">O gerenciamento de memória é a preocupação mais importante se você quiser criar XLLs eficientes e estáveis.</span><span class="sxs-lookup"><span data-stu-id="8a268-106">Memory management is the most important concern if you want to create efficient and stable XLLs.</span></span> <span data-ttu-id="8a268-107">A falha no gerenciamento da memória pode levar a uma variedade de problemas no Microsoft Excel, desde pequenos problemas, como alocação de memória ineficiente e vazamentos de memória pequenos, para grandes problemas, como a desestabilização do Excel.</span><span class="sxs-lookup"><span data-stu-id="8a268-107">Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="8a268-108">O gerenciamento inconsistente de memória é a fonte mais comum de problemas relacionados a suplementos sérios.</span><span class="sxs-lookup"><span data-stu-id="8a268-108">Mismanagement of memory is the most common source of serious add-in-related problems.</span></span> <span data-ttu-id="8a268-109">Portanto, você deve criar seu projeto com uma estratégia consistente e bem elaborada sobre o gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-109">Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="8a268-110">O gerenciamento de memória ficou mais complexo no Microsoft Office Excel 2007 com a introdução do recálculo de pasta de trabalho multithread.</span><span class="sxs-lookup"><span data-stu-id="8a268-110">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation.</span></span> <span data-ttu-id="8a268-111">Se você quiser criar e exportar funções de planilha com segurança de thread, você deve gerenciar os conflitos resultantes que podem ocorrer quando vários threads competem o acesso.</span><span class="sxs-lookup"><span data-stu-id="8a268-111">If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="8a268-112">Há considerações de memória para os seguintes três tipos de estrutura de dados:</span><span class="sxs-lookup"><span data-stu-id="8a268-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="8a268-113">**XLOPER**s e **XLOPER12**s</span><span class="sxs-lookup"><span data-stu-id="8a268-113">**XLOPER**s and **XLOPER12**s</span></span>
    
- <span data-ttu-id="8a268-114">Cadeias de caracteres que não estão em um **XLOPER** ou **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="8a268-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="8a268-115">Matrizes de **FP** e **FP12**</span><span class="sxs-lookup"><span data-stu-id="8a268-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="8a268-116">Memória XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="8a268-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="8a268-117">A estrutura de dados **XLOPER**/ **XLOPER12** tem alguns subtipos que contêm ponteiros para blocos de memória, como cadeias de caracteres (**xltypeStr**), matrizes (**xltypeMulti**) e referências externas (**xltypeRef**).</span><span class="sxs-lookup"><span data-stu-id="8a268-117">The **XLOPER**/ **XLOPER12** data structure has a few sub-types that contain pointers to blocks of memory, namely strings (**xltypeStr**), arrays (**xltypeMulti**) and external references (**xltypeRef**).</span></span> <span data-ttu-id="8a268-118">Observe também que as matrizes do **xltypeMulti** podem conter cadeias de caracteres \*\*\*\*/ de**XLOPER12s** que, por sua vez, apontam para outros blocos de memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="8a268-119">Um **XLOPER**/ **XLOPER12** pode ser criado de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="8a268-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span></span> 
  
- <span data-ttu-id="8a268-120">Pelo Excel ao preparar argumentos para serem passados para uma função XLL</span><span class="sxs-lookup"><span data-stu-id="8a268-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="8a268-121">Pelo Excel ao retornar **XLOPER** ou **XLOPER12** em uma chamada da API C</span><span class="sxs-lookup"><span data-stu-id="8a268-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="8a268-122">Pela sua DLL ao criar argumentos a serem passados para uma chamada da API de C</span><span class="sxs-lookup"><span data-stu-id="8a268-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="8a268-123">Por sua DLL ao criar um valor de retorno da função XLL</span><span class="sxs-lookup"><span data-stu-id="8a268-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="8a268-124">Um bloco de memória dentro de um dos tipos de apontador de memória pode ser alocado de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="8a268-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="8a268-125">Pode ser um bloco estático dentro da sua DLL fora de qualquer código de função e, nesse caso, você não precisa alocar ou liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="8a268-126">Pode ser um bloco estático dentro da sua DLL dentro de algum código de função e, nesse caso, você não precisa alocar ou liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="8a268-127">Ela pode ser alocada dinamicamente e liberada por sua DLL de várias maneiras possíveis: **malloc** e **Free**, **New** e **delete**, e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8a268-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="8a268-128">Ele pode ser alocado dinamicamente pelo Excel.</span><span class="sxs-lookup"><span data-stu-id="8a268-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="8a268-129">Dada a quantidade de possíveis origens para a memória **XLOPER**/ **XLOPER12** e o número de situações nas quais o **XLOPER**/ **XLOPER12** pode ter tido essa memória atribuída, não é surpresa que esse assunto possa Parece muito difícil.</span><span class="sxs-lookup"><span data-stu-id="8a268-129">Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult.</span></span> <span data-ttu-id="8a268-130">No enTanto, a complexidade pode ser muito reduzida se você seguir várias regras e diretrizes.</span><span class="sxs-lookup"><span data-stu-id="8a268-130">However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="8a268-131">Regras para trabalhar com XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="8a268-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="8a268-132">Não tente liberar memória ou substituir **XLOPER**/ **XLOPER12**s que são passados como argumentos para a função XLL.</span><span class="sxs-lookup"><span data-stu-id="8a268-132">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function.</span></span> <span data-ttu-id="8a268-133">Você deve tratar esses argumentos como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8a268-133">You should treat such arguments as read-only.</span></span> <span data-ttu-id="8a268-134">Para obter mais informações, consulte "retornando **XLOPER** ou **XLOPER12** modificando argumentos no local" em [problemas conhecidos no desenvolvimento XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="8a268-134">For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="8a268-135">Se o Excel alocou memória para um **XLOPER**/ **XLOPER12** retornado para sua dll em uma chamada para a API de C:</span><span class="sxs-lookup"><span data-stu-id="8a268-135">If Excel has allocated memory for an **XLOPER**/ **XLOPER12** returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="8a268-136">Você deve liberar a memória quando não precisar mais do **XLOPER**/ **XLOPER12** usando uma chamada a [xlFree](xlfree.md).</span><span class="sxs-lookup"><span data-stu-id="8a268-136">You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md).</span></span> <span data-ttu-id="8a268-137">Não use nenhum outro método, como livre ou excluído, para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-137">Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="8a268-138">Se o tipo retornado for **xltypeMulti**, não substitua nenhum **XLOPER**/ **XLOPER12**s dentro da matriz, especialmente se eles contiverem cadeias de caracteres e, especialmente, onde você está tentando substituir por uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a268-138">If the returned type is **xltypeMulti**, do not overwrite any **XLOPER**/ **XLOPER12**s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="8a268-139">Se você quiser retornar o **XLOPER**/ **XLOPER12** ao Excel como o valor de retorno da função DLL, deverá informar ao Excel que há memória que o Excel deve liberar quando tiver terminado.</span><span class="sxs-lookup"><span data-stu-id="8a268-139">If you want to return the **XLOPER**/ **XLOPER12** to Excel as your DLL function's return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="8a268-140">Você só deve chamar **xlFree** em um **XLOPER**/ **XLOPER12** que foi criado como o valor de retorno para uma chamada da API de C.</span><span class="sxs-lookup"><span data-stu-id="8a268-140">You must only call **xlFree** on an **XLOPER**/ **XLOPER12** that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="8a268-141">Se sua dll alocou memória para um **XLOPER**/ **XLOPER12** que você deseja retornar ao Excel como o valor de retorno da função DLL, você deve informar ao Excel que há memória que a DLL deve liberar.</span><span class="sxs-lookup"><span data-stu-id="8a268-141">If your DLL has allocated memory for an **XLOPER**/ **XLOPER12** that you want to return to Excel as your DLL function's return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="8a268-142">Diretrizes para gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="8a268-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="8a268-143">Seja consistente em sua DLL no método que você usa para alocar e liberar memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-143">Be consistent in your DLL in the method that you use to allocate and release memory.</span></span> <span data-ttu-id="8a268-144">Evite misturar métodos.</span><span class="sxs-lookup"><span data-stu-id="8a268-144">Avoid mixing methods.</span></span> <span data-ttu-id="8a268-145">Uma boa abordagem é envolver o método que você está usando em uma classe de memória ou estrutura, dentro da qual você pode alterar o método usado sem alterar seu código em muitos lugares.</span><span class="sxs-lookup"><span data-stu-id="8a268-145">A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="8a268-146">Ao criar matrizes do **xltypeMulti** dentro da sua dll, seja consistente na forma como você aloca memória para cadeias de caracteres: sempre aloque dinamicamente a memória para elas ou sempre use a memória estática.</span><span class="sxs-lookup"><span data-stu-id="8a268-146">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory.</span></span> <span data-ttu-id="8a268-147">Se você fizer isso, quando estiver liberando a memória, saberá que você deve sempre ou nunca liberar as cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a268-147">If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="8a268-148">Faça cópias profundas da memória alocada no Excel quando você estiver copiando um \*\*\*\*/ **XLOPER12**XLOPER criado pelo Excel.</span><span class="sxs-lookup"><span data-stu-id="8a268-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created **XLOPER**/ **XLOPER12**.</span></span>
    
- <span data-ttu-id="8a268-149">Não coloque cadeias de caracteres de \*\*\*\*/ sequência de caracteres alocadas do Excel**XLOPER12**s dentro de matrizes do **xltypeMulti** .</span><span class="sxs-lookup"><span data-stu-id="8a268-149">Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays.</span></span> <span data-ttu-id="8a268-150">Faça cópias profundas das cadeias de caracteres e armazene ponteiros para as cópias na matriz.</span><span class="sxs-lookup"><span data-stu-id="8a268-150">Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="8a268-151">Liberando memória XLOPER/XLOPER12 alocada ao Excel</span><span class="sxs-lookup"><span data-stu-id="8a268-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="8a268-152">Considere o seguinte comando XLL, que usa **xlGetName** para obter uma cadeia de caracteres contendo o caminho e o nome de arquivo da dll e o exibe em uma caixa de diálogo de alerta usando o **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="8a268-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

<span data-ttu-id="8a268-153">Quando a função não precisa mais da memória apontada pelo **xDllName**, ela pode liberá-la usando uma chamada para a [função xlFree](xlfree.md), uma das funções da API C-only da dll.</span><span class="sxs-lookup"><span data-stu-id="8a268-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="8a268-154">A função **xlFree** está totalmente documentada na seção de referência de função (consulte [funções da API C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), mas lembre-se do seguinte:</span><span class="sxs-lookup"><span data-stu-id="8a268-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="8a268-155">você pode passar ponteiros para mais de um **XLOPER**/ **XLOPER12**s em uma única chamada para **xlFree**, limitado apenas pelo número de argumentos de função com suporte na versão em execução do excel (30 no excel 2003, 255 a partir do excel 2007).</span><span class="sxs-lookup"><span data-stu-id="8a268-155">You can pass pointers to more than one **XLOPER**/ **XLOPER12**s in a single call to **xlFree**, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in Excel 2007).</span></span>
    
- <span data-ttu-id="8a268-156">**xlFree** define o ponteiro contido como **nulo** para garantir que uma tentativa de liberar um \*\*\*\*/ **XLOPER12** XLOPER que já tenha sido liberado é segura.</span><span class="sxs-lookup"><span data-stu-id="8a268-156">**xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe.</span></span> <span data-ttu-id="8a268-157">**xlFree** é a única função da API C que modifica seus argumentos.</span><span class="sxs-lookup"><span data-stu-id="8a268-157">**xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="8a268-158">Você pode chamar o **xlFree** com segurança em qualquer**XLOPER12** **XLOPER**/ usado para o valor de retorno de uma chamada para a API de C, independentemente se ele contém um ponteiro para a memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-158">You can safely call **xlFree** on any **XLOPER**/ **XLOPER12** used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="8a268-159">Retornar XLOPER/XLOPER12s a ser liberado pelo Excel</span><span class="sxs-lookup"><span data-stu-id="8a268-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="8a268-160">Suponha que você quisesse modificar o comando de exemplo na seção anterior e alterá-lo para uma função de planilha que retorna o caminho de DLL e o nome do arquivo quando passado um argumento **true** **Boolean** e **#N/a** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="8a268-160">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise.</span></span> <span data-ttu-id="8a268-161">Sem dúvida, não é possível chamar **xlFree** para liberar a memória da cadeia de caracteres antes de devolvê-la ao Excel.</span><span class="sxs-lookup"><span data-stu-id="8a268-161">Clearly you cannot call **xlFree** to release the string memory before returning it to Excel.</span></span> <span data-ttu-id="8a268-162">No enTanto, se não for liberado em algum momento, o suplemento vazará memória toda vez que a função for chamada.</span><span class="sxs-lookup"><span data-stu-id="8a268-162">However, if it is not freed at some point, the add-in will leak memory every time the function is called.</span></span> <span data-ttu-id="8a268-163">Para contornar esse problema, você pode definir um bit no campo **xltype** do **XLOPER**/ **XLOPER12**, definido como **xlbitXLFree** em xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="8a268-163">To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h.</span></span> <span data-ttu-id="8a268-164">Definir isso informa ao Excel que ele deve liberar a memória retornada quando terminar de copiar o valor.</span><span class="sxs-lookup"><span data-stu-id="8a268-164">Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="8a268-165">Exemplo</span><span class="sxs-lookup"><span data-stu-id="8a268-165">Example</span></span>

<span data-ttu-id="8a268-166">O exemplo de código a seguir mostra o comando XLL da seção anterior convertida em uma função de planilha XLL.</span><span class="sxs-lookup"><span data-stu-id="8a268-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

<span data-ttu-id="8a268-167">Funções XLL que usam **XLOPER**/ **XLOPER12**s devem ser declaradas como pegar e retornar ponteiros para **XLOPER**/ **XLOPER12**s.</span><span class="sxs-lookup"><span data-stu-id="8a268-167">XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s.</span></span> <span data-ttu-id="8a268-168">O uso neste exemplo de um **XLOPER12** estático dentro da função não é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8a268-168">The use in this example of a static **XLOPER12** within the function is not thread safe.</span></span> <span data-ttu-id="8a268-169">Você pode registrar incorretamente essa função como thread-safe, mas o risco **xRtnValue** ser substituído por um thread antes que outro thread tivesse concluído.</span><span class="sxs-lookup"><span data-stu-id="8a268-169">You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="8a268-170">Você deve definir **xlbitXLFree** após a chamada para o retorno de chamada do Excel que o aloca.</span><span class="sxs-lookup"><span data-stu-id="8a268-170">You must set **xlbitXLFree** after the call to the Excel callback that allocates it.</span></span> <span data-ttu-id="8a268-171">Se você defini-la antes disso, ela será sobrescrita e não terá o efeito desejado.</span><span class="sxs-lookup"><span data-stu-id="8a268-171">If you set it before this, it is overwritten and does not have the effect that you want.</span></span> <span data-ttu-id="8a268-172">Se você pretende usar o valor como um argumento em uma chamada para outra função da API C antes de devolvê-lo à planilha, você deve definir esse bit após qualquer chamada.</span><span class="sxs-lookup"><span data-stu-id="8a268-172">If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call.</span></span> <span data-ttu-id="8a268-173">Caso contrário, você confundirá funções que não mascaram esse bit antes de verificar o tipo de**XLLOPER12** **XLOPER**/ .</span><span class="sxs-lookup"><span data-stu-id="8a268-173">Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="8a268-174">Retornar XLOPER/XLOPER12s a ser liberado pela DLL</span><span class="sxs-lookup"><span data-stu-id="8a268-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="8a268-175">Um problema semelhante a isso ocorre quando seu XLL alocou memória para um **XLOPER**/ **XLOPER12** e deseja retorná-lo ao Excel.</span><span class="sxs-lookup"><span data-stu-id="8a268-175">A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel.</span></span> <span data-ttu-id="8a268-176">O Excel reconhece outro bit que pode ser definido no campo **xltype** do **XLOPER**/ **XLOPER12**, definido como **xlbitDLLFree** em xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="8a268-176">Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h.</span></span> 
  
<span data-ttu-id="8a268-177">Quando o Excel recebe **um XLOPER**/ **XLOPER12** com esse conjunto de bits, ele tenta chamar uma função que deve ser exportada pelo XLL chamado [xlAutoFree](xlautofree-xlautofree12.md) (para **XLOPER**s) ou **xlAutoFree12** (para **XLOPER12**s).</span><span class="sxs-lookup"><span data-stu-id="8a268-177">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s).</span></span> <span data-ttu-id="8a268-178">Essa função é descrita mais completamente na referência de função (consulte [Gerenciador de suplementos e funções da interface XLL](add-in-manager-and-xll-interface-functions.md)), mas um exemplo de implementação mínima é fornecido aqui.</span><span class="sxs-lookup"><span data-stu-id="8a268-178">This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here.</span></span> <span data-ttu-id="8a268-179">Sua finalidade é liberar a memória **XLOPER**/ **XLOPER12** de forma consistente com a forma como ela foi alocada originalmente.</span><span class="sxs-lookup"><span data-stu-id="8a268-179">Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="8a268-180">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8a268-180">Examples</span></span>

<span data-ttu-id="8a268-181">A função de exemplo a seguir faz o mesmo que a função anterior, exceto pelo fato de que ela inclui o texto "o nome de caminho completo para esta DLL é" antes do nome da DLL.</span><span class="sxs-lookup"><span data-stu-id="8a268-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

<span data-ttu-id="8a268-182">Uma implementação minimamente suficiente de **xlAutoFree12** no XLL que exportou a função anterior seria como a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a268-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="8a268-183">Essa implementação só será suficiente se o XLL retornar apenas cadeias de caracteres **XLOPER12** , e essas cadeias de caracteres serão alocadas apenas usando **malloc**.</span><span class="sxs-lookup"><span data-stu-id="8a268-183">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**.</span></span> <span data-ttu-id="8a268-184">Observe que o teste</span><span class="sxs-lookup"><span data-stu-id="8a268-184">Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="8a268-185">falhará nesse caso porque o **xlbitDLLFree** está definido.</span><span class="sxs-lookup"><span data-stu-id="8a268-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="8a268-186">Em geral, **xlAutoFree** e **xlAutoFree12** devem ser implementados para que eles liberem memória associada a matrizES **xltypeMulti** criadas por XLL e as referências externas do **xltypeRef** .</span><span class="sxs-lookup"><span data-stu-id="8a268-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="8a268-187">Você pode decidir implementar suas funções XLL para que todas elas retornem **XLOPER**s e **XLOPER12**s alocados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8a268-187">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s.</span></span> <span data-ttu-id="8a268-188">Nesse caso, você precisaria definir **xlbitDLLFree** em todos esses **XLOPER**s e **XLOPER12**s independentemente do subtipo.</span><span class="sxs-lookup"><span data-stu-id="8a268-188">In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type.</span></span> <span data-ttu-id="8a268-189">Você também precisaria implementar o **xlAutoFree** e o **xlAutoFree12** para que essa memória seja liberada e também qualquer memória apontada dentro do **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="8a268-189">You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="8a268-190">Essa abordagem é uma maneira de tornar o valor de retorno em thread seguro.</span><span class="sxs-lookup"><span data-stu-id="8a268-190">This approach is one way to make the return value thread safe.</span></span> <span data-ttu-id="8a268-191">Por exemplo, a função Previous pode ser reescrita da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8a268-191">For example, the previous function could be rewritten as follows.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

<span data-ttu-id="8a268-192">Para obter mais informações sobre o **xlAutoFree** e o **XlAutoFree12**, consulte [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span><span class="sxs-lookup"><span data-stu-id="8a268-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="8a268-193">Retornando argumentos de modificação no local</span><span class="sxs-lookup"><span data-stu-id="8a268-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="8a268-194">O Excel permite que uma função XLL retorne um valor modificando um argumento no local.</span><span class="sxs-lookup"><span data-stu-id="8a268-194">Excel allows an XLL function to return a value by modifying an argument in place.</span></span> <span data-ttu-id="8a268-195">Só é possível fazer isso com um argumento passado como um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="8a268-195">You can only do this with an argument passed in as a pointer.</span></span> <span data-ttu-id="8a268-196">Para funcionar dessa forma, a função deve ser registrada de uma maneira que informa ao Excel qual argumento será modificado.</span><span class="sxs-lookup"><span data-stu-id="8a268-196">To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="8a268-197">Esse método de retorno de um valor é suportado para todos os tipos de dados que podem ser passados por ponteiro, mas é especialmente útil para os seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="8a268-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="8a268-198">Sequências de bytes ASCII de tamanho contado e terminada por caractere nulo</span><span class="sxs-lookup"><span data-stu-id="8a268-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="8a268-199">Cadeias de caracteres largos Unicode de tamanho contado e terminada em nulo (começando no Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="8a268-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="8a268-200">Matrizes de ponto flutuante de **FP**</span><span class="sxs-lookup"><span data-stu-id="8a268-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="8a268-201">**FP12** matrizes de ponto flutuante (começando no Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="8a268-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8a268-202">Você não deve tentar retornar **XLOPER**s ou **XLOPER12**s dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="8a268-202">You should not try to return **XLOPER**s or **XLOPER12**s in this manner.</span></span> <span data-ttu-id="8a268-203">Confira mais informações em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="8a268-203">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="8a268-204">A vantagem de usar essa técnica, em vez de apenas usar a instrução return, é que o Excel aloca a memória para os valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="8a268-204">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values.</span></span> <span data-ttu-id="8a268-205">Depois que o Excel concluir a leitura dos dados retornados, ele liberará a memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-205">Once Excel has finished reading the returned data, it releases the memory.</span></span> <span data-ttu-id="8a268-206">Isso leva as tarefas de gerenciamento de memória para longe da função XLL.</span><span class="sxs-lookup"><span data-stu-id="8a268-206">This takes the memory management tasks away from the XLL function.</span></span> <span data-ttu-id="8a268-207">Essa técnica é thread-safe: se chamado simultaneamente pelo Excel em threads diferentes, cada chamada de função em cada thread tem seu próprio buffer.</span><span class="sxs-lookup"><span data-stu-id="8a268-207">This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="8a268-208">É útil para os tipos de dados listados anteriormente, em particular, porque o mecanismo de chamada de retorno para a dll para liberar a memória post-return existente para **XLOPER**/ **XLOPER12**s não existe para cadeias de caracteres simples e **FP** /  Matrizes do **FP12** .</span><span class="sxs-lookup"><span data-stu-id="8a268-208">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12**s does not exist for simple strings and **FP**/ **FP12** arrays.</span></span> <span data-ttu-id="8a268-209">Portanto, ao retornar uma cadeia de caracteres criada por DLL ou uma matriz de ponto flutuante, você tem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="8a268-209">Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="8a268-210">Definir um ponteiro persistente para um buffer alocado dinamicamente, retornar o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="8a268-210">Set a persistent pointer to a dynamically allocated buffer, return the pointer.</span></span> <span data-ttu-id="8a268-211">Na próxima chamada para a função (1) Verifique se o ponteiro não é nulo, (2) libere os recursos alocados na chamada anterior e redefina o ponteiro como nulo, (3) reutilize o ponteiro de um bloco de memória recentemente alocado.</span><span class="sxs-lookup"><span data-stu-id="8a268-211">On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="8a268-212">Crie suas cadeias de caracteres e matrizes em um buffer estático que não precise ser liberado e retorne um ponteiro para isso.</span><span class="sxs-lookup"><span data-stu-id="8a268-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="8a268-213">Modificar um argumento no lugar, gravando a cadeia de caracteres ou matriz diretamente no conjunto de espaços do Excel.</span><span class="sxs-lookup"><span data-stu-id="8a268-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="8a268-214">Caso contrário, você deve criar um **XLOPER**/ **XLOPER12**e usar **xlbitDLLFree** e **xlAutoFree**/ **xlAutoFree12** para liberar os recursos.</span><span class="sxs-lookup"><span data-stu-id="8a268-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span></span> 
  
<span data-ttu-id="8a268-215">A última opção pode ser a mais simples nesses casos em que você está sendo passado um argumento do mesmo tipo que o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="8a268-215">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value.</span></span> <span data-ttu-id="8a268-216">O ponto-chave a ser lembrado é que os tamanhos de buffer são limitados e você deve ter muito cuidado para não satura-los.</span><span class="sxs-lookup"><span data-stu-id="8a268-216">The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them.</span></span> <span data-ttu-id="8a268-217">É possível que esse problema falhe no Excel.</span><span class="sxs-lookup"><span data-stu-id="8a268-217">Getting this wrong could crash Excel.</span></span> <span data-ttu-id="8a268-218">Tamanhos de buffer para cadeias de caracteres e**FP12** de **FP**/ são abordados a seguir.</span><span class="sxs-lookup"><span data-stu-id="8a268-218">Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="8a268-219">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="8a268-219">Strings</span></span>

<span data-ttu-id="8a268-220">Problemas com o gerenciamento da memória da cadeia de caracteres são, supostamente, a causa mais comum de instabilidade em aplicativos e suplementos. É possível que seja compreensível, uma vez que as várias maneiras nas quais as cadeias de caracteres são tratadas: terminadas por caractere nulo ou de tamanho contado (ou ambos); buffers estáticos ou dinâmicos; comprimento fixo ou comprimento quase ilimitado; memória gerenciada do sistema operacional (por exemplo, OLE BSTR) ou cadeias de caracteres não gerenciadas; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8a268-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="8a268-221">Os programadores de C/C++ estão mais familiarizados com cadeias de caracteres terminadas por caractere nulo.</span><span class="sxs-lookup"><span data-stu-id="8a268-221">C/C++ programmers are most familiar with null-terminated strings.</span></span> <span data-ttu-id="8a268-222">A biblioteca C padrão foi projetada para trabalhar com essas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a268-222">The standard C library is designed to work with such strings.</span></span> <span data-ttu-id="8a268-223">Literais de cadeia de caracteres estática no código são compilados em cadeias de caracteres terminadas em nulo.</span><span class="sxs-lookup"><span data-stu-id="8a268-223">Static string literals in code are compiled into null-terminated strings.</span></span> <span data-ttu-id="8a268-224">Como alternativa, o Excel funciona com cadeias de caracteres de tamanho contado que não estão em um término geral nulo.</span><span class="sxs-lookup"><span data-stu-id="8a268-224">Alternatively, Excel works with length-counted strings that are not in general null-terminated.</span></span> <span data-ttu-id="8a268-225">A combinação desses fatos requer uma abordagem clara e consistente em sua DLL/XLL em relação à forma como você lida com cadeias de caracteres e memória de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a268-225">The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="8a268-226">Os problemas mais comuns são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="8a268-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="8a268-227">A passagem de um ponteiro nulo ou inválido para uma função que espera um ponteiro válido e não ou não pode verificar a própria validade do ponteiro.</span><span class="sxs-lookup"><span data-stu-id="8a268-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="8a268-228">A superexecução dos limites de um buffer de cadeia de caracteres por uma função que não ou não pode verificar o tamanho do buffer em relação ao comprimento da cadeia de caracteres que está sendo gravada.</span><span class="sxs-lookup"><span data-stu-id="8a268-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="8a268-229">Tentar liberar a memória do buffer de cadeia de caracteres que é estática, ou já foi liberada, ou não foi alocada de uma maneira consistente com o modo como está sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="8a268-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="8a268-230">Vazamentos de memória que resultam de cadeias de caracteres sendo alocadas e, em seguida, não liberadas, geralmente em uma função chamada freqüentemente.</span><span class="sxs-lookup"><span data-stu-id="8a268-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="8a268-231">Regras para cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="8a268-231">Rules for Strings</span></span>

<span data-ttu-id="8a268-232">Assim como \*\*\*\*/ com o XLOPER**XLOPER**s, há regras e diretrizes que você deve seguir.</span><span class="sxs-lookup"><span data-stu-id="8a268-232">As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow.</span></span> <span data-ttu-id="8a268-233">As diretrizes são as mesmas que foram fornecidas na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="8a268-233">The guidelines are the same as given in the previous section.</span></span> <span data-ttu-id="8a268-234">As regras aqui são uma extensão das regras especificamente para cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a268-234">The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="8a268-235">**Regras**</span><span class="sxs-lookup"><span data-stu-id="8a268-235">**Rules:**</span></span>
  
- <span data-ttu-id="8a268-236">Não tente liberar memória ou substituir as cadeias \*\*\*\*/ de caracteres de tamanho de cadeia de caracteres**XLOPER12**s ou de comprimento simples ou nulos passados como argumentos para a função XLL.</span><span class="sxs-lookup"><span data-stu-id="8a268-236">Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12**s or simple length-counted or null-terminated strings passed as arguments to your XLL function.</span></span> <span data-ttu-id="8a268-237">Você deve tratar esses argumentos como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="8a268-237">You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="8a268-238">Onde o Excel aloca memória para um **XLOPER**/ de cadeia de caracteres**XLOPER12** para o valor de retorno de uma função de retorno de chamada de API de C, use **xlFree** para liberá-lo ou defina **xlbitXLFree** se retornar ao Excel a partir de uma função XLL.</span><span class="sxs-lookup"><span data-stu-id="8a268-238">Where Excel allocates memory for a string **XLOPER**/ **XLOPER12** for the return value of a C API callback function, use **xlFree** to free it, or set **xlbitXLFree** if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="8a268-239">Onde sua dll aloca dinamicamente um buffer de cadeia de caracteres para um **XLOPER**/ **XLOPER12**, liberá-lo de forma consistente com a forma como você o alocou quando tiver terminado, ou definir **xlbitDLLFree** se retornar ao Excel a partir de uma função XLL e liberá-lo em **xlAutoFree** /  **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="8a268-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span></span>
    
- <span data-ttu-id="8a268-240">Se o Excel alocou memória para uma matriz **xltypeMulti** retornada à sua dll em uma chamada para a API de C, não substitua nenhum **XLOPER**/ de cadeia de caracteres**XLOPER12**s dentro da matriz.</span><span class="sxs-lookup"><span data-stu-id="8a268-240">If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12**s within the array.</span></span> <span data-ttu-id="8a268-241">Essas matrizes só devem ser liberadas usando **xlFree**ou, se forem retornadas por uma função XLL, definindo **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="8a268-241">Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="8a268-242">Tipos de cadeia de caracteres suportados</span><span class="sxs-lookup"><span data-stu-id="8a268-242">String Types Supported</span></span>

<span data-ttu-id="8a268-243">**XltypeStr de API C/XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="8a268-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="8a268-244">\* \* Cadeias de caracteres de byte: \* \* XLOPER \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8a268-244">\*\*Byte strings: \*\*XLOPER\*\*\*\*</span></span>|<span data-ttu-id="8a268-245">\* \* Cadeias de caracteres largos: \* \* XLOPER12 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="8a268-245">\*\*Wide character strings: \*\*XLOPER12\*\*\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a268-246">Todas as versões do Excel</span><span class="sxs-lookup"><span data-stu-id="8a268-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="8a268-247">Iniciando no Excel 2007</span><span class="sxs-lookup"><span data-stu-id="8a268-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="8a268-248">Comprimento máximo: 255 bytes estendidos ASCII</span><span class="sxs-lookup"><span data-stu-id="8a268-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="8a268-249">Caracteres Unicode de comprimento máximo 32.767</span><span class="sxs-lookup"><span data-stu-id="8a268-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="8a268-250">Byte primeiro (não assinado) = comprimento</span><span class="sxs-lookup"><span data-stu-id="8a268-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="8a268-251">Primeiro caractere Unicode = comprimento</span><span class="sxs-lookup"><span data-stu-id="8a268-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="8a268-252">Não assuma a terminação nula de cadeias de caracteres **XLOPER** ou **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="8a268-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="8a268-253">**Cadeias de caracteres C/C++**</span><span class="sxs-lookup"><span data-stu-id="8a268-253">**C/C++ strings**</span></span>

|<span data-ttu-id="8a268-254">**Cadeias de caracteres de byte**</span><span class="sxs-lookup"><span data-stu-id="8a268-254">**Byte strings**</span></span>|<span data-ttu-id="8a268-255">**Cadeias de caracteres largos**</span><span class="sxs-lookup"><span data-stu-id="8a268-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="8a268-256">Terminada em nulo (**Char** \*) "C" tamanho máximo: 255 bytes ASCII estendidos</span><span class="sxs-lookup"><span data-stu-id="8a268-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="8a268-257">Terminada em nulo (**wchar_t** \*) "C%" tamanho máximo de 32.767 caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="8a268-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="8a268-258">Comprimento contado (unsigned**Char** \*) "D"</span><span class="sxs-lookup"><span data-stu-id="8a268-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="8a268-259">Comprimento contado (**wchar_t** \*) "D%"</span><span class="sxs-lookup"><span data-stu-id="8a268-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="8a268-260">Cadeias de caracteres em matrizes xltypeMulti XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="8a268-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="8a268-261">Em vários casos, o Excel cria uma matriz **xltypeMulti** para uso em sua dll/XLL.</span><span class="sxs-lookup"><span data-stu-id="8a268-261">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL.</span></span> <span data-ttu-id="8a268-262">Várias das funções de informações XLM retornam essas matrizes.</span><span class="sxs-lookup"><span data-stu-id="8a268-262">Several of the XLM information functions return such arrays.</span></span> <span data-ttu-id="8a268-263">Por exemplo, a função da API C **xlfGetWorkspace**, quando passado o argumento *44* , retorna uma matriz contendo cadeias de caracteres que DESCREVEM todos os procedimentos dll registrados no momento.</span><span class="sxs-lookup"><span data-stu-id="8a268-263">For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures.</span></span> <span data-ttu-id="8a268-264">A função da API C **xlfDialogBox** retorna uma cópia modificada do seu argumento de matriz, contendo cópias profundas das cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a268-264">The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings.</span></span> <span data-ttu-id="8a268-265">Talvez a maneira mais comum de que um XLL encontre uma matriz **xltypeMulti** seja onde ela foi passada como um argumento para uma função XLL ou foi forçada a esse tipo de uma referência de intervalo.</span><span class="sxs-lookup"><span data-stu-id="8a268-265">Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference.</span></span> <span data-ttu-id="8a268-266">Nesses últimos casos, o Excel cria cópias profundas das cadeias de caracteres nas células de origem e aponta para elas dentro da matriz.</span><span class="sxs-lookup"><span data-stu-id="8a268-266">In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="8a268-267">Onde você deseja modificar essas cadeias de caracteres em sua DLL, você deve fazer suas próprias cópias profundas.</span><span class="sxs-lookup"><span data-stu-id="8a268-267">Where you want to modify these strings in your DLL, you should make your own deep copies.</span></span> <span data-ttu-id="8a268-268">Ao criar suas próprias matrizes do **xltypeMulti** , você não deve colocar a cadeia de caracteres \*\*\*\*/ \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="8a268-268">When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them.</span></span> <span data-ttu-id="8a268-269">Esses riscos não são liberados corretamente mais tarde ou não os liberam.</span><span class="sxs-lookup"><span data-stu-id="8a268-269">This risks you not freeing them correctly later, or not freeing them at all.</span></span> <span data-ttu-id="8a268-270">Novamente, você deve fazer cópias profundas das cadeias de caracteres e armazenar ponteiros para as cópias na matriz.</span><span class="sxs-lookup"><span data-stu-id="8a268-270">Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="8a268-271">**Exemplos**</span><span class="sxs-lookup"><span data-stu-id="8a268-271">**Examples**</span></span>
  
<span data-ttu-id="8a268-272">A função de exemplo a seguir cria uma cópia alocada dinamicamente de uma cadeia de caracteres Unicode contada por comprimento.</span><span class="sxs-lookup"><span data-stu-id="8a268-272">The following example function creates a dynamically allocated copy of a length-counted Unicode string.</span></span> <span data-ttu-id="8a268-273">Observe que o chamador deve liberar a memória alocada neste exemplo usando **delete**[], e que a cadeia de caracteres de origem não é considerada nula terminada.</span><span class="sxs-lookup"><span data-stu-id="8a268-273">Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated.</span></span> <span data-ttu-id="8a268-274">A cadeia de caracteres de cópia será truncada se necessário para segurança e não será terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="8a268-274">The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

<span data-ttu-id="8a268-275">Essa função pode ser usada com segurança para copiar um **XLOPER12**, conforme mostrado na seguinte função exportável XLL que retorna uma cópia do seu argumento se for uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="8a268-275">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string.</span></span> <span data-ttu-id="8a268-276">Todos os outros tipos são retornados como uma cadeia de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="8a268-276">All other types are returned as a zero-length string.</span></span> <span data-ttu-id="8a268-277">Observe que os intervalos não são tratados, a função retorna **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="8a268-277">Note that ranges are not handled—the function returns **#VALUE!**.</span></span> <span data-ttu-id="8a268-278">A função deve ser registrada como pegar um argumento de tipo U para que as referências sejam passadas como valores.</span><span class="sxs-lookup"><span data-stu-id="8a268-278">The function must be registered as taking a type U argument so that references are passed in as values.</span></span> <span data-ttu-id="8a268-279">Isso equivale à função de planilha interna **T ()** , exceto pelo fato de \*\*\*\* que astext também converte erros em cadeias de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="8a268-279">This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings.</span></span> <span data-ttu-id="8a268-280">Este exemplo de código pressupõe que o **xlAutoFree12** libera o ponteiro passado, e também seu conteúdo, usando **delete**.</span><span class="sxs-lookup"><span data-stu-id="8a268-280">This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="8a268-281">Retornando argumentos de cadeia de caracteres de modificação no local</span><span class="sxs-lookup"><span data-stu-id="8a268-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="8a268-282">Argumentos registrados como Types **F**, **G**, **F%** e **G%** podem ser modificados no local.</span><span class="sxs-lookup"><span data-stu-id="8a268-282">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place.</span></span> <span data-ttu-id="8a268-283">Quando o Excel está preparando argumentos de cadeia de caracteres para esses tipos, ele cria um buffer de comprimento máximo.</span><span class="sxs-lookup"><span data-stu-id="8a268-283">When Excel is preparing string arguments for these types, it creates a maximum length buffer.</span></span> <span data-ttu-id="8a268-284">Em seguida, ele copia a cadeia de caracteres de argumento para isso, mesmo que essa cadeia de caracteres seja muito mais curta.</span><span class="sxs-lookup"><span data-stu-id="8a268-284">Then it copies the argument string into that, even if this string is very much shorter.</span></span> <span data-ttu-id="8a268-285">Isso permite que a função XLL escreva o valor de retorno diretamente na mesma memória.</span><span class="sxs-lookup"><span data-stu-id="8a268-285">This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="8a268-286">Os tamanhos de buffer definidos para esses tipos são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="8a268-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="8a268-287">**Cadeias de caracteres de byte:** 256 bytes incluindo o contador de comprimento (tipo G) ou de finalização nula (tipo F).</span><span class="sxs-lookup"><span data-stu-id="8a268-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="8a268-288">Cadeias de caracteres **Unicode:** 32.768 caracteres largos (65.536 bytes) incluindo o contador comprimento (tipo G%) ou de finalização nula (tipo F%).</span><span class="sxs-lookup"><span data-stu-id="8a268-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="8a268-289">Não é possível chamar essa função diretamente do Visual Basic for Applications (VBA) porque você não pode garantir que um buffer suficientemente grande tenha sido alocado.</span><span class="sxs-lookup"><span data-stu-id="8a268-289">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated.</span></span> <span data-ttu-id="8a268-290">Você só pode chamar essa função de outra DLL com segurança se tiver passado explicitamente um buffer suficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="8a268-290">You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="8a268-291">Veja a seguir um exemplo de uma função XLL que reverte uma cadeia de caracteres largo terminada por nulo usando a função de biblioteca padrão **wcsrev**.</span><span class="sxs-lookup"><span data-stu-id="8a268-291">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**.</span></span> <span data-ttu-id="8a268-292">O argumento nesse caso seria registrado como o tipo **F%**.</span><span class="sxs-lookup"><span data-stu-id="8a268-292">The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="8a268-293">Armazenamento persistente (nomes binários)</span><span class="sxs-lookup"><span data-stu-id="8a268-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="8a268-294">Os nomes binários são definidos e associados aos blocos de binários, ou seja, não estruturados, que são armazenados juntos com a pasta de trabalho.</span><span class="sxs-lookup"><span data-stu-id="8a268-294">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook.</span></span> <span data-ttu-id="8a268-295">Eles são criados usando a função [xlDefineBinaryName](xldefinebinaryname.md)e os dados são recuperados usando a função [xlGetBinaryName](xlgetbinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="8a268-295">They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md).</span></span> <span data-ttu-id="8a268-296">Ambas as funções são descritas em mais detalhes na referência de função (consulte [funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)) e ambos usam o **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="8a268-296">Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="8a268-297">Para obter informações sobre problemas conhecidos que limitam os aplicativos práticos de nomes binários, consulte [problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="8a268-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="8a268-298">Pilha do Excel</span><span class="sxs-lookup"><span data-stu-id="8a268-298">Excel Stack</span></span>

<span data-ttu-id="8a268-299">O Excel compartilha o espaço em pilha com todas as DLLs carregadas.</span><span class="sxs-lookup"><span data-stu-id="8a268-299">Excel shares its stack space with all the DLLs it has loaded.</span></span> <span data-ttu-id="8a268-300">O espaço de pilha geralmente é mais do que adequado para uso comum, e você não precisa se preocupar com ele desde que siga algumas diretrizes:</span><span class="sxs-lookup"><span data-stu-id="8a268-300">Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="8a268-301">Não transmita estruturas muito grandes como argumentos para funções por valor na pilha.</span><span class="sxs-lookup"><span data-stu-id="8a268-301">Do not pass very large structures as arguments to functions by value on the stack.</span></span> <span data-ttu-id="8a268-302">Passe em vez de ponteiros ou referências.</span><span class="sxs-lookup"><span data-stu-id="8a268-302">Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="8a268-303">Não retorna estruturas grandes na pilha.</span><span class="sxs-lookup"><span data-stu-id="8a268-303">Do not return large structures on the stack.</span></span> <span data-ttu-id="8a268-304">Retornar ponteiros para memória estática ou dinamicamente alocada ou usar argumentos passados por referência.</span><span class="sxs-lookup"><span data-stu-id="8a268-304">Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="8a268-305">Não declare estruturas de variáveis automáticas muito grandes no código de função.</span><span class="sxs-lookup"><span data-stu-id="8a268-305">Do not declare very large automatic variable structures in the function code.</span></span> <span data-ttu-id="8a268-306">Se você precisar deles, declare-os como estáticos.</span><span class="sxs-lookup"><span data-stu-id="8a268-306">If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="8a268-307">Não chame funções recursivamente, a menos que você tenha certeza de que a profundidade da recursão sempre será superficial.</span><span class="sxs-lookup"><span data-stu-id="8a268-307">Do not call functions recursively unless you are sure the depth of recursion will always be shallow.</span></span> <span data-ttu-id="8a268-308">Em vez disso, tente usar um loop.</span><span class="sxs-lookup"><span data-stu-id="8a268-308">Try using a loop instead.</span></span>
    
<span data-ttu-id="8a268-309">Quando uma DLL chama de volta para o Excel usando a API C, o Excel verifica primeiro se há espaço suficiente na pilha para a chamada de uso de pior caso que pudesse ser feita.</span><span class="sxs-lookup"><span data-stu-id="8a268-309">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made.</span></span> <span data-ttu-id="8a268-310">Se ele achar que pode haver espaço insuficiente, a chamada será malsucedida, mesmo que possa ter espaço suficiente para essa chamada específica.</span><span class="sxs-lookup"><span data-stu-id="8a268-310">If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call.</span></span> <span data-ttu-id="8a268-311">Nesse caso, os retornos de chamada retornam o código **xlretFailed**.</span><span class="sxs-lookup"><span data-stu-id="8a268-311">In this case, the callbacks return the code **xlretFailed**.</span></span> <span data-ttu-id="8a268-312">Para uso comum da API C e da pilha, isso é uma improvável causa da falha de uma chamada da API de C.</span><span class="sxs-lookup"><span data-stu-id="8a268-312">For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="8a268-313">Se estiver preocupado, ou apenas curioso, ou se quiser eliminar falta de espaço de pilha como motivo para uma falha não explicada, você pode descobrir quanto espaço de pilha há com uma chamada para a função [xlStack](xlstack.md) .</span><span class="sxs-lookup"><span data-stu-id="8a268-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8a268-314">Confira também</span><span class="sxs-lookup"><span data-stu-id="8a268-314">See also</span></span>



[<span data-ttu-id="8a268-315">Recálculo com vários threads no Excel</span><span class="sxs-lookup"><span data-stu-id="8a268-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="8a268-316">Multithreading e conTenção de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="8a268-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="8a268-317">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="8a268-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

