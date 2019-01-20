---
title: Chamar no Excel a partir de DLL ou XLL
manager: soliver
ms.date: 08/22/2018
ms.audience: Developer
ms.topic: overview
keywords:
- caixas de diálogo [excel 2007], chamando comandos excel, DLLs [Excel 2007], chamando para o Excel, passando argumentos para funções da API C [Excel 2007], comandos [Excel 2007], invocando caixas de diálogo, comandos [Excel 2007], acessíveis da DLL / XLL, função Excel4 [Excel 2007], função Excel12 [Excel 2007], função XLCallVer [Excel 2007], argumento operRes [Excel 2007], funções [Excel 2007], acessíveis da DLL / XLL, função Excel12v [Excel 2007 ], Somente funções DLL [Excel 2007], API C [Excel 2007], passando argumentos, argumento de contagem [Excel 2007], comandos [Excel 2007], chamadas em versões internacionais, comandos somente DLL [Excel 2007], versões internacionais [Excel 2007], chamando funções e comandos, XLLs [Excel 2007], chamando em Excel, função Excel 4v [Excel 2007], argumento xlfn [Excel 2007], funções [Excel 2007], chamando em versões internacionais
ms.assetid: 616e3def-e4ec-4f3c-bc65-3b92710da1e6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 8f2b63ba84b0a78bbf317c284913a8ec0986436f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726117"
---
# <a name="calling-into-excel-from-the-dll-or-xll"></a><span data-ttu-id="bd103-104">Chamar no Excel a partir de DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="bd103-104">Calling into Excel from the DLL or XLL</span></span>

<span data-ttu-id="bd103-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="bd103-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="bd103-106">O Microsoft Excel permite que sua DLL acesse comandos incorporados do Excel, funções de planilha e funções de folha de macro.</span><span class="sxs-lookup"><span data-stu-id="bd103-106">Microsoft Excel enables your DLL to access built-in Excel commands, worksheet functions, and macro sheet functions.</span></span> <span data-ttu-id="bd103-107">Eles estão disponíveis em comandos e funções da DLL chamados do Visual Basic for Applications (VBA) e de comandos e funções XLL registrados, chamados diretamente pelo Excel.</span><span class="sxs-lookup"><span data-stu-id="bd103-107">These are available both from DLL commands and functions called from Visual Basic for Applications (VBA), and from registered XLL commands and functions called directly by Excel.</span></span>
  
## <a name="excel4-excel4v-excel12-and-excel12v-functions"></a><span data-ttu-id="bd103-108">Funções Excel4, Excel4v, Excel12 e Excel12v </span><span class="sxs-lookup"><span data-stu-id="bd103-108">Excel4, Excel4v, Excel12, and Excel12v Functions</span></span>

