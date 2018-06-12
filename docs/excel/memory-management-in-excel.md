---
title: Gerenciamento de memória no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- memória XLOPER12 [excel 2007], gerenciar memória no Excel, do Excel pilha, cadeias de caracteres [Excel 2007], gerenciamento de memória, gerenciamento de memória no Excel, memória XLOPER [Excel 2007], memória [Excel 2007], diretrizes de gerenciamento
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 97c76d762fdc5e575c571804816e5581a7bec8bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765429"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="9383a-104">Gerenciamento de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="9383a-104">Memory Management in Excel</span></span>

 <span data-ttu-id="9383a-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9383a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="9383a-106">Gerenciamento de memória é a preocupação mais importante se você quiser criar XLLs eficientes e estáveis.</span><span class="sxs-lookup"><span data-stu-id="9383a-106">Memory management is the most important concern if you want to create efficient and stable XLLs.</span></span> <span data-ttu-id="9383a-107">Falha ao gerenciar memória também pode levar a um intervalo de problemas no Microsoft Excel — de pequenos problemas, como a alocação de memória ineficientes e inicialização e vazamento de memória pequeno, para os principais problemas, como o destabilization do Excel.</span><span class="sxs-lookup"><span data-stu-id="9383a-107">Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="9383a-108">Mal gerenciamento de memória é a origem mais comuns de problemas sérios adicionar em relacionados.</span><span class="sxs-lookup"><span data-stu-id="9383a-108">Mismanagement of memory is the most common source of serious add-in-related problems.</span></span> <span data-ttu-id="9383a-109">Portanto, você deve construir seu projeto com uma estratégia consistente e bem-planejado por meio de gerenciamento de memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-109">Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="9383a-110">Gerenciamento de memória se tornou mais complexo no Microsoft Office Excel 2007 com a introdução de recálculo de pasta de trabalho multithread.</span><span class="sxs-lookup"><span data-stu-id="9383a-110">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation.</span></span> <span data-ttu-id="9383a-111">Se você deseja criar e exportar as funções de planilha de thread-safe, você deve gerenciar os conflitos resultantes que podem ocorrer quando vários threads competem por acesso.</span><span class="sxs-lookup"><span data-stu-id="9383a-111">If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="9383a-112">Há considerações de memória para os seguintes tipos de estrutura de dados de três:</span><span class="sxs-lookup"><span data-stu-id="9383a-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="9383a-113">S **XLOPER**e **XLOPER12**s</span><span class="sxs-lookup"><span data-stu-id="9383a-113">**XLOPER**s and **XLOPER12**s</span></span>
    
- <span data-ttu-id="9383a-114">Cadeias de caracteres que não estão em um **XLOPER** ou **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="9383a-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="9383a-115">Matrizes **FP** e **FP12**</span><span class="sxs-lookup"><span data-stu-id="9383a-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="9383a-116">Memória XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="9383a-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="9383a-117">**XLOPER**/ **XLOPER12** estrutura de dados tem algumas subtipos que contêm ponteiros para blocos de memória, notadamente cadeias de caracteres (**xltypeStr**), matrizes (**xltypeMulti**) e as referências externas (**xltypeRef**).</span><span class="sxs-lookup"><span data-stu-id="9383a-117">The **XLOPER**/ **XLOPER12** data structure has a few sub-types that contain pointers to blocks of memory, namely strings (**xltypeStr**), arrays (**xltypeMulti**) and external references (**xltypeRef**).</span></span> <span data-ttu-id="9383a-118">Observe também que matrizes **xltypeMulti** podem conter a cadeia de caracteres **XLOPER**/ **XLOPER12s** que por sua vez apontam para outros blocos de memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="9383a-119">**XLOPER**/ **XLOPER12** podem ser criados de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="9383a-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span></span> 
  