<span data-ttu-id="bd103-109">O Excel permite que sua DLL acesse os comandos e funções por meio das funções de retorno de chamada [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), e [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="bd103-109">Excel enables your DLL to access the commands and functions through the callback functions [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), and [Excel12v](excel4v-excel12v.md).</span></span>
  
<span data-ttu-id="bd103-110">As funções**Excel4** e **Excel4v** foram introduzidas na versão 4.</span><span class="sxs-lookup"><span data-stu-id="bd103-110">The **Excel4** and **Excel4v** functions were introduced in Excel version 4.</span></span> <span data-ttu-id="bd103-111">Elas funcionam com a estrutura de dados **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="bd103-111">They work with the **XLOPER** data structure.</span></span> <span data-ttu-id="bd103-112">O Excel 2007 introduziu duas funções novas de retorno de chamada, **Excel12** e **Excel12v**, que funcionam com a estrutura de dados **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="bd103-112">Excel 2007 introduced two new callback functions, **Excel12** and **Excel12v**, which work with the **XLOPER12** data structure.</span></span> <span data-ttu-id="bd103-113">As funções **Excel4** e **Excel4v**são exportadas pela biblioteca Xlcall32.lib, que deve ser incluída no seu projeto DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="bd103-113">The **Excel4** and **Excel4v** functions are exported by the library Xlcall32.lib, which must be included in your DLL or XLL project.</span></span> <span data-ttu-id="bd103-114">**Excel12** e **Excel12v** estão incluídas no arquivo de origem do SDK C ++ Xlcall.cpp, que deve ser incluído no seu projeto se você deseja acessar a funcionalidade do Excel usando as estruturas **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="bd103-114">**Excel12** and **Excel12v** are included in the SDK C++ source file Xlcall.cpp, which must be included in your project if you want to access Excel functionality by using **XLOPER12** structures.</span></span> 
  
<span data-ttu-id="bd103-115">O código a seguir mostra os protótipos função dessas quatro funções.</span><span class="sxs-lookup"><span data-stu-id="bd103-115">The following code shows the function prototypes for these four functions.</span></span> <span data-ttu-id="bd103-116">Os três primeiros argumentos são iguais, exceto pelo fato de que o segundo argumento é um ponteiro para um **XLOPER** no primeiro par e o ponteiro para um **XLOPER12** no segundo par.</span><span class="sxs-lookup"><span data-stu-id="bd103-116">The first three arguments are the same except that the second argument is a pointer to an **XLOPER** in the first pair and a pointer to an **XLOPER12** in the second pair.</span></span> <span data-ttu-id="bd103-117">A convenção de chamada é **cdecl** no **Excel4** e **Excel12** para permitir que o argumento variável listas.</span><span class="sxs-lookup"><span data-stu-id="bd103-117">The calling convention is **_cdecl** in **Excel4** and **Excel12** to permit the variable argument lists.</span></span> <span data-ttu-id="bd103-118">As reticências representam ponteiros para os valores **XLOPER** para **Excel4** e valores **XLOPER12** para **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="bd103-118">The ellipsis represents pointers to **XLOPER** values for **Excel4** and **XLOPER12** values for **Excel12**.</span></span> <span data-ttu-id="bd103-119">O número de sugestões é igual ao valor do parâmetro _contagem_.</span><span class="sxs-lookup"><span data-stu-id="bd103-119">The number of pointers equals the value of the  _count_ parameter.</span></span> 
  
<span data-ttu-id="bd103-120">**Todas as versões do Excel**</span><span class="sxs-lookup"><span data-stu-id="bd103-120">**All versions of Excel:**</span></span>
  
 `int _cdecl Excel4(int xlfn, LPXLOPER operRes, int count,... );`
  
 `int pascal Excel4v(int xlfn, LPXLOPER operRes, int count, LPXLOPER opers[]);`
  
<span data-ttu-id="bd103-121">**Começando no Excel 2007**</span><span class="sxs-lookup"><span data-stu-id="bd103-121">**(starting in Excel 2007)**</span></span>
  
 `int _cdecl Excel12(int xlfn, LPXLOPER12 operRes, int count,... );`
  
 `int pascal Excel12v(int xlfn, LPXLOPER12 operRes, int count, LPXLOPER12 opers[]);`
  
<span data-ttu-id="bd103-122">Para a DLL fazer chamadas **Excel4**, **Excel4v**, **Excel12**, ou **Excel12v**, o Excel deve passar o controle para a DLL.</span><span class="sxs-lookup"><span data-stu-id="bd103-122">For the DLL to be able to call **Excel4**, **Excel4v**, **Excel12**, or **Excel12v**, Excel must pass control to the DLL.</span></span> <span data-ttu-id="bd103-123">Isso significa que esses retornos de chamada da API C podem ser chamados apenas nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="bd103-123">This means that these C API callbacks can be called only in the following scenarios:</span></span>
  
- <span data-ttu-id="bd103-124">De dentro de um comando XLL que o Excel chamou diretamente ou via VBA.</span><span class="sxs-lookup"><span data-stu-id="bd103-124">From within an XLL command that Excel has called directly or via VBA.</span></span>
    
- <span data-ttu-id="bd103-125">De dentro de uma planilha XLL ou função de folha de macro que o Excel chamou diretamente ou via VBA.</span><span class="sxs-lookup"><span data-stu-id="bd103-125">From within an XLL worksheet or macro sheet function that Excel has called directly or via VBA.</span></span>
    
<span data-ttu-id="bd103-126">Você não pode chamar o C API do Excel nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="bd103-126">You cannot call the Excel C API in the following scenarios:</span></span>
  
- <span data-ttu-id="bd103-127">De um evento do sistema operacional (por exemplo, função [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain)).</span><span class="sxs-lookup"><span data-stu-id="bd103-127">From an operating system event (for example, from the [DllMain](https://docs.microsoft.com/windows/desktop/dlls/dllmain) function).</span></span> 
    
- <span data-ttu-id="bd103-128">De um thread de segundo plano que sua DLL criou.</span><span class="sxs-lookup"><span data-stu-id="bd103-128">From a background thread that your DLL created.</span></span>
    
### <a name="return-values"></a><span data-ttu-id="bd103-129">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="bd103-129">Return values</span></span>

<span data-ttu-id="bd103-130">Todas as quatro funções retornam um valor inteiro que informa ao chamador se a função ou comando foi chamado com sucesso.</span><span class="sxs-lookup"><span data-stu-id="bd103-130">All four of these functions return an integer value that informs the caller whether the function or command was called successfully.</span></span> <span data-ttu-id="bd103-131">Os valores retornados podem ser um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="bd103-131">The returned string can be one of the following values: , , or .</span></span>
  
|<span data-ttu-id="bd103-132">**Valor de retorno**</span><span class="sxs-lookup"><span data-stu-id="bd103-132">**Return value**</span></span>|<span data-ttu-id="bd103-133">**Estipulados em xlcall. h como**</span><span class="sxs-lookup"><span data-stu-id="bd103-133">**Defined in Xlcall.h as**</span></span>|<span data-ttu-id="bd103-134">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bd103-134">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd103-135">0</span><span class="sxs-lookup"><span data-stu-id="bd103-135">(0)</span></span>  <br/> |<span data-ttu-id="bd103-136">**xlretSuccess**</span><span class="sxs-lookup"><span data-stu-id="bd103-136">**xlretSuccess**</span></span> <br/> |<span data-ttu-id="bd103-137">A função ou comando foi executada com êxito.</span><span class="sxs-lookup"><span data-stu-id="bd103-137">The function or command executed successfully.</span></span> <span data-ttu-id="bd103-138">Isso significa que a execução foi livre de erros.</span><span class="sxs-lookup"><span data-stu-id="bd103-138">This does not mean that the execution was error free.</span></span> <span data-ttu-id="bd103-139">Por exemplo, **Excel4** pode retornar **xlretSuccess** ao chamar a função **FIND**, embora avaliado como **#VALUE!**</span><span class="sxs-lookup"><span data-stu-id="bd103-139">For example, **Excel4** could return **xlretSuccess** when calling the function **FIND**, even though it evaluated to **#VALUE!**</span></span> <span data-ttu-id="bd103-140">porque não foi possível localizar o texto de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="bd103-140">because the search text could not be found.</span></span> <span data-ttu-id="bd103-141">Você deve inspecionar o tipo e o valor do **XLOPER/XLOPER12** em que esta é uma possibilidade.</span><span class="sxs-lookup"><span data-stu-id="bd103-141">You should inspect the type and value of the returned **XLOPER/XLOPER12** where this is a possibility.</span></span>  <br/> |
|<span data-ttu-id="bd103-142">1</span><span class="sxs-lookup"><span data-stu-id="bd103-142">-1</span></span>  <br/> |<span data-ttu-id="bd103-143">**xlretAbort**</span><span class="sxs-lookup"><span data-stu-id="bd103-143">**xlretAbort**</span></span> <br/> |<span data-ttu-id="bd103-144">Uma macro de comando foi interrompida pelo usuário clicando no botão**Cancelar** ou pressionando a tecla ESC.</span><span class="sxs-lookup"><span data-stu-id="bd103-144">A command macro was stopped by the user clicking the **CANCEL** button or pressing the ESC key.</span></span>  <br/> |
|<span data-ttu-id="bd103-145">2</span><span class="sxs-lookup"><span data-stu-id="bd103-145">-2</span></span>  <br/> |<span data-ttu-id="bd103-146">**xlretInvXlfn**</span><span class="sxs-lookup"><span data-stu-id="bd103-146">**xlretInvXlfn**</span></span> <br/> |<span data-ttu-id="bd103-147">A função fornecida ou código de comando não é válido.</span><span class="sxs-lookup"><span data-stu-id="bd103-147">The supplied function or command code is not valid.</span></span> <span data-ttu-id="bd103-148">Este erro pode ocorrer quando a função de chamadas não tem permissão para ligar para o comando ou função.</span><span class="sxs-lookup"><span data-stu-id="bd103-148">This error can occur when the calling function does not have permission to call the function or command.</span></span> <span data-ttu-id="bd103-149">Por exemplo, uma função de planilha não pode chamar uma função de informações de folha de macro ou uma função de comando.</span><span class="sxs-lookup"><span data-stu-id="bd103-149">For example, a worksheet function cannot call a macro sheet information function or a command function.</span></span>  <br/> |
|<span data-ttu-id="bd103-150">4</span><span class="sxs-lookup"><span data-stu-id="bd103-150">4\*</span></span>  <br/> |<span data-ttu-id="bd103-151">**xlretInvCount**</span><span class="sxs-lookup"><span data-stu-id="bd103-151">**xlretInvCount**</span></span> <br/> |<span data-ttu-id="bd103-152">O número de argumentos fornecido com a chamada não está correto.</span><span class="sxs-lookup"><span data-stu-id="bd103-152">The number of arguments supplied in the call is not correct.</span></span>  <br/> |
|<span data-ttu-id="bd103-153">8</span><span class="sxs-lookup"><span data-stu-id="bd103-153">8\*</span></span>  <br/> |<span data-ttu-id="bd103-154">**xlretInvXloper**</span><span class="sxs-lookup"><span data-stu-id="bd103-154">**xlretInvXloper**</span></span> <br/> |<span data-ttu-id="bd103-155">Um ou mais dos valores do argumento **XLOPER** ou **XLOPER12** não são adequadamente formados ou preenchidos.</span><span class="sxs-lookup"><span data-stu-id="bd103-155">One or more of the argument **XLOPER** or **XLOPER12** values are not properly formed or populated.</span></span>  <br/> |
|<span data-ttu-id="bd103-156">16</span><span class="sxs-lookup"><span data-stu-id="bd103-156">1.6</span></span>  <br/> |<span data-ttu-id="bd103-157">**xlretStackOvfl**</span><span class="sxs-lookup"><span data-stu-id="bd103-157">**xlretStackOvfl**</span></span> <br/> |<span data-ttu-id="bd103-158">O Excel detectou o risco de a operação poder exceder sua pilha e, portanto, não chamou a função.</span><span class="sxs-lookup"><span data-stu-id="bd103-158">Excel detected a risk that the operation might overflow its stack and, therefore, did not call the function.</span></span>  <br/> |
|<span data-ttu-id="bd103-159">32</span><span class="sxs-lookup"><span data-stu-id="bd103-159">32\*\*</span></span>  <br/> |<span data-ttu-id="bd103-160">**xlretFailed**</span><span class="sxs-lookup"><span data-stu-id="bd103-160">**xlretFailed**</span></span> <br/> |<span data-ttu-id="bd103-161">O comando ou função falhou por um motivo não descrito por um dos outros valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="bd103-161">The command or function failed for a reason not described by one of the other return values.</span></span> <span data-ttu-id="bd103-162">Uma operação que exigiria muita memória, por exemplo, falharia com esse erro.</span><span class="sxs-lookup"><span data-stu-id="bd103-162">An operation that would require too much memory, for example, would fail with this error.</span></span> <span data-ttu-id="bd103-163">Isso pode ocorrer durante a tentativa de converter uma vasta referência a uma matriz **xltypeMulti** matriz usando a função [xlCoerce](xlcoerce.md).</span><span class="sxs-lookup"><span data-stu-id="bd103-163">This could happen during an attempt to convert a very large reference to an **xltypeMulti** array by using the [xlCoerce](xlcoerce.md) function.</span></span>  <br/> |
|<span data-ttu-id="bd103-164">64</span><span class="sxs-lookup"><span data-stu-id="bd103-164">6.4</span></span>  <br/> |<span data-ttu-id="bd103-165">**xlretUncalced**</span><span class="sxs-lookup"><span data-stu-id="bd103-165">**xlretUncalced**</span></span> <br/> |<span data-ttu-id="bd103-166">A operação tentou recuperar o valor de uma célula não calculada.</span><span class="sxs-lookup"><span data-stu-id="bd103-166">The operation attempted to retrieve the value of an uncalculated cell.</span></span> <span data-ttu-id="bd103-167">Para preservar a integridade de recálculo no Excel, as funções de planilha não são autorizadas a fazer isso.</span><span class="sxs-lookup"><span data-stu-id="bd103-167">To preserve recalculation integrity in Excel, worksheet functions are not permitted to do this.</span></span> <span data-ttu-id="bd103-168">No entanto, os comandos e funções XLL registrados como funções de folha de macro têm permissão para acessar valores de célula não calculados.</span><span class="sxs-lookup"><span data-stu-id="bd103-168">However, XLL commands and functions registered as macro sheet functions are permitted to access uncalculated cell values.</span></span>  <br/> |
|<span data-ttu-id="bd103-169">128</span><span class="sxs-lookup"><span data-stu-id="bd103-169">128 bits</span></span>  <br/> |<span data-ttu-id="bd103-170">**xlretNotThreadSafe**</span><span class="sxs-lookup"><span data-stu-id="bd103-170">**xlretNotThreadSafe**</span></span> <br/> |<span data-ttu-id="bd103-171">(Começando no Excel 2007) Uma função de planilha XLL registrada como thread-safe tentou chamar uma função da API C que não é thread-safe.</span><span class="sxs-lookup"><span data-stu-id="bd103-171">(Starting in Excel 2007) An XLL worksheet function registered as thread safe attempted to call a C API function that is not thread safe.</span></span> <span data-ttu-id="bd103-172">Por exemplo, uma função de threads não pode chamar a função XLM **xlfGetCell**.</span><span class="sxs-lookup"><span data-stu-id="bd103-172">For example, a thread-safe function cannot call the XLM function **xlfGetCell**.</span></span>  <br/> |
|<span data-ttu-id="bd103-173">256</span><span class="sxs-lookup"><span data-stu-id="bd103-173">256
(&H100)</span></span>  <br/> |<span data-ttu-id="bd103-174">**xlRetInvAsynchronousContext**</span><span class="sxs-lookup"><span data-stu-id="bd103-174">**xlRetInvAsynchronousContext**</span></span> <br/> |<span data-ttu-id="bd103-175">(Começando no Excel 2010) O identificador de função assíncrona é inválido.</span><span class="sxs-lookup"><span data-stu-id="bd103-175">(Starting in Excel 2010) The asynchronous function handle is invalid.</span></span>  <br/> |
|<span data-ttu-id="bd103-176">512</span><span class="sxs-lookup"><span data-stu-id="bd103-176">5.12</span></span>  <br/> |<span data-ttu-id="bd103-177">**xlretNotClusterSafe**</span><span class="sxs-lookup"><span data-stu-id="bd103-177">**xlretNotClusterSafe**</span></span> <br/> |<span data-ttu-id="bd103-178">(Começando no Excel 2010) Não há suporte para a chamada em clusters.</span><span class="sxs-lookup"><span data-stu-id="bd103-178">(Starting in Excel 2010) The call is not supported on clusters.</span></span>  <br/> |
   
<span data-ttu-id="bd103-179">Se a função retorna um dos valores de falha na tabela (ou seja, ela não retorna **xlretSuccess**), o valor de retorno **XLOPER** ou **XLOPER12**  também será definido como **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="bd103-179">If the function returns one of the failure values in the table (that is, it does not return **xlretSuccess**), the **XLOPER** or **XLOPER12** return value will also be set to **#VALUE!**.</span></span> <span data-ttu-id="bd103-180">Em certas circunstâncias, verificar isso pode ser um teste de sucesso, mas você deve observar que uma chamada pode retornar **xlretSuccess** e **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="bd103-180">In certain circumstances, checking for this might be a sufficient test of success, but you should note that a call can return both **xlretSuccess** and **#VALUE!**.</span></span>
  
<span data-ttu-id="bd103-181">Se uma chamada de API C resulta em um **xlretUncalced** ou **xlretAbort**, o código DLL ou XLL deve retornar o controle para o Excel antes de fazer quaisquer outras chamadas de API C (diferente de chamadas para a função [xlfree ](xlfree.md) para liberar recursos de memória Excel alocados nos valores **XLOPER** e **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="bd103-181">If a call to the C API results in either **xlretUncalced** or **xlretAbort**, your DLL or XLL code should return control to Excel before making any other C API calls (other than calls to the [xlfree](xlfree.md) function to release Excel-allocated memory resources in **XLOPER** and **XLOPER12** values).</span></span> 
  
### <a name="command-or-function-enumeration-argument-xlfn"></a><span data-ttu-id="bd103-182">Argumento de Enumeração de Comando ou Função: xlfn</span><span class="sxs-lookup"><span data-stu-id="bd103-182">Command or Function Enumeration Argument: xlfn</span></span>

<span data-ttu-id="bd103-183">O argumento _xlfn_ é o primeiro argumento para as funções de retorno de chamada e é um inteiro assinado de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bd103-183">The  _xlfn_ argument is the first argument to the callback functions and is a 32-bit signed integer.</span></span> <span data-ttu-id="bd103-184">Seu valor deve ser uma das enumerações de função ou comando definidas no arquivo de cabeçalho do SDK Xlcall.h, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd103-184">Its value should be one of the function or command enumerations defined in the SDK header file Xlcall.h, as shown in the following example.</span></span> 
  
```cs
// Excel function numbers. 
#define xlfCount 0
#define xlfIsna 2
#define xlfIserror 3
#define xlfSum 4
#define xlfAverage 5
#define xlfMin 6
#define xlfMax 7
#define xlfRow 8
#define xlfColumn 9
#define xlfNa 10
...
// Excel command numbers. 
#define xlcBeep (0 | xlCommand)
#define xlcOpen (1 | xlCommand)
#define xlcOpenLinks (2 | xlCommand)
#define xlcCloseAll (3 | xlCommand)
#define xlcSave (4 | xlCommand)
#define xlcSaveAs (5 | xlCommand)
#define xlcFileDelete (6 | xlCommand)
#define xlcPageSetup (7 | xlCommand)
#define xlcPrint (8 | xlCommand)
#define xlcPrinterSetup (9 | xlCommand)
...
```

<span data-ttu-id="bd103-185">Todas as funções de planilha e folha de macro estão no intervalo de 0 (**xlfCount**) a 0x0fff hexadecimal, embora o maior número atribuído no Excel 2013 seja decimal 547, 0x0223 hexadecimal. (**xlfFloor_precise**).</span><span class="sxs-lookup"><span data-stu-id="bd103-185">All worksheet and macro sheet functions are in the range from 0 (**xlfCount**) through 0x0fff hexadecimal, although the highest assigned number in Excel 2013 is 547 decimal, 0x0223 hexadecimal (**xlfFloor_precise**).</span></span>
  
<span data-ttu-id="bd103-186">Todas as funções de comando estão no intervalo de 0x8000 hexadecimal (**xlcBeep**) em 0x8fff hexadecimal, embora o maior número atribuído no Excel 2013 é 0x8328 hexadecimal (**xlcHideallInkannots** ).</span><span class="sxs-lookup"><span data-stu-id="bd103-186">All command functions are in the range from 0x8000 hexadecimal (**xlcBeep**) through 0x8fff hexadecimal, although the highest assigned number in Excel 2013 is 0x8328 hexadecimal (**xlcHideallInkannots**).</span></span> <span data-ttu-id="bd103-187">Estes são definidos no arquivo de cabeçalho como `(n | xlCommand)` onde `n` é um número decimal maior ou igual a 0 e **xlCommand** é definido como 0x8000 hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="bd103-187">These are defined in the header file as  `(n | xlCommand)` where  `n` is a decimal number greater than or equal to 0 and **xlCommand** is defined as 0x8000 hexadecimal.</span></span> 
  
### <a name="invoking-excel-commands-that-use-dialog-boxes"></a><span data-ttu-id="bd103-188">Invocando comandos do Excel que usam caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="bd103-188">Invoking Excel Commands that Use Dialog Boxes</span></span>

<span data-ttu-id="bd103-189">Alguns códigos de comando correspondem à ações no Excel que usam caixas de diálogo.</span><span class="sxs-lookup"><span data-stu-id="bd103-189">Some of the command codes correspond to actions in Excel that use dialog boxes.</span></span> <span data-ttu-id="bd103-190">Por exemplo, **xlcFileDelete** tem um argumento único: um nome de arquivo ou máscara.</span><span class="sxs-lookup"><span data-stu-id="bd103-190">For example, **xlcFileDelete** takes a single argument: a file name or mask.</span></span> <span data-ttu-id="bd103-191">Isso pode ser chamado com a caixa de diálogo para que o usuário tenha a oportunidade de cancelar ou modificar a operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="bd103-191">This can be invoked with the dialog box so that the user has the opportunity to cancel or modify the delete operation.</span></span> <span data-ttu-id="bd103-192">Ele também pode ser chamado sem a caixa de diálogo, caso em que o arquivo ou arquivos são excluídos sem qualquer interação adicional, supondo que eles existam e o chamador tenha permissão.</span><span class="sxs-lookup"><span data-stu-id="bd103-192">It can also be called without the dialog box, in which case the file or files are deleted without any further interaction, assuming they exist and the caller has permission.</span></span> <span data-ttu-id="bd103-193">Para chamar esses comandos em sua forma de caixa de diálogo, a enumeração de comando deve ser combinada usando a operação OR bit a bit com 0x1000 (**xlPrompt**).</span><span class="sxs-lookup"><span data-stu-id="bd103-193">To call such commands in their dialog box form, the command enumeration must be combined by using the bitwise OR operation with 0x1000 (**xlPrompt**).</span></span>
  
<span data-ttu-id="bd103-194">O exemplo de código a seguir exclui arquivos no diretório atual que correspondem à máscara my_data\*.bak, exibindo uma caixa de diálogo apenas se o argumento for verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="bd103-194">The following code example deletes files in the current directory matching the mask my_data\*.bak, displaying a dialog box only if the argument is true.</span></span>
  
```cs
bool delete_my_backup_files(bool show_dialog)
{
    XLOPER12 xResult, xFilter;
    xFilter.xltype = xltypeStr;
    xFilter.val.str = L"\014my_data*.bak"; // String length: 14 octal
    int cmd;
    if(show_dialog)
        cmd = xlcFileDelete | xlPrompt;
    else
        cmd = xlcFileDelete;
// xResult should be Boolean TRUE if successful, in which
// case return true; otherwise, false.
    return (Excel12(cmd, &xResult, 1, &xFilter) == xlretSuccess
        && xResult.xltype == xltypeBool
        && xResult.val.xbool == 1);
}
```

### <a name="calling-functions-and-commands-in-international-versions"></a><span data-ttu-id="bd103-195">Funções de Chamada e Comandos em Versões Internacionais</span><span class="sxs-lookup"><span data-stu-id="bd103-195">Calling Functions and Commands in International Versions</span></span>

<span data-ttu-id="bd103-196">Você pode configurar o Excel para exibir os nomes dos comandos e funções XLM em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="bd103-196">You can configure Excel to display functions and XLM command names in a variety of languages.</span></span> <span data-ttu-id="bd103-197">Alguns comandos e funções da API C operam em cadeias de caracteres que são interpretadas como nomes de funções ou comandos.</span><span class="sxs-lookup"><span data-stu-id="bd103-197">Some C API commands and functions operate on strings that are interpreted as function or command names.</span></span> <span data-ttu-id="bd103-198">Por exemplo, **xlcFormula** tem um argumento de cadeia de caracteres que deve ser colocado em uma célula especificada.</span><span class="sxs-lookup"><span data-stu-id="bd103-198">For example, **xlcFormula** takes a string argument that is intended to be placed in a specified cell.</span></span> <span data-ttu-id="bd103-199">Para o suplemento trabalhar com todas as configurações de idioma, você pode fornecer os nomes de cadeia de inglês e definir bits 0x2000 (**xlIntl**) na função ou comando de enumeração.</span><span class="sxs-lookup"><span data-stu-id="bd103-199">For your add-in to work with all language settings, you can supply the English string names and set the bit 0x2000 (**xlIntl**) in the function or command enumeration.</span></span>
  
<span data-ttu-id="bd103-200">O exemplo a seguir coloca o equivalente a `=SUM(X1:X100)` na célula A2 da planilha ativa.</span><span class="sxs-lookup"><span data-stu-id="bd103-200">The following code example places the equivalent of  `=SUM(X1:X100)` in cell A2 on the active sheet.</span></span> <span data-ttu-id="bd103-201">Observe que a função de estrutura **TempActiveRef** é usada para criar uma referência externa temporária **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="bd103-201">Note that it uses the Framework function, **TempActiveRef**, to create a temporary external reference **XLOPER**.</span></span> <span data-ttu-id="bd103-202">A fórmula aparecerá em A2 no idioma determinado pelo código de idioma correto (por exemplo `=SOMME(X1:X100)`, se o idioma for francês).</span><span class="sxs-lookup"><span data-stu-id="bd103-202">The formula will appear in A2 in the correct locale-determined language (for example,  `=SOMME(X1:X100)` if the language is French).</span></span> 
  
```cs
int WINAPI InternationlExample(void)
{
    XLOPER12 xSum, xResult;
    xSum.xltype = xltypeStr;
    xSum.val.str = L"\015=SUM(X1:X100)";
    Excel12(xlcFormula | xlIntl, &xResult, 2,
        &xSum, TempActiveRef(2,2,1,1));
    return 1;
}

```

> [!NOTE]
> <span data-ttu-id="bd103-203">Como o resultado da chamada para o **Excel12** não é necessário, zero (NULL) pode ser passado como segundo argumento em vez do endereço de **xResult**.</span><span class="sxs-lookup"><span data-stu-id="bd103-203">Because the result of the call to **Excel12** is not required, zero (NULL) could be passed as the second argument instead of the address of **xResult**.</span></span> <span data-ttu-id="bd103-204">Isso é mais abordado na próxima seção.</span><span class="sxs-lookup"><span data-stu-id="bd103-204">This is discussed more in the next section.</span></span> 
  
### <a name="dll-only-functions-and-commands"></a><span data-ttu-id="bd103-205">Comandos e funções somente DLL</span><span class="sxs-lookup"><span data-stu-id="bd103-205">DLL-Only Functions and Commands</span></span>

<span data-ttu-id="bd103-206">O Excel suporta um pequeno número de funções que só podem ser acessadas por uma DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="bd103-206">Excel supports a small number of functions that are only accessible from a DLL or XLL.</span></span> <span data-ttu-id="bd103-207">Estes são definidos no arquivo como cabeçalho `(n | xlSpecial)` onde `n` é um número decimal maior ou igual a 0 e `xlSpecial` é definido como 0x4000 hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="bd103-207">These are defined in the header file as  `(n | xlSpecial)` where  `n` is a decimal number greater than or equal to 0 and  `xlSpecial` is defined as 0x4000 hexadecimal.</span></span> <span data-ttu-id="bd103-208">Essas funções estão listadas na tabela a seguir e documentadas em [referência da API de função](excel-xll-sdk-api-function-reference.md).</span><span class="sxs-lookup"><span data-stu-id="bd103-208">These functions are listed in the following table and documented in the [API Function Reference](excel-xll-sdk-api-function-reference.md).</span></span>
  
||||
|:-----|:-----|:-----|
|[<span data-ttu-id="bd103-209">xlFree</span><span class="sxs-lookup"><span data-stu-id="bd103-209">xlFree</span></span>](xlfree.md) <br/> |<span data-ttu-id="bd103-210">0</span><span class="sxs-lookup"><span data-stu-id="bd103-210">(0)</span></span> | <span data-ttu-id="bd103-211">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-211">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-212">Libera recursos de memória alocados no Excel.</span><span class="sxs-lookup"><span data-stu-id="bd103-212">Frees Excel-allocated memory resources.</span></span>  <br/> |
|[<span data-ttu-id="bd103-213">xlStack</span><span class="sxs-lookup"><span data-stu-id="bd103-213">xlStack</span></span>](xlstack.md) <br/> |<span data-ttu-id="bd103-214">1</span><span class="sxs-lookup"><span data-stu-id="bd103-214">-1</span></span> | <span data-ttu-id="bd103-215">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-215">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-216">Retorna o espaço livre na pilha do Excel.</span><span class="sxs-lookup"><span data-stu-id="bd103-216">Returns the free space on the Excel stack.</span></span>  <br/> |
|[<span data-ttu-id="bd103-217">xlCoerce</span><span class="sxs-lookup"><span data-stu-id="bd103-217">xlCoerce</span></span>](xlcoerce.md) <br/> |<span data-ttu-id="bd103-218">2</span><span class="sxs-lookup"><span data-stu-id="bd103-218">-2</span></span> | <span data-ttu-id="bd103-219">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-219">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-220">Converte entre os tipos **XLOPER** e **XLOPER12**</span><span class="sxs-lookup"><span data-stu-id="bd103-220">Converts between **XLOPER** and **XLOPER12** types</span></span>  <br/> |
|[<span data-ttu-id="bd103-221">xlSet</span><span class="sxs-lookup"><span data-stu-id="bd103-221">xlSet</span></span>](xlset.md) <br/> |<span data-ttu-id="bd103-222">3</span><span class="sxs-lookup"><span data-stu-id="bd103-222">-3</span></span> | <span data-ttu-id="bd103-223">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-223">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-224">Fornece um método rápido para definir valores de células.</span><span class="sxs-lookup"><span data-stu-id="bd103-224">Provides a fast method of setting cell values.</span></span>  <br/> |
|[<span data-ttu-id="bd103-225">xlSheetId</span><span class="sxs-lookup"><span data-stu-id="bd103-225">xlSheetId</span></span>](xlsheetid.md) <br/> |<span data-ttu-id="bd103-226">4</span><span class="sxs-lookup"><span data-stu-id="bd103-226">4\*</span></span> | <span data-ttu-id="bd103-227">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-227">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-228">Obtém um nome de planilha a partir do ID interno.</span><span class="sxs-lookup"><span data-stu-id="bd103-228">Obtains a worksheet name from its internal ID.</span></span>  <br/> |
|[<span data-ttu-id="bd103-229">xlSheetNm</span><span class="sxs-lookup"><span data-stu-id="bd103-229">xlSheetNm</span></span>](xlsheetnm.md) <br/> |<span data-ttu-id="bd103-230">5</span><span class="sxs-lookup"><span data-stu-id="bd103-230">$-5</span></span> | <span data-ttu-id="bd103-231">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-231">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-232">Obtém um ID interno da planilha de seu nome..</span><span class="sxs-lookup"><span data-stu-id="bd103-232">Obtains a worksheet internal ID from its name.</span></span>  <br/> |
|[<span data-ttu-id="bd103-233">xlAbort</span><span class="sxs-lookup"><span data-stu-id="bd103-233">xlAbort</span></span>](xlabort.md) <br/> |<span data-ttu-id="bd103-234">6</span><span class="sxs-lookup"><span data-stu-id="bd103-234">-6</span></span> | <span data-ttu-id="bd103-235">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-235">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-236">Verifica se o usuário clica no botão **Cancelar** ou pressiona a tecla ESC.</span><span class="sxs-lookup"><span data-stu-id="bd103-236">Verifies whether the user clicked the **CANCEL** button or pressed the ESC key.</span></span>  <br/> |
|[<span data-ttu-id="bd103-237">xlGetInst</span><span class="sxs-lookup"><span data-stu-id="bd103-237">xlGetInst</span></span>](xlgetinst.md) <br/> |<span data-ttu-id="bd103-238">7</span><span class="sxs-lookup"><span data-stu-id="bd103-238">-7</span></span> | <span data-ttu-id="bd103-239">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-239">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-240">Obtém a alça de instância do Excel.</span><span class="sxs-lookup"><span data-stu-id="bd103-240">Gets the Excel instance handle.</span></span>  <br/> |
|[<span data-ttu-id="bd103-241">xlGetHwnd</span><span class="sxs-lookup"><span data-stu-id="bd103-241">xlGetHwnd</span></span>](xlgethwnd.md) <br/> |<span data-ttu-id="bd103-242">8</span><span class="sxs-lookup"><span data-stu-id="bd103-242">8\*</span></span> | <span data-ttu-id="bd103-243">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-243">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-244">Obtém o identificador de janela principal do Excel.</span><span class="sxs-lookup"><span data-stu-id="bd103-244">Gets the Excel main window handle.</span></span>  <br/> |
|[<span data-ttu-id="bd103-245">xlGetName</span><span class="sxs-lookup"><span data-stu-id="bd103-245">xlGetName</span></span>](xlgetname.md) <br/> |<span data-ttu-id="bd103-246">9</span><span class="sxs-lookup"><span data-stu-id="bd103-246">-9</span></span> | <span data-ttu-id="bd103-247">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-247">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-248">Obtém o caminho e o nome de arquivo da DLL.</span><span class="sxs-lookup"><span data-stu-id="bd103-248">Gets the path and file name of the Visual Report template. Read-only String .</span></span>  <br/> |
|[<span data-ttu-id="bd103-249">xlEnableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="bd103-249">xlEnableXLMsgs</span></span>](xlenablexlmsgs.md) <br/> |<span data-ttu-id="bd103-250">10</span><span class="sxs-lookup"><span data-stu-id="bd103-250">1.0</span></span> | <span data-ttu-id="bd103-251">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-251">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-252">Esta função é substituída e não precisa mais ser chamada.</span><span class="sxs-lookup"><span data-stu-id="bd103-252">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="bd103-253">xlDisableXLMsgs</span><span class="sxs-lookup"><span data-stu-id="bd103-253">xlDisableXLMsgs</span></span>](xldisablexlmsgs.md) <br/> |<span data-ttu-id="bd103-254">11</span><span class="sxs-lookup"><span data-stu-id="bd103-254">1.1</span></span> | <span data-ttu-id="bd103-255">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-255">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-256">Esta função é substituída e não precisa mais ser chamada.</span><span class="sxs-lookup"><span data-stu-id="bd103-256">This function is deprecated and no longer needs to be called.</span></span>  <br/> |
|[<span data-ttu-id="bd103-257">xlDefineBinaryName</span><span class="sxs-lookup"><span data-stu-id="bd103-257">xlDefineBinaryName</span></span>](xldefinebinaryname.md) <br/> |<span data-ttu-id="bd103-258">12</span><span class="sxs-lookup"><span data-stu-id="bd103-258">1.2</span></span> | <span data-ttu-id="bd103-259">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-259">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-260">Define um nome de armazenamento binário persistente.</span><span class="sxs-lookup"><span data-stu-id="bd103-260">Defines a persistent binary storage name.</span></span>  <br/> |
|[<span data-ttu-id="bd103-261">xlGetBinaryName</span><span class="sxs-lookup"><span data-stu-id="bd103-261">xlGetBinaryName</span></span>](xlgetbinaryname.md) <br/> |<span data-ttu-id="bd103-262">13</span><span class="sxs-lookup"><span data-stu-id="bd103-262">1.3</span></span> | <span data-ttu-id="bd103-263">xlSpecial</span><span class="sxs-lookup"><span data-stu-id="bd103-263">xlSpecial</span></span>  <br/> |<span data-ttu-id="bd103-264">Obtém os dados de um nome de armazenamento binário persistente.</span><span class="sxs-lookup"><span data-stu-id="bd103-264">Gets a persistent binary storage name's data.</span></span>  <br/> |
   
## <a name="return-value-xloperxloper12-operres"></a><span data-ttu-id="bd103-265">Retorna o valor oper/XLOPER12: operRes</span><span class="sxs-lookup"><span data-stu-id="bd103-265">Return value XLOPER/XLOPER12: operRes</span></span>

<span data-ttu-id="bd103-266">O argumento _operRes_ é o segundo argumento para os retornos de chamada e é um ponteiro para uma **XLOPER** (**Excel4** e **Excel4v**) ou\*\* XLOPER12\*\* (**Excel12** e **Excel12v**).</span><span class="sxs-lookup"><span data-stu-id="bd103-266">The  _operRes_ argument is the second argument to the callbacks and is a pointer to an **XLOPER** (**Excel4** and **Excel4v**) or **XLOPER12** (**Excel12** and **Excel12v**).</span></span> <span data-ttu-id="bd103-267">Após uma chamada bem-sucedida, ele contém o valor de retorno da função ou comando.</span><span class="sxs-lookup"><span data-stu-id="bd103-267">After a successful call, it contains the return value of the function or command.</span></span> <span data-ttu-id="bd103-268">**operRes** pode ser definida como zero (ponteiro nulo) se o valor de retorno for necessário.</span><span class="sxs-lookup"><span data-stu-id="bd103-268">**operRes** can be set to zero (NULL pointer) if no return value is required.</span></span> <span data-ttu-id="bd103-269">O conteúdo anterior de **operRes** é sobrescrito para que qualquer memória anteriormente apontada seja liberada antes da chamada para evitar vazamentos de memória.</span><span class="sxs-lookup"><span data-stu-id="bd103-269">The previous contents of **operRes** are overwritten so that any memory previously pointed to must be freed before to the call to avoid memory leaks.</span></span> 
  
<span data-ttu-id="bd103-270">Se o comando ou a função não pode ser chamado (por exemplo, se os argumentos estão incorretos), **operRes** está definido para o erro **#VALUE!**.</span><span class="sxs-lookup"><span data-stu-id="bd103-270">If the function or command cannot be called (for example, if the arguments are incorrect), **operRes** is set to the error **#VALUE!**.</span></span> <span data-ttu-id="bd103-271">Um comando sempre retorna **Booleano** **TRUE** se for bem-sucedido, ou **FALSE** se tiver falhado ou for cancelado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="bd103-271">A command always returns **Boolean** **TRUE** if it is successful, or **FALSE** if it failed or the user canceled it.</span></span> 
  
## <a name="number-of-subsequent-arguments-count"></a><span data-ttu-id="bd103-272">Número de argumentos subsequentes: contagem</span><span class="sxs-lookup"><span data-stu-id="bd103-272">Number of Subsequent Arguments: count</span></span>

<span data-ttu-id="bd103-273">O argumento _contagem_ é o terceiro argumento para o retorno de chamada e é um inteiro assinado de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="bd103-273">The  _count_ argument is the third argument to the callbacks and is a 32-bit signed integer.</span></span> <span data-ttu-id="bd103-274">Deve ser definido para o número de argumentos subsequentes, contando a partir de 1.</span><span class="sxs-lookup"><span data-stu-id="bd103-274">It should be set to the number of subsequent arguments, counting from 1.</span></span> <span data-ttu-id="bd103-275">Se uma função ou comando não tiver argumentos, ele deverá ser definido como zero.</span><span class="sxs-lookup"><span data-stu-id="bd103-275">If a function or command takes no arguments, it should be set to zero.</span></span> <span data-ttu-id="bd103-276">No Microsoft Office Excel 2003, o número máximo de argumentos que qualquer função pode levar é 30, embora a maioria leve menos do que isso.</span><span class="sxs-lookup"><span data-stu-id="bd103-276">In Microsoft Office Excel 2003, the maximum number of arguments that any function can take is 30, although most take fewer than this.</span></span> <span data-ttu-id="bd103-277">A partir do Excel 2007, o número máximo de argumentos que qualquer função pode levar aumentou para 255.</span><span class="sxs-lookup"><span data-stu-id="bd103-277">Starting in Excel 2007, the maximum number of arguments that any function can take was increased to 255.</span></span> 
  
<span data-ttu-id="bd103-278">Com **Excel4** e **Excel12**, _contagem_ é o número de sugestões para valores **XLOPER** ou **XLOPER12** que estão sendo passados.</span><span class="sxs-lookup"><span data-stu-id="bd103-278">With **Excel4** and **Excel12**,  _count_ is the number of pointers to **XLOPER** or **XLOPER12** values that are being passed.</span></span> <span data-ttu-id="bd103-279">Você deve ter muito cuidado para não transmitir menos argumentos do que o valor para o qual a _contagem_ está configurada.</span><span class="sxs-lookup"><span data-stu-id="bd103-279">You should be very careful not to pass fewer arguments than the value that  _count_ is set to.</span></span> <span data-ttu-id="bd103-280">Isso resultaria na leitura do Excel adiante na pilha e na tentativa de processar valores **XLOPER** ou **XLOPER12** inválidos, o que poderia causar uma falha no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="bd103-280">This would result in Excel reading ahead into the stack and trying to process invalid **XLOPER** or **XLOPER12** values, which could cause an application crash.</span></span> 
  
<span data-ttu-id="bd103-281">Com **Excel4v** e **Excel12v**, _contagem_ é o tamanho da matriz dos ponteiros para os valores **XLOPER** ou **XLOPER12**que está sendo passado como o próximo e último argumento.</span><span class="sxs-lookup"><span data-stu-id="bd103-281">With **Excel4v** and **Excel12v**,  _count_ is the size of the array of pointers to **XLOPER** or **XLOPER12** values that is being passed as the next and final argument.</span></span> <span data-ttu-id="bd103-282">Novamente, você deve ter muito cuidado para não transmitir uma matriz menor do que o elemento _contagem_ em tamanho, pois isso fará com que os limites da matriz sejam excedidos.</span><span class="sxs-lookup"><span data-stu-id="bd103-282">Again, you should be very careful not to pass a smaller array than  _count_ elements in size, as this will result in the bounds of the array being overrun.</span></span> 
  
## <a name="passing-arguments-to-c-api-functions"></a><span data-ttu-id="bd103-283">Passando Argumentos para Funções da API C</span><span class="sxs-lookup"><span data-stu-id="bd103-283">Passing Arguments to C API Functions</span></span>

<span data-ttu-id="bd103-284">O **Excel4** e o **Excel12** usam listas de argumentos de tamanho variável, após _contagem_, que são interpretadas como ponteiros para os valores **XLOPER** e **XLOPER12**, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="bd103-284">Both **Excel4** and **Excel12** take variable length argument lists, after  _count_, which are interpreted as pointers to **XLOPER** and **XLOPER12** values, respectively.</span></span> <span data-ttu-id="bd103-285">**Excel4v** e **Excel12v** fazer um argumento único, após _contagem_, que é um ponteiro para uma matriz de ponteiros para valores **XLOPER** no caso do**Excel4v**e valores**XLOPER12** no caso do **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="bd103-285">**Excel4v** and **Excel12v** take a single argument, after  _count_, which is a pointer to an array of pointers to **XLOPER** values in the case of **Excel4v**, and to **XLOPER12** values in the case of **Excel12v**.</span></span>
  
<span data-ttu-id="bd103-286">Os formulários de matriz **Excel4v** e **Excel12v**, 
permite que você codifique uma chamada para a API C de forma limpa quando o número de argumentos for variável.</span><span class="sxs-lookup"><span data-stu-id="bd103-286">The array forms, **Excel4v** and **Excel12v**, enable you to code a call to the C API cleanly when the number of arguments is variable.</span></span> <span data-ttu-id="bd103-287">O exemplo a seguir mostra uma função que usa uma matriz de números de tamanho variável e usa funções de planilha do Excel, por meio da API C, para calcular a soma, a média, o mínimo e o máximo.</span><span class="sxs-lookup"><span data-stu-id="bd103-287">The following example shows a function that takes a variable-sized array of numbers and uses Excel worksheet functions, via the C API, to calculate the sum, average, minimum, and maximum.</span></span> 
  
```cs
void Excel12v_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// 30 is the limit in Excel 2003. 255 is the limit in Excel 2007.
// Use the lower limit to be safe, although it is better to make
// the function version-aware and use the correct limit.
    if(size < 1 || size > 30)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create an array of pointers to XLOPER12 values.
    LPXLOPER12 *xPtrArray =
        (LPXLOPER12 *)malloc(size * sizeof(LPXLOPER12));
// Initialize and populate the array of XLOPER12 values
// and set up the pointers in the pointer array.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
        xPtrArray[i] = xOpArray + i;
    }
    XLOPER12 xResult;
    int retval;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        retval = Excel12v(fn[i], &xResult, size, xPtrArray);
        if(retval == xlretSuccess && xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xPtrArray);
    free(xOpArray);
}

```

<span data-ttu-id="bd103-288">Substituindo referências a valores **XLOPER12** com  **XLOPER**, e **Excel12v** com **Excel4v**, no código anterior resultaria em um função que funcionaria com todas as versões do Excel.</span><span class="sxs-lookup"><span data-stu-id="bd103-288">Replacing references to **XLOPER12** values with **XLOPER**, and **Excel12v** with **Excel4v**, in the preceding code would result in a function that would work with all versions of Excel.</span></span> <span data-ttu-id="bd103-289">Essa operação das funções do Excel **SUM**, **AVERAGE**, **MIN** e **MAX** é tão simples que seria mais eficiente codificá-las em C e evitar a sobrecarga ao preparar os argumentos e chamar o Excel.</span><span class="sxs-lookup"><span data-stu-id="bd103-289">This operation of the Excel functions **SUM**, **AVERAGE**, **MIN**, and **MAX** is simple enough that it would be more efficient to code them in C and avoid the overhead of preparing the arguments and calling into Excel.</span></span> <span data-ttu-id="bd103-290">No entanto, muitas das funções que o Excel contém são mais complexas, tornando essa abordagem útil em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="bd103-290">However, many of the functions Excel contains are more complex, making this approach useful in some cases.</span></span> 
  
<span data-ttu-id="bd103-291">O tópico [xlfRegister](xlfregister-form-1.md) fornece outro exemplo de trabalho com **Excel4v** e **Excel12v**.</span><span class="sxs-lookup"><span data-stu-id="bd103-291">The [xlfRegister](xlfregister-form-1.md) topic provides another example of working with **Excel4v** and **Excel12v**.</span></span> <span data-ttu-id="bd103-292">Ao registrar uma função de planilha XLL, você pode fornecer uma cadeia de caracteres descritiva para cada argumento que é usado na caixa de diálogo **Colar função**.</span><span class="sxs-lookup"><span data-stu-id="bd103-292">When registering an XLL worksheet function, you can supply a descriptive string for each argument that is used in the **Paste Function** dialog box.</span></span> <span data-ttu-id="bd103-293">Portanto, o número total de argumentos fornecidos para o **xlfRegister** depende do número de argumentos que sua função XLL usa e varia de uma função para outra.</span><span class="sxs-lookup"><span data-stu-id="bd103-293">Therefore, the number of total arguments being supplied to **xlfRegister** depends on the number of arguments your XLL function takes and will vary from one function to the next.</span></span> 
  
<span data-ttu-id="bd103-294">Onde você sempre chama uma função ou um comando da API C com o mesmo número de argumentos, você deseja evitar a etapa extra de criar uma matriz de ponteiros para esses argumentos.</span><span class="sxs-lookup"><span data-stu-id="bd103-294">Where you always call a C API function or command with the same number of arguments, you want to avoid the extra step of creating an array of pointers for those arguments.</span></span> <span data-ttu-id="bd103-295">Nesses casos, é mais simples e mais limpo usar **Excel4** e **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="bd103-295">In those cases, it is simpler and cleaner to use **Excel4** and **Excel12**.</span></span> <span data-ttu-id="bd103-296">Por exemplo, ao registrar funções e comandos XLL, você precisa fornecer o caminho completo e o nome do arquivo da DLL ou XLL.</span><span class="sxs-lookup"><span data-stu-id="bd103-296">For example, when registering XLL functions and commands, you need to supply the full path and file name of the DLL or XLL.</span></span> <span data-ttu-id="bd103-297">Você pode obter o nome do arquivo em uma chamada de **xlfGetName** e, em seguida, soltar com uma chamada ao **xlFree**, conforme mostrado no exemplo a seguir para o **Excel4** e \*\* Excel12\*\*.</span><span class="sxs-lookup"><span data-stu-id="bd103-297">You can obtain the file name in a call to **xlfGetName** and then release it with a call to **xlFree**, as shown in the following example for both **Excel4** and **Excel12**.</span></span>
  
```cs
XLOPER xDllName;
if(Excel4(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and 
    // then free the memory that Excel allocated for the string.
    Excel4(xlFree, 0, 1, &xDllName);
}
XLOPER12 xDllName;
if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
{
    // Use the name, and
    // then free the memory that Excel allocated for the string.
    Excel12(xlFree, 0, 1, &xDllName);
}

```

<span data-ttu-id="bd103-298">Na prática, a função **Excel12v_example**, pode ser classificada com mais eficiência, criando um único argumento**xltypeMulti** **XLOPER12** e chamando a API C usando **Excel12**, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="bd103-298">In practice, the function, **Excel12v_example**, could be coded more efficiently by creating a single **xltypeMulti** **XLOPER12** argument, and calling the C API by using **Excel12**, as shown in the following example.</span></span>
  
```cs
void Excel12_example(double *dbl_array, int size, double &sum, double &average, double &min, double &max)
{
// In this implementation, the upper limit is the largest
// single column array (equals 2^20, or 1048576, rows in Excel 2007).
    if(size < 1 || size > 1048576)
        return;
// Create an array of XLOPER12 values.
    XLOPER12 *xOpArray = (XLOPER12 *)malloc(size * sizeof(XLOPER12));
// Create and initialize an xltypeMulti array
// that represents a one-column array.
    XLOPER12 xOpMulti;
    xOpMulti.xltype = xltypeMulti;
    xOpMulti.val.array.lparray = xOpArray;
    xOpMulti.val.array.columns = 1;
    xOpMulti.val.array.rows = size;
// Initialize and populate the array of XLOPER12 values.
    for(int i = 0; i < size; i++)
    {
        xOpArray[i].xltype = xltypeNum;
        xOpArray[i].val.num = dbl_array[i];
    }
    XLOPER12 xResult;
    int fn[4] = {xlfSum, xlfAverage, xlfMin, xlfMax};
    double *result_ptr[4] = {&sum, &average, &min, &max};
    for(i = 0; i < 4; i++)
    {
        Excel12(fn[i], &xResult, 1, &xOpMulti);
        if(xResult.xltype == xltypeNum)
            *result_ptr[i] = xResult.val.num;
    }
    free(xOpArray);
}

```

> [!NOTE]
> <span data-ttu-id="bd103-299">Nesse caso, o valor de retorno **Excel12** será ignorado.</span><span class="sxs-lookup"><span data-stu-id="bd103-299">In this case, the return value of **Excel12** is ignored.</span></span> <span data-ttu-id="bd103-300">Em vez disso, o código verifica que o**XLOPER12** fornecido é **xltypeNum** para determinar se a chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bd103-300">The code instead checks that the returned **XLOPER12** is **xltypeNum** to determine whether the call was successful.</span></span> 
  
## <a name="xlcallver"></a><span data-ttu-id="bd103-301">XLCallVer</span><span class="sxs-lookup"><span data-stu-id="bd103-301">XLCallVer</span></span>

<span data-ttu-id="bd103-302">Além dos retornos de chamada **Excel4**, **Excel4v**, **Excel12**, e **Excel12v**, o Excel exporta uma função \*\* XLCallVer\*\*, que retorna a versão da API C em execução.</span><span class="sxs-lookup"><span data-stu-id="bd103-302">In addition to the callbacks **Excel4**, **Excel4v**, **Excel12**, and **Excel12v**, Excel exports a function **XLCallVer**, which returns the version of the C API currently running.</span></span>
  
<span data-ttu-id="bd103-303">O protótipo da função é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="bd103-303">The function prototype is as follows:</span></span>
  
 `int pascal XLCallVer(void);`
  
<span data-ttu-id="bd103-304">Você pode chamar essa função, que é thread-safe, de qualquer comando ou função XLL.</span><span class="sxs-lookup"><span data-stu-id="bd103-304">You can call this function, which is thread safe, from any XLL command or function.</span></span>
  
<span data-ttu-id="bd103-305">Do Excel 97 até o Excel 2003, **XLCallVer** retorna 0x0500 = 1280 hex = 5 x 256, que indica o Excel versão 5.</span><span class="sxs-lookup"><span data-stu-id="bd103-305">In Excel 97 through Excel 2003, **XLCallVer** returns 1280 = 0x0500 hex = 5 x 256, which indicates Excel version 5.</span></span> <span data-ttu-id="bd103-306">A partir do Excel 2007, ela retorna 3072 = 0x0c00 hex = 12 x 256, que indica a versão 12 da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="bd103-306">Starting in Excel 2007, it returns 3072 = 0x0c00 hex = 12 x 256, which similarly indicates version 12.</span></span>
  
<span data-ttu-id="bd103-307">Embora você possa usar isso para determinar se a nova API de C está disponível em tempo de execução, talvez você prefira detectar a versão do Excel em execução usando `Excel4(xlfGetWorkspace, &version, 1, &arg)`, no qual `arg` é um numérico **XLOPER** definido para 2.</span><span class="sxs-lookup"><span data-stu-id="bd103-307">Although you can use this to determine whether the new C API is available at run time, you might prefer to detect the running version of Excel by using  `Excel4(xlfGetWorkspace, &version, 1, &arg)`, where  `arg` is a numeric **XLOPER** set to 2.</span></span> <span data-ttu-id="bd103-308">A função retorna uma cadeia de caracteres **XLOPER**, versão, que pode ser forçada a um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="bd103-308">The function returns a string **XLOPER**, version, which can then be coerced to an integer.</span></span> <span data-ttu-id="bd103-309">O motivo para confiar na versão do Excel em vez da versão da API C é que existem diferenças entre o Excel 2000, o Excel 2002 e o Excel 2003 que o seu suplemento também pode precisar detectar.</span><span class="sxs-lookup"><span data-stu-id="bd103-309">The reason for relying on the Excel version rather than the C API version is that there are differences between Excel 2000, Excel 2002, and Excel 2003 that your add-in may also need to detect.</span></span> <span data-ttu-id="bd103-310">Por exemplo, foram feitas alterações na precisão de algumas das funções estatísticas.</span><span class="sxs-lookup"><span data-stu-id="bd103-310">For example, changes were made to the accuracy of some of the statistics functions.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bd103-311">Confira também</span><span class="sxs-lookup"><span data-stu-id="bd103-311">See also</span></span>

- [<span data-ttu-id="bd103-312">Criar XLLs</span><span class="sxs-lookup"><span data-stu-id="bd103-312">Creating XLLs</span></span>](creating-xlls.md)  
- [<span data-ttu-id="bd103-313">Acessar o código de XLL no Excel</span><span class="sxs-lookup"><span data-stu-id="bd103-313">Accessing XLL code in Excel</span></span>](accessing-xll-code-in-excel.md)  
- [<span data-ttu-id="bd103-314">Excel XLL SDK API Function Reference</span><span class="sxs-lookup"><span data-stu-id="bd103-314">Excel XLL SDK API Function Reference</span></span>](excel-xll-sdk-api-function-reference.md)  
- [<span data-ttu-id="bd103-315">Retorno de chamada da API de C: funções Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="bd103-315">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md)  
- [<span data-ttu-id="bd103-316">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="bd103-316">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