- <span data-ttu-id="9383a-120">Pelo Excel ao preparar os argumentos a serem passados para uma função XLL</span><span class="sxs-lookup"><span data-stu-id="9383a-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="9383a-121">Pelo Excel ao retornar um **XLOPER** ou **XLOPER12** em uma API C chamada</span><span class="sxs-lookup"><span data-stu-id="9383a-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="9383a-122">Por sua DLL ao criar argumentos a serem passados para uma API C chamada</span><span class="sxs-lookup"><span data-stu-id="9383a-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="9383a-123">Por sua DLL ao criar uma função XLL do valor de retorno</span><span class="sxs-lookup"><span data-stu-id="9383a-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="9383a-124">Um bloco de memória em um dos tipos de memória apontando pode ser alocado de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="9383a-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="9383a-125">Pode ser um bloco estático dentro da sua DLL fora qualquer código de função, caso em que você não precisará alocar ou liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="9383a-126">Pode ser um bloco estático dentro da sua DLL dentro de alguns códigos de função, caso em que você não precisará alocar ou liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="9383a-127">Ele pode ser dinamicamente alocado e liberado pela sua DLL de várias maneiras possíveis: **malloc** e **livres**, **novo** e **Excluir**e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9383a-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="9383a-128">Ele pode ser alocado dinamicamente pelo Excel.</span><span class="sxs-lookup"><span data-stu-id="9383a-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="9383a-129">Dado o número de origens possíveis para **XLOPER**/ **XLOPER12** memória e o número de situações nas quais o **XLOPER**/ **XLOPER12** poderia gerar que atribuído a memória, não é surpreendente que esse assunto pode parece muito difícil.</span><span class="sxs-lookup"><span data-stu-id="9383a-129">Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult.</span></span> <span data-ttu-id="9383a-130">No entanto, a complexidade pode ser reduzida significativamente se você seguir várias regras e diretrizes.</span><span class="sxs-lookup"><span data-stu-id="9383a-130">However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="9383a-131">Regras para trabalhar com XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="9383a-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="9383a-132">Não tente liberar memória ou para substituí **XLOPERs**/ **XLOPER12**s são passados como argumentos para sua função XLL.</span><span class="sxs-lookup"><span data-stu-id="9383a-132">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function.</span></span> <span data-ttu-id="9383a-133">Você deve tratar tais argumentos como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9383a-133">You should treat such arguments as read-only.</span></span> <span data-ttu-id="9383a-134">Para obter mais informações, consulte "Retornando **XLOPER** ou **XLOPER12** pelos argumentos Modifying in-loco" em [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="9383a-134">For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="9383a-135">Se Excel tem memória alocada para **XLOPER**/ **XLOPER12** retornado para sua DLL em uma chamada para a API C:</span><span class="sxs-lookup"><span data-stu-id="9383a-135">If Excel has allocated memory for an **XLOPER**/ **XLOPER12** returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="9383a-136">Você deve liberar a memória quando não precisar mais **XLOPER**/ **XLOPER12** usando uma chamada para [xlFree](xlfree.md).</span><span class="sxs-lookup"><span data-stu-id="9383a-136">You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md).</span></span> <span data-ttu-id="9383a-137">Não usar qualquer outro método, como gratuito ou excluir para liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-137">Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="9383a-138">Se o tipo retornado é **xltypeMulti**, não substituir qualquer **XLOPER**/ **XLOPER12**s dentro do conjunto, especialmente se eles contêm cadeias de caracteres, e especialmente não onde você está tentando substituir por uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9383a-138">If the returned type is **xltypeMulti**, do not overwrite any **XLOPER**/ **XLOPER12**s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="9383a-139">Se você deseja retornar **XLOPER**/ **XLOPER12** para o Excel como valor de retorno da função da DLL, você deve informar ao Excel que não há memória que o Excel deve liberar quando terminado.</span><span class="sxs-lookup"><span data-stu-id="9383a-139">If you want to return the **XLOPER**/ **XLOPER12** to Excel as your DLL function's return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="9383a-140">Você só deve chamar **xlFree** em **XLOPER**/ **XLOPER12** que foi criado como o valor de retorno para uma chamada de API C.</span><span class="sxs-lookup"><span data-stu-id="9383a-140">You must only call **xlFree** on an **XLOPER**/ **XLOPER12** that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="9383a-141">Se sua DLL tem memória alocada para **XLOPER**/ **XLOPER12** que você deseja retornar ao Excel como valor de retorno da função da DLL, você deve informar ao Excel que não há memória a DLL deve liberar.</span><span class="sxs-lookup"><span data-stu-id="9383a-141">If your DLL has allocated memory for an **XLOPER**/ **XLOPER12** that you want to return to Excel as your DLL function's return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="9383a-142">Diretrizes para o gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="9383a-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="9383a-143">Seja consistente em seu DLL no método que você usa para alocar e liberar memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-143">Be consistent in your DLL in the method that you use to allocate and release memory.</span></span> <span data-ttu-id="9383a-144">Evite a combinação de métodos.</span><span class="sxs-lookup"><span data-stu-id="9383a-144">Avoid mixing methods.</span></span> <span data-ttu-id="9383a-145">Uma boa abordagem é quebrar o método que você está usando para cima em uma classe de memória ou a estrutura, dentro do qual você pode alterar o método usado sem alterar o seu código em muitos locais.</span><span class="sxs-lookup"><span data-stu-id="9383a-145">A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="9383a-146">Quando você criar matrizes **xltypeMulti** dentro da sua DLL, seja consistente da maneira que você alocar memória para as cadeias de caracteres: sempre dinamicamente alocar a memória para eles ou sempre use static memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-146">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory.</span></span> <span data-ttu-id="9383a-147">Se você fizer isso, quando você estiver liberando a memória, você saberá que você deve sempre ou nunca liberar as cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9383a-147">If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="9383a-148">Fazer cópias de profundidade de memória alocada para Excel quando você está copiando criados pelo Excel **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="9383a-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created **XLOPER**/ **XLOPER12**.</span></span>
    
- <span data-ttu-id="9383a-149">Não coloque alocadas Excel cadeia de caracteres **XLOPER**/ **XLOPER12**s dentro **xltypeMulti** matrizes.</span><span class="sxs-lookup"><span data-stu-id="9383a-149">Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays.</span></span> <span data-ttu-id="9383a-150">Faça cópias profundas das cadeias de caracteres e armazene ponteiros para as cópias na matriz.</span><span class="sxs-lookup"><span data-stu-id="9383a-150">Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="9383a-151">Liberar memória XLOPER/XLOPER12 alocada para Excel</span><span class="sxs-lookup"><span data-stu-id="9383a-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="9383a-152">Considere o seguinte comando XLL, que usa **xlGetName** para obter uma cadeia de caracteres contendo o nome de arquivo e o caminho da DLL e o exibe em uma caixa de diálogo alerta usando **xlcAlert**.</span><span class="sxs-lookup"><span data-stu-id="9383a-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
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

<span data-ttu-id="9383a-153">Quando a função não precisa mais a memória apontada pela **xDllName**, ele pode liberá-la usando uma chamada para a [função xlFree](xlfree.md), uma das funções somente DLL C API.</span><span class="sxs-lookup"><span data-stu-id="9383a-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="9383a-154">A função **xlFree** é totalmente documentada na seção de referência de função (consulte [C API funções que pode ser chamado apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), mas esteja ciente das seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="9383a-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="9383a-155">Você pode passar ponteiros para mais de um **XLOPER**/ **XLOPER12**s em uma única chamada de **xlFree**, limitado somente pelo número de argumentos da função compatíveis com a versão em execução do Excel (30 no Excel 2003, 255 iniciada no Excel 2007).</span><span class="sxs-lookup"><span data-stu-id="9383a-155">You can pass pointers to more than one **XLOPER**/ **XLOPER12**s in a single call to **xlFree**, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in Excel 2007).</span></span>
    
- <span data-ttu-id="9383a-156">**xlFree** define o ponteiro contido como **Nulo** para garantir que uma tentativa de liberar um **XLOPER**/ **XLOPER12** que já foi liberada é seguro.</span><span class="sxs-lookup"><span data-stu-id="9383a-156">**xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe.</span></span> <span data-ttu-id="9383a-157">**xlFree** é a única função de API C que modifica seus argumentos.</span><span class="sxs-lookup"><span data-stu-id="9383a-157">**xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="9383a-158">Você pode chamar com segurança **xlFree** em qualquer **XLOPER**/ **XLOPER12** usado para o valor de retorno de uma chamada para a API C, independentemente se ele contém um ponteiro para a memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-158">You can safely call **xlFree** on any **XLOPER**/ **XLOPER12** used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="9383a-159">Retornando XLOPER/XLOPER12s serem liberados pelo Excel</span><span class="sxs-lookup"><span data-stu-id="9383a-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="9383a-160">Suponha que você queria modificar o comando de exemplo na seção anterior e alterá-la para uma função de planilha que retorna o caminho e nome da DLL quando passado um argumento **booleano** de **true** e **# N/d** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9383a-160">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise.</span></span> <span data-ttu-id="9383a-161">Sem dúvida, você não pode chamar **xlFree** para liberar memória a cadeia de caracteres antes de retorná-la para o Excel.</span><span class="sxs-lookup"><span data-stu-id="9383a-161">Clearly you cannot call **xlFree** to release the string memory before returning it to Excel.</span></span> <span data-ttu-id="9383a-162">No entanto, se ela não é liberada em algum momento, o suplemento será vazamento de memória sempre que a função for chamada.</span><span class="sxs-lookup"><span data-stu-id="9383a-162">However, if it is not freed at some point, the add-in will leak memory every time the function is called.</span></span> <span data-ttu-id="9383a-163">Para contornar esse problema, você pode definir um pouco no campo **xltype** da **XLOPER**/ **XLOPER12**, definido como **xlbitXLFree** no xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="9383a-163">To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h.</span></span> <span data-ttu-id="9383a-164">Essa configuração informa ao Excel que ele deve liberar a memória retornada quando ele tiver terminado, copiando o valor.</span><span class="sxs-lookup"><span data-stu-id="9383a-164">Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="9383a-165">Example</span><span class="sxs-lookup"><span data-stu-id="9383a-165">Example</span></span>

<span data-ttu-id="9383a-166">O exemplo de código a seguir mostra o comando XLL na seção anterior convertida em uma função de planilha XLL.</span><span class="sxs-lookup"><span data-stu-id="9383a-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
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

<span data-ttu-id="9383a-167">Funções XLL que usam **XLOPER**/ **XLOPER12**s deve ser declarada como levando e retornando ponteiros para **XLOPER**/ **XLOPER12**s.</span><span class="sxs-lookup"><span data-stu-id="9383a-167">XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s.</span></span> <span data-ttu-id="9383a-168">O uso neste exemplo de uma estática **XLOPER12** dentro da função não é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="9383a-168">The use in this example of a static **XLOPER12** within the function is not thread safe.</span></span> <span data-ttu-id="9383a-169">Você pode registrar incorretamente dessa função como thread-safe, mas você poderia ser um risco **xRtnValue** sejam sobrescritos por um segmento antes de outro thread tinha concluído com ele.</span><span class="sxs-lookup"><span data-stu-id="9383a-169">You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="9383a-170">Você deve definir **xlbitXLFree** após a chamada para o retorno de chamada do Excel que aloca-lo.</span><span class="sxs-lookup"><span data-stu-id="9383a-170">You must set **xlbitXLFree** after the call to the Excel callback that allocates it.</span></span> <span data-ttu-id="9383a-171">Se você defini-la antes que isso, ele será substituído e não tem o efeito que você deseja.</span><span class="sxs-lookup"><span data-stu-id="9383a-171">If you set it before this, it is overwritten and does not have the effect that you want.</span></span> <span data-ttu-id="9383a-172">Se você pretende usar o valor como um argumento em uma chamada para outra função do C API antes de retorná-la à planilha, você deve definir esse bit após qualquer tal chamada.</span><span class="sxs-lookup"><span data-stu-id="9383a-172">If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call.</span></span> <span data-ttu-id="9383a-173">Caso contrário, você irá confunda funções que não mascarar esse bit antes de verificar **XLOPER**/ **XLLOPER12** tipo.</span><span class="sxs-lookup"><span data-stu-id="9383a-173">Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="9383a-174">Retornando XLOPER/XLOPER12s serem liberados pela DLL</span><span class="sxs-lookup"><span data-stu-id="9383a-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="9383a-175">Um problema semelhante a isso ocorre quando o seu XLL tem memória alocada para **XLOPER**/ **XLOPER12** e quer retorná-lo para o Excel.</span><span class="sxs-lookup"><span data-stu-id="9383a-175">A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel.</span></span> <span data-ttu-id="9383a-176">O Excel reconhece outra bit que pode ser definida no campo **xltype** da **XLOPER**/ **XLOPER12**, definido como **xlbitDLLFree** em xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="9383a-176">Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h.</span></span> 
  
<span data-ttu-id="9383a-177">Quando o Excel recebe **um XLOPER**/ **XLOPER12** com esse bit definido, ele tentará chamar uma função que deve ser exportada pelo XLL chamado [xlAutoFree](xlautofree-xlautofree12.md) (para **XLOPER**s) ou **xlAutoFree12** (para **XLOPER12**s).</span><span class="sxs-lookup"><span data-stu-id="9383a-177">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s).</span></span> <span data-ttu-id="9383a-178">Essa função é descrita com mais detalhes na referência de função (consulte [Gerenciador de suplementos e funções da Interface XLL](add-in-manager-and-xll-interface-functions.md)), mas um exemplo de implementação mínimo é fornecido aqui.</span><span class="sxs-lookup"><span data-stu-id="9383a-178">This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here.</span></span> <span data-ttu-id="9383a-179">Seu objetivo é livre **XLOPER**/ **XLOPER12** memória de forma consistente com como ela foi originalmente alocada.</span><span class="sxs-lookup"><span data-stu-id="9383a-179">Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="9383a-180">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9383a-180">Examples</span></span>

<span data-ttu-id="9383a-181">A função de exemplo a seguir faz o mesmo que a função anterior, exceto que inclui o texto "o nome do caminho completo para essa DLL é" antes do nome da DLL.</span><span class="sxs-lookup"><span data-stu-id="9383a-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
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

<span data-ttu-id="9383a-182">Uma implementação minimamente suficiente de **xlAutoFree12** em XLL que exportou a função anterior seria da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="9383a-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="9383a-183">Essa implementação é suficiente apenas se o XLL retorna apenas **XLOPER12** cadeias de caracteres, e essas cadeias de caracteres somente são alocadas usando **malloc**.</span><span class="sxs-lookup"><span data-stu-id="9383a-183">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**.</span></span> <span data-ttu-id="9383a-184">Observe que o teste</span><span class="sxs-lookup"><span data-stu-id="9383a-184">Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="9383a-185">falhará neste caso porque **xlbitDLLFree** está definido.</span><span class="sxs-lookup"><span data-stu-id="9383a-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="9383a-186">Em geral, **xlAutoFree** e **xlAutoFree12** devem ser implementados para que eles liberar memória associada criados XLL **xltypeMulti** matrizes e **xltypeRef** as referências externas.</span><span class="sxs-lookup"><span data-stu-id="9383a-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="9383a-187">Talvez você decida implementar suas funções XLL, para que eles todos retorno alocadas dinamicamente s **XLOPER**e **XLOPER12**s.</span><span class="sxs-lookup"><span data-stu-id="9383a-187">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s.</span></span> <span data-ttu-id="9383a-188">Nesse caso, você precisaria definir **xlbitDLLFree** todos os tais s **XLOPER**e **XLOPER12**s independentemente do subtipo.</span><span class="sxs-lookup"><span data-stu-id="9383a-188">In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type.</span></span> <span data-ttu-id="9383a-189">Você também precisará implementar **xlAutoFree** e **xlAutoFree12** para que essa memória foi liberada e também qualquer memória apontado para dentro **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="9383a-189">You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**.</span></span> <span data-ttu-id="9383a-190">Essa abordagem é uma maneira de fazer o thread de valor de retorno seguros.</span><span class="sxs-lookup"><span data-stu-id="9383a-190">This approach is one way to make the return value thread safe.</span></span> <span data-ttu-id="9383a-191">Por exemplo, a função anterior poderia ser reescrita da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="9383a-191">For example, the previous function could be rewritten as follows.</span></span>
  
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

<span data-ttu-id="9383a-192">Para obter mais informações sobre **xlAutoFree** e **xlAutoFree12**, consulte [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span><span class="sxs-lookup"><span data-stu-id="9383a-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="9383a-193">Retornando argumentos modificar-in-loco</span><span class="sxs-lookup"><span data-stu-id="9383a-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="9383a-194">Excel permite que uma função XLL retornar um valor modificando um argumento in-loco.</span><span class="sxs-lookup"><span data-stu-id="9383a-194">Excel allows an XLL function to return a value by modifying an argument in place.</span></span> <span data-ttu-id="9383a-195">Você só pode fazer isso com um argumento passado como um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="9383a-195">You can only do this with an argument passed in as a pointer.</span></span> <span data-ttu-id="9383a-196">Para trabalhar assim, a função deve ser registrada de forma que informa ao Excel qual argumento será modificado.</span><span class="sxs-lookup"><span data-stu-id="9383a-196">To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="9383a-197">Esse método de retornar um valor é suportado para todos os tipos de dados que podem ser passados pelo ponteiro, mas é especialmente útil para os seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="9383a-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="9383a-198">Comprimento contado e terminada em nulo cadeias de caracteres de byte de ASCII</span><span class="sxs-lookup"><span data-stu-id="9383a-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="9383a-199">Comprimento contado e terminada em nulo cadeias de caracteres longa de Unicode (começando no Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="9383a-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="9383a-200">Matrizes de ponto flutuante **FP**</span><span class="sxs-lookup"><span data-stu-id="9383a-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="9383a-201">Matrizes de ponto flutuante **FP12** (começando no Excel 2007)</span><span class="sxs-lookup"><span data-stu-id="9383a-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="9383a-202">Você não deve tentar retornar **XLOPER**s ou s **XLOPER12**dessa maneira.</span><span class="sxs-lookup"><span data-stu-id="9383a-202">You should not try to return **XLOPER**s or **XLOPER12**s in this manner.</span></span> <span data-ttu-id="9383a-203">Para obter mais informações, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="9383a-203">For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="9383a-204">A vantagem de usar essa técnica, em vez de usar apenas a instrução retornar, é que o Excel aloca a memória para os valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="9383a-204">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values.</span></span> <span data-ttu-id="9383a-205">Depois que o Excel concluiu a ler os dados retornados, ele libera a memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-205">Once Excel has finished reading the returned data, it releases the memory.</span></span> <span data-ttu-id="9383a-206">Isso leva a memória para tarefas de gerenciamento, separando-a função XLL.</span><span class="sxs-lookup"><span data-stu-id="9383a-206">This takes the memory management tasks away from the XLL function.</span></span> <span data-ttu-id="9383a-207">Essa técnica é thread-safe: se chamado simultaneamente pelo Excel em threads diferentes, cada chamada de função em cada segmento tem seu próprio buffer.</span><span class="sxs-lookup"><span data-stu-id="9383a-207">This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="9383a-208">É útil para os tipos de dados listados anteriormente em particular porque o mecanismo de chamada de volta a DLL para liberar memória POST-retornar que existe para **XLOPER**/ **XLOPER12**s não existe para cadeias de caracteres simples e **FP** /  Matrizes de **FP12** .</span><span class="sxs-lookup"><span data-stu-id="9383a-208">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12**s does not exist for simple strings and **FP**/ **FP12** arrays.</span></span> <span data-ttu-id="9383a-209">Portanto, ao retornar uma cadeia de caracteres criada a DLL ou matriz de ponto flutuante, você tem as seguintes opções:</span><span class="sxs-lookup"><span data-stu-id="9383a-209">Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="9383a-210">Definir um ponteiro persistente em um buffer alocado dinamicamente, o ponteiro de retorno.</span><span class="sxs-lookup"><span data-stu-id="9383a-210">Set a persistent pointer to a dynamically allocated buffer, return the pointer.</span></span> <span data-ttu-id="9383a-211">Na próxima chamada para a função (1) verificação de que o ponteiro não é nula (2) gratuito os recursos alocados na chamada anterior em Redefinir o ponteiro como null, (3) reutilização o ponteiro para um bloco recentemente alocado de memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-211">On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="9383a-212">Crie seu cadeias de caracteres e matrizes em um buffer estático que não precisam ser liberados e retornar um ponteiro para que.</span><span class="sxs-lookup"><span data-stu-id="9383a-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="9383a-213">Modifica um argumento in-loco, gravar sua cadeia de caracteres ou matriz diretamente para o espaço reservado pelo Excel.</span><span class="sxs-lookup"><span data-stu-id="9383a-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="9383a-214">Caso contrário, você deve criar um **XLOPER**/ **XLOPER12**e uso **xlbitDLLFree** e **xlAutoFree**/ **xlAutoFree12** para liberar os recursos.</span><span class="sxs-lookup"><span data-stu-id="9383a-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span></span> 
  
<span data-ttu-id="9383a-215">A última opção pode ser o mais simples nesses casos em que você está sendo um argumento do mesmo tipo passados como o valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="9383a-215">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value.</span></span> <span data-ttu-id="9383a-216">O ponto-chave lembrar é que os tamanhos de buffer são limitados e você deve tomar muito cuidado para não saturação-los.</span><span class="sxs-lookup"><span data-stu-id="9383a-216">The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them.</span></span> <span data-ttu-id="9383a-217">Obter isso errado poderia falha no Excel.</span><span class="sxs-lookup"><span data-stu-id="9383a-217">Getting this wrong could crash Excel.</span></span> <span data-ttu-id="9383a-218">Tamanhos de cadeias de caracteres e **FP**de buffer/ **FP12** matrizes são abordadas em Avançar.</span><span class="sxs-lookup"><span data-stu-id="9383a-218">Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="9383a-219">Cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="9383a-219">Strings</span></span>

<span data-ttu-id="9383a-220">Problemas com o gerenciamento de memória de cadeia de caracteres relativamente são a causa mais comum de instabilidade em suplementos e aplicativos. É compreensível talvez, dado a várias maneiras em que as cadeias de caracteres são tratadas: terminada em nulo ou comprimento contado (ou ambos); buffers estáticos ou dinâmicos; comprimento fixo ou comprimento quase ilimitado; sistema operacional gerenciadas (por exemplo, denominadas Bstr OLE) de memória ou não gerenciadas cadeias de caracteres; e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="9383a-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="9383a-221">Programadores C/C++ estão mais familiarizados com cadeias de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="9383a-221">C/C++ programmers are most familiar with null-terminated strings.</span></span> <span data-ttu-id="9383a-222">A biblioteca C padrão é projetada para funcionar com essas cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9383a-222">The standard C library is designed to work with such strings.</span></span> <span data-ttu-id="9383a-223">Os literais de cadeia de caracteres estática no código são compilados em cadeias de caracteres terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="9383a-223">Static string literals in code are compiled into null-terminated strings.</span></span> <span data-ttu-id="9383a-224">Como alternativa, o Excel funciona com comprimento contado as cadeias de caracteres que não são em geral terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="9383a-224">Alternatively, Excel works with length-counted strings that are not in general null-terminated.</span></span> <span data-ttu-id="9383a-225">A combinação desses fatos requer uma abordagem clara e consistente dentro de sua DLL/XLL relacionadas a como você manipular cadeias de caracteres e memória de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9383a-225">The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="9383a-226">Os problemas mais comuns são:</span><span class="sxs-lookup"><span data-stu-id="9383a-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="9383a-227">A passagem de um ponteiro nulo ou inválido para uma função que espera um ponteiro válido e não aparecer ou não é possível verificar a validade do ponteiro em si.</span><span class="sxs-lookup"><span data-stu-id="9383a-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="9383a-228">Saturar os limites de um buffer de cadeia de caracteres por uma função que não aparecer ou não é possível verificar o tamanho do buffer contra o comprimento da cadeia de caracteres que está sendo gravado.</span><span class="sxs-lookup"><span data-stu-id="9383a-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="9383a-229">Tentando liberar memória de buffer de cadeia de caracteres que é estáticas, foi liberada já ou não foi alocada de forma que é consistente com como está sendo liberada.</span><span class="sxs-lookup"><span data-stu-id="9383a-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="9383a-230">O vazamento de memória que resultam de cadeias de caracteres que está sendo alocado e, em seguida, não liberada, geralmente em uma função chamada com frequência.</span><span class="sxs-lookup"><span data-stu-id="9383a-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="9383a-231">Regras de cadeias de caracteres</span><span class="sxs-lookup"><span data-stu-id="9383a-231">Rules for Strings</span></span>

<span data-ttu-id="9383a-232">Como ocorre com **XLOPER**/ s**XLOPER**, há regras e diretrizes que você deve seguir.</span><span class="sxs-lookup"><span data-stu-id="9383a-232">As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow.</span></span> <span data-ttu-id="9383a-233">As diretrizes são os mesmos determinado na seção anterior.</span><span class="sxs-lookup"><span data-stu-id="9383a-233">The guidelines are the same as given in the previous section.</span></span> <span data-ttu-id="9383a-234">As regras aqui são uma extensão das regras especificamente para as cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9383a-234">The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="9383a-235">**Regras:**</span><span class="sxs-lookup"><span data-stu-id="9383a-235">**Rules:**</span></span>
  
- <span data-ttu-id="9383a-236">Não tente liberar memória ou substituir a cadeia de caracteres **XLOPER**/ **XLOPER12**s ou simples cadeias de caracteres de comprimento contado ou terminada em nulo passados como argumentos para sua função XLL.</span><span class="sxs-lookup"><span data-stu-id="9383a-236">Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12**s or simple length-counted or null-terminated strings passed as arguments to your XLL function.</span></span> <span data-ttu-id="9383a-237">Você deve tratar tais argumentos como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9383a-237">You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="9383a-238">Onde o Excel aloca memória para uma cadeia de caracteres **XLOPER**/ **XLOPER12** para o valor de retorno de uma função de retorno de chamada da API C, use **xlFree** para liberá-la ou definir **xlbitXLFree** se retorná-lo para o Excel de uma função XLL.</span><span class="sxs-lookup"><span data-stu-id="9383a-238">Where Excel allocates memory for a string **XLOPER**/ **XLOPER12** for the return value of a C API callback function, use **xlFree** to free it, or set **xlbitXLFree** if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="9383a-239">Onde sua DLL dinamicamente aloca um buffer de cadeia de caracteres para um **XLOPER**/ **XLOPER12**, liberá-la de forma consistente com como alocado-lo quando feito ou defina **xlbitDLLFree** se retorná-lo para o Excel de uma função XLL e, em seguida, liberá-la em **xlAutoFree** /  **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="9383a-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span></span>
    
- <span data-ttu-id="9383a-240">Se o Excel tem memória alocada para uma matriz de **xltypeMulti** retornada para sua DLL em uma chamada para a API C, não substituir qualquer cadeia de caracteres **XLOPER**/ **XLOPER12**s dentro da matriz.</span><span class="sxs-lookup"><span data-stu-id="9383a-240">If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12**s within the array.</span></span> <span data-ttu-id="9383a-241">Tais matrizes somente devem ser liberados usando **xlFree**, ou, se estiver sendo retornados por uma função XLL, definindo **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="9383a-241">Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="9383a-242">Tipos de cadeia de caracteres com suporte</span><span class="sxs-lookup"><span data-stu-id="9383a-242">String Types Supported</span></span>

<span data-ttu-id="9383a-243">**C API xltypeStr XLOPER/XLOPER12s**</span><span class="sxs-lookup"><span data-stu-id="9383a-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="9383a-244">\* \* Cadeias de caracteres byte: \* \* XLOPER \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9383a-244">**Byte strings: **XLOPER****</span></span>|<span data-ttu-id="9383a-245">\* \* Larga cadeias de caracteres: \* \* XLOPER12 \* \* \*</span><span class="sxs-lookup"><span data-stu-id="9383a-245">**Wide character strings: **XLOPER12****</span></span>|
|:-----|:-----|
|<span data-ttu-id="9383a-246">Todas as versões do Excel</span><span class="sxs-lookup"><span data-stu-id="9383a-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="9383a-247">Iniciando no Excel 2007</span><span class="sxs-lookup"><span data-stu-id="9383a-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="9383a-248">Comprimento máximo: 255 estendido bytes ASCII</span><span class="sxs-lookup"><span data-stu-id="9383a-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="9383a-249">Comprimento máximo 32.767 caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="9383a-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="9383a-250">Primeiro byte (não assinado) = comprimento</span><span class="sxs-lookup"><span data-stu-id="9383a-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="9383a-251">Primeiro caractere Unicode = comprimento</span><span class="sxs-lookup"><span data-stu-id="9383a-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="9383a-252">Não presuma finalização null das cadeias de caracteres **XLOPER** ou **XLOPER12** .</span><span class="sxs-lookup"><span data-stu-id="9383a-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="9383a-253">**Cadeias de caracteres do C/C++**</span><span class="sxs-lookup"><span data-stu-id="9383a-253">**C/C++ strings**</span></span>

|<span data-ttu-id="9383a-254">**Cadeias de caracteres de byte**</span><span class="sxs-lookup"><span data-stu-id="9383a-254">**Byte strings**</span></span>|<span data-ttu-id="9383a-255">**Cadeias de caracteres longa**</span><span class="sxs-lookup"><span data-stu-id="9383a-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9383a-256">Terminada em nulo (**char** \*) "C" comprimento máximo: 255 estendido bytes ASCII</span><span class="sxs-lookup"><span data-stu-id="9383a-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="9383a-257">Terminada em nulo (**wchar_t** \*) "C %" comprimento de máximo 32.767 caracteres Unicode</span><span class="sxs-lookup"><span data-stu-id="9383a-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="9383a-258">Comprimento contado (**não assinados char** \*) "D"</span><span class="sxs-lookup"><span data-stu-id="9383a-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="9383a-259">Comprimento contado (**wchar_t** \*) "D %"</span><span class="sxs-lookup"><span data-stu-id="9383a-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="9383a-260">Cadeias de caracteres em xltypeMulti XLOPER/XLOPER12 matrizes</span><span class="sxs-lookup"><span data-stu-id="9383a-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="9383a-261">Em alguns casos, o Excel criará uma matriz **xltypeMulti** para uso na sua DLL/XLL.</span><span class="sxs-lookup"><span data-stu-id="9383a-261">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL.</span></span> <span data-ttu-id="9383a-262">Várias das funções de informações de XLM retornam tais matrizes.</span><span class="sxs-lookup"><span data-stu-id="9383a-262">Several of the XLM information functions return such arrays.</span></span> <span data-ttu-id="9383a-263">Por exemplo, a API C função **xlfGetWorkspace**, quando passados o argumento *44* , retorna uma matriz que contém as cadeias de caracteres que descrevem todos os procedimentos DLL registrados no momento.</span><span class="sxs-lookup"><span data-stu-id="9383a-263">For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures.</span></span> <span data-ttu-id="9383a-264">A função do C API **xlfDialogBox** retorna uma cópia de modificação do seu argumento de matriz, contendo as cópias profundas das cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9383a-264">The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings.</span></span> <span data-ttu-id="9383a-265">Talvez a maneira mais comum de que um XLL encontra uma matriz **xltypeMulti** é onde ele foi passado como um argumento para uma função XLL ou foi forçado a esse tipo de uma referência de intervalo.</span><span class="sxs-lookup"><span data-stu-id="9383a-265">Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference.</span></span> <span data-ttu-id="9383a-266">Nesses casos último, o Excel cria cópias profundas das cadeias de caracteres nas células de origem e pontos a essas dentro da matriz.</span><span class="sxs-lookup"><span data-stu-id="9383a-266">In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="9383a-267">Onde você deseja modificar essas cadeias de caracteres na sua DLL, você deve fazer seus próprios cópias profundas.</span><span class="sxs-lookup"><span data-stu-id="9383a-267">Where you want to modify these strings in your DLL, you should make your own deep copies.</span></span> <span data-ttu-id="9383a-268">Quando você estiver criando seus próprio matrizes **xltypeMulti** , você não deve colocar a cadeia de caracteres alocado pelo Excel **XLOPER**/ **XLOPER12**s dentro deles.</span><span class="sxs-lookup"><span data-stu-id="9383a-268">When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them.</span></span> <span data-ttu-id="9383a-269">Os riscos não liberando corretamente mais tarde, ou não dispensando-los.</span><span class="sxs-lookup"><span data-stu-id="9383a-269">This risks you not freeing them correctly later, or not freeing them at all.</span></span> <span data-ttu-id="9383a-270">Novamente, você deve fazer cópias profundas das cadeias de caracteres e armazenar ponteiros para as cópias na matriz.</span><span class="sxs-lookup"><span data-stu-id="9383a-270">Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="9383a-271">**Exemplos**</span><span class="sxs-lookup"><span data-stu-id="9383a-271">**Examples**</span></span>
  
<span data-ttu-id="9383a-272">A função de exemplo a seguir cria uma cópia alocada dinamicamente de uma cadeia de caracteres Unicode de comprimento contado.</span><span class="sxs-lookup"><span data-stu-id="9383a-272">The following example function creates a dynamically allocated copy of a length-counted Unicode string.</span></span> <span data-ttu-id="9383a-273">Observe que o chamador basicamente deve liberar a memória alocada neste exemplo usando [] de **Excluir**, e que a cadeia de caracteres de origem não é assumida como nulo encerrada.</span><span class="sxs-lookup"><span data-stu-id="9383a-273">Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated.</span></span> <span data-ttu-id="9383a-274">A cadeia de caracteres de cópia será truncada se necessário para segurança e não for nula finalizada.</span><span class="sxs-lookup"><span data-stu-id="9383a-274">The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
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

<span data-ttu-id="9383a-275">Essa função, em seguida, pode ser usada com segurança para copiar **XLOPER12**, conforme mostrado na seguinte exportável XLL função que retorna uma cópia do seu argumento se ele for uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9383a-275">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string.</span></span> <span data-ttu-id="9383a-276">Todos os outros tipos são retornados como uma cadeia de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="9383a-276">All other types are returned as a zero-length string.</span></span> <span data-ttu-id="9383a-277">Observe que os intervalos não são manipulados — a função retornará **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="9383a-277">Note that ranges are not handled—the function returns **#VALUE!**.</span></span> <span data-ttu-id="9383a-278">A função deve ser registrada como colocar um argumento de tipo U para que as referências são passadas como valores.</span><span class="sxs-lookup"><span data-stu-id="9383a-278">The function must be registered as taking a type U argument so that references are passed in as values.</span></span> <span data-ttu-id="9383a-279">Isso é equivalente à função de planilha internas **T()** , exceto que **AsText** também converte erros em cadeias de caracteres de comprimento zero.</span><span class="sxs-lookup"><span data-stu-id="9383a-279">This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings.</span></span> <span data-ttu-id="9383a-280">Este exemplo de código pressupõe que **xlAutoFree12** libera o ponteiro no passado e também seu conteúdo, usando a **Excluir**.</span><span class="sxs-lookup"><span data-stu-id="9383a-280">This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
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

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="9383a-281">Retornando argumentos de cadeia de caracteres de modificar-in-loco</span><span class="sxs-lookup"><span data-stu-id="9383a-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="9383a-282">Argumentos são registrados como tipos **F**, **G**, **F %** e **% G** podem ser modificados no lugar.</span><span class="sxs-lookup"><span data-stu-id="9383a-282">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place.</span></span> <span data-ttu-id="9383a-283">Quando o Excel está preparando argumentos de cadeia de caracteres para esses tipos, ele cria um buffer de tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="9383a-283">When Excel is preparing string arguments for these types, it creates a maximum length buffer.</span></span> <span data-ttu-id="9383a-284">Em seguida, ele copia a cadeia de caracteres de argumento para que, mesmo se esta cadeia de caracteres é muito menor.</span><span class="sxs-lookup"><span data-stu-id="9383a-284">Then it copies the argument string into that, even if this string is very much shorter.</span></span> <span data-ttu-id="9383a-285">Isso permite que a função XLL gravar seu valor de retorno diretamente para a mesma memória.</span><span class="sxs-lookup"><span data-stu-id="9383a-285">This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="9383a-286">Tamanhos de buffer isolam para esses tipos são:</span><span class="sxs-lookup"><span data-stu-id="9383a-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="9383a-287">**Cadeias de caracteres de byte:** 256 bytes incluindo o contador de comprimento (tipo G) ou finalização null (tipo F).</span><span class="sxs-lookup"><span data-stu-id="9383a-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="9383a-288">**Cadeias de caracteres Unicode:** 32.768 ampla caracteres (65.536 bytes) incluindo o contador de comprimento (% de tipo G) ou finalização null (tipo F %).</span><span class="sxs-lookup"><span data-stu-id="9383a-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="9383a-289">Você não pode chamar tal função diretamente do Visual Basic for Applications (VBA) porque você não pode garantir que um buffer suficientemente grande foi alocado.</span><span class="sxs-lookup"><span data-stu-id="9383a-289">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated.</span></span> <span data-ttu-id="9383a-290">Você só pode chamar tal função a partir de outro DLL com segurança se você tiver passado explicitamente um buffer grande o suficiente.</span><span class="sxs-lookup"><span data-stu-id="9383a-290">You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="9383a-291">Aqui está um exemplo de uma função XLL que reverte uma cadeia de caracteres passada em caracteres terminada em nulo ampla usando a função de biblioteca padrão **wcsrev**.</span><span class="sxs-lookup"><span data-stu-id="9383a-291">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**.</span></span> <span data-ttu-id="9383a-292">O argumento neste caso seria ser registrado como tipo **F %**.</span><span class="sxs-lookup"><span data-stu-id="9383a-292">The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="9383a-293">Armazenamento persistente (nomes de binários)</span><span class="sxs-lookup"><span data-stu-id="9383a-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="9383a-294">Nomes de binários são definidos e associados blocos de binário, ou seja, os dados não estruturados, que são armazenados em conjunto com a pasta de trabalho.</span><span class="sxs-lookup"><span data-stu-id="9383a-294">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook.</span></span> <span data-ttu-id="9383a-295">Eles são criados usando a função [xlDefineBinaryName](xldefinebinaryname.md)e os dados são recuperados usando a função [xlGetBinaryName](xlgetbinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="9383a-295">They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md).</span></span> <span data-ttu-id="9383a-296">Ambas as funções são descritas em mais detalhes na referência de função (consulte [C API funções que pode ser chamado apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), e ambos usam **xltypeBigData** **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="9383a-296">Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="9383a-297">Para obter informações sobre problemas conhecidos que limitam as aplicações práticas de nomes de binários, consulte [Problemas conhecidos no desenvolvimento de XLL do Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="9383a-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="9383a-298">Pilha do Excel</span><span class="sxs-lookup"><span data-stu-id="9383a-298">Excel Stack</span></span>

<span data-ttu-id="9383a-299">Excel compartilha seu espaço de pilha com todas as DLLs que ele tenha carregado.</span><span class="sxs-lookup"><span data-stu-id="9383a-299">Excel shares its stack space with all the DLLs it has loaded.</span></span> <span data-ttu-id="9383a-300">Espaço em pilha geralmente é mais do que adequado para uso comum, e você não precisará se preocupar com ele, desde que você seguir algumas diretrizes:</span><span class="sxs-lookup"><span data-stu-id="9383a-300">Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="9383a-301">Não passe estruturas muito grandes como argumentos às funções pelo valor na pilha.</span><span class="sxs-lookup"><span data-stu-id="9383a-301">Do not pass very large structures as arguments to functions by value on the stack.</span></span> <span data-ttu-id="9383a-302">Passe ponteiros ou referências em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9383a-302">Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="9383a-303">Não retornam estruturas grandes na pilha.</span><span class="sxs-lookup"><span data-stu-id="9383a-303">Do not return large structures on the stack.</span></span> <span data-ttu-id="9383a-304">Retornam ponteiros para memória estática ou alocada dinamicamente ou usar os argumentos passados por referência.</span><span class="sxs-lookup"><span data-stu-id="9383a-304">Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="9383a-305">Não declare muito grandes estruturas variáveis automáticas no código de função.</span><span class="sxs-lookup"><span data-stu-id="9383a-305">Do not declare very large automatic variable structures in the function code.</span></span> <span data-ttu-id="9383a-306">Se você precisar deles, declare-las como estático.</span><span class="sxs-lookup"><span data-stu-id="9383a-306">If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="9383a-307">Não chame funções recursivamente menos que tenha certeza de que a profundidade de recursão sempre será superficial.</span><span class="sxs-lookup"><span data-stu-id="9383a-307">Do not call functions recursively unless you are sure the depth of recursion will always be shallow.</span></span> <span data-ttu-id="9383a-308">Tente usar um loop em vez disso.</span><span class="sxs-lookup"><span data-stu-id="9383a-308">Try using a loop instead.</span></span>
    
<span data-ttu-id="9383a-309">Quando uma DLL chama de volta para o Excel usando a API C, o Excel primeiro verifica se há espaço suficiente na pilha para a chamada de pior caso de uso que poderia ser feita.</span><span class="sxs-lookup"><span data-stu-id="9383a-309">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made.</span></span> <span data-ttu-id="9383a-310">Se ele achar que pode haver espaço insuficiente, ele falhará a chamada para ser seguro, mesmo que realmente tenha sido espaço suficiente para essa chamada específica.</span><span class="sxs-lookup"><span data-stu-id="9383a-310">If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call.</span></span> <span data-ttu-id="9383a-311">Nesse caso, os retornos de chamada retornam o código **xlretFailed**.</span><span class="sxs-lookup"><span data-stu-id="9383a-311">In this case, the callbacks return the code **xlretFailed**.</span></span> <span data-ttu-id="9383a-312">Para uso comum da API C e a pilha de itens, esse é um improvável motivo da falha de uma chamada de API C.</span><span class="sxs-lookup"><span data-stu-id="9383a-312">For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="9383a-313">Se você estiver preocupado ou apenas curioso, ou você deseja eliminar falta de espaço em pilha como um motivo para uma falha inexplicado, você pode descobrir quanto espaço de pilha lá está com uma chamada para a função [xlStack](xlstack.md) .</span><span class="sxs-lookup"><span data-stu-id="9383a-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9383a-314">Confira também</span><span class="sxs-lookup"><span data-stu-id="9383a-314">See also</span></span>



[<span data-ttu-id="9383a-315">Recálculo multithreaded no Excel</span><span class="sxs-lookup"><span data-stu-id="9383a-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="9383a-316">Multithreading e contenção de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="9383a-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="9383a-317">Developing Excel XLLs</span><span class="sxs-lookup"><span data-stu-id="9383a-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

