---
title: Desenvolver DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLLs [excel 2007], criação, criar DLLs [Excel 2007]
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 89dd7b65ad94ba2fc7e1cf3f99ee163d3003d0fe
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704746"
---
# <a name="developing-dlls"></a><span data-ttu-id="f6598-104">Desenvolver DLLs</span><span class="sxs-lookup"><span data-stu-id="f6598-104">Developing DLLs</span></span>

<span data-ttu-id="f6598-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f6598-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f6598-106">Uma biblioteca é de uma base de códigos compilados que fornece algumas funcionalidades e dados para um aplicativo executável.</span><span class="sxs-lookup"><span data-stu-id="f6598-106">A library is a body of compiled code that provides some functionality and data to an executable application.</span></span> <span data-ttu-id="f6598-107">As bibliotecas podem ser vinculadas estaticamente ou vinculadas dinamicamente e, convencionalmente, têm extensões de nome de arquivo .lib e .dll, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f6598-107">Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively.</span></span> <span data-ttu-id="f6598-108">Bibliotecas estáticas (como a biblioteca de tempo de execução C) são vinculadas ao aplicativo na compilação e, portanto, tornam-se parte da resultante executável.</span><span class="sxs-lookup"><span data-stu-id="f6598-108">Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable.</span></span> <span data-ttu-id="f6598-109">O aplicativo carrega uma DLL quando necessário, normalmente quando o aplicativo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="f6598-109">The application loads a DLL when it is needed, usually when the application starts up.</span></span> <span data-ttu-id="f6598-110">Um DLL pode carregar e vincular dinamicamente a DLL do outro.</span><span class="sxs-lookup"><span data-stu-id="f6598-110">One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="f6598-111">Benefícios do uso de DLLs</span><span class="sxs-lookup"><span data-stu-id="f6598-111">Benefits of using MDS</span></span>

<span data-ttu-id="f6598-112">Os principais benefícios de DLLs são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="f6598-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="f6598-113">Todos os aplicativos podem compartilhar uma única cópia no disco.</span><span class="sxs-lookup"><span data-stu-id="f6598-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="f6598-114">Os arquivos executáveis dos aplicativos são menores.</span><span class="sxs-lookup"><span data-stu-id="f6598-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="f6598-115">Eles permitem que grandes projetos de desenvolvimento sejam desmembrados.</span><span class="sxs-lookup"><span data-stu-id="f6598-115">They enable large development projects to be broken down.</span></span> <span data-ttu-id="f6598-116">Desenvolvedores de aplicativo e DLL só precisam concordar uma interface entre suas respectivas partes.</span><span class="sxs-lookup"><span data-stu-id="f6598-116">Application and DLL developers only need agree an interface between their respective parts.</span></span> <span data-ttu-id="f6598-117">Essa interface é exportada pela DLL.</span><span class="sxs-lookup"><span data-stu-id="f6598-117">This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="f6598-118">Os desenvolvedores de DLL podem atualizar as DLLs, talvez para torná-las mais eficientes ou para corrigir um bug, sem precisar atualizar todos os aplicativos que as utilizam, desde que a interface exportada da DLL não seja alterada.</span><span class="sxs-lookup"><span data-stu-id="f6598-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="f6598-119">Você pode usar DLLs para adicionar comandos e funções de planilha no Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="f6598-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="f6598-120">Recursos para a criação de DLLs</span><span class="sxs-lookup"><span data-stu-id="f6598-120">Resources for creating DLLs</span></span>

<span data-ttu-id="f6598-121">Para criar uma DLL, você precisa de:</span><span class="sxs-lookup"><span data-stu-id="f6598-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="f6598-122">Um editor de código-fonte.</span><span class="sxs-lookup"><span data-stu-id="f6598-122">A source code editor.</span></span>
    
- <span data-ttu-id="f6598-123">Compilador para ativar o código-fonte do código de objeto que seja compatível com o seu hardware.</span><span class="sxs-lookup"><span data-stu-id="f6598-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="f6598-124">Vinculador para adicionar o código de bibliotecas estáticas, quando usado e para criar o arquivo executável DLL.</span><span class="sxs-lookup"><span data-stu-id="f6598-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="f6598-125">Ambientes de desenvolvimento integrados modernos (IDEs), como o Microsoft Visual Studio, fornecem todas essas coisas.</span><span class="sxs-lookup"><span data-stu-id="f6598-125">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things.</span></span> <span data-ttu-id="f6598-126">Eles também fornecem muito mais: editores inteligentes, ferramentas para depurar seu código, ferramentas para gerenciar vários projetos, novos assistentes de projeto e muitas outras ferramentas importantes.</span><span class="sxs-lookup"><span data-stu-id="f6598-126">They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="f6598-127">Você pode criar DLLs em vários idiomas, por exemplo, C++ Pascal e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6598-127">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic.</span></span> <span data-ttu-id="f6598-128">Dado que o código-fonte da API fornecido com o Excel é C e C ++, somente esses dois idiomas são considerados nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="f6598-128">Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="f6598-129">Exportar comandos e funções</span><span class="sxs-lookup"><span data-stu-id="f6598-129">Exporting functions and commands</span></span>

<span data-ttu-id="f6598-130">Ao compilar um projeto DLL, o compilador e o vinculador precisam saber quais funções devem ser exportadas para que possam disponibilizá-las para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f6598-130">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application.</span></span> <span data-ttu-id="f6598-131">Esta seção descreve as maneiras de fazer isso.</span><span class="sxs-lookup"><span data-stu-id="f6598-131">This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="f6598-132">Quando compiladores compilam o código-fonte, em geral, eles alteram os nomes das funções de sua aparência no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="f6598-132">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code.</span></span> <span data-ttu-id="f6598-133">Eles geralmente fazem isso adicionando o início e/ou final do nome de um processo denominado nome decoração.</span><span class="sxs-lookup"><span data-stu-id="f6598-133">They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration.</span></span> <span data-ttu-id="f6598-134">Você precisa garantir que a função é exportada com um nome reconhecível para o aplicativo ao carregar a DLL.</span><span class="sxs-lookup"><span data-stu-id="f6598-134">You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL.</span></span> <span data-ttu-id="f6598-135">Isso pode significar informar ao vinculador para associar o nome decorado com um nome de exportação mais simples.</span><span class="sxs-lookup"><span data-stu-id="f6598-135">This can mean telling the linker to associate the decorated name with a simpler export name.</span></span> <span data-ttu-id="f6598-136">O nome da exportação pode ser o nome que apareceu originalmente no código-fonte ou qualquer outra coisa.</span><span class="sxs-lookup"><span data-stu-id="f6598-136">The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="f6598-137">A maneira como o nome é decorado depende do idioma e de como o compilador é instruído a disponibilizar a função, ou seja, a convenção de chamada.</span><span class="sxs-lookup"><span data-stu-id="f6598-137">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention.</span></span> <span data-ttu-id="f6598-138">A convenção de chamada padrão entre processos para o Windows usada por DLLs é conhecida como a convenção WinAPI.</span><span class="sxs-lookup"><span data-stu-id="f6598-138">The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention.</span></span> <span data-ttu-id="f6598-139">Ele é definida nos arquivos de cabeçalho do Windows como **WINAPI**, que por sua vez é definido usando o **__stdcall** do declarador do Win32.</span><span class="sxs-lookup"><span data-stu-id="f6598-139">It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="f6598-140">Uma função de exportação de DLL para uso com o Excel (se é uma função de planilha, função equivalente de folha de macro ou comando definido pelo usuário) sempre deve usar a convenção de chamada**WINAPI** / **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="f6598-140">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention.</span></span> <span data-ttu-id="f6598-141">É necessário incluir o especificador **WINAPI** explicitamente na definição da função, pois o padrão nos compiladores Win32 é usar a convenção de chamada **__cdecl**, também definida como **WINAPIV**, se nenhuma outra for especificada.</span><span class="sxs-lookup"><span data-stu-id="f6598-141">It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="f6598-142">Você pode dizer ao vinculador que uma função deve ser exportada, e o nome deve ser conhecido externamente de uma das várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="f6598-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="f6598-143">Coloque a função em um arquivo DEF após a palavra-chave **EXPORTS** e defina a configuração do projeto DLL para fazer referência a esse arquivo, vincular.</span><span class="sxs-lookup"><span data-stu-id="f6598-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="f6598-144">Use o declarador **__declspec(dllexport)** na definição de função.</span><span class="sxs-lookup"><span data-stu-id="f6598-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="f6598-145">Use uma diretiva de pré-processador **#pragma** diretiva para enviar o vinculador.</span><span class="sxs-lookup"><span data-stu-id="f6598-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="f6598-146">Embora seu projeto possa usar todos os três métodos e seu compilador e vinculador os suportem, você não deve tentar exportar uma função em mais de uma destas maneiras.</span><span class="sxs-lookup"><span data-stu-id="f6598-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="f6598-147">Por exemplo, suponha que uma DLL contenha dois módulos de código-fonte, um C e um C ++, que contenham duas funções a serem exportadas, **meu\_C\_exportar** e **meu\_Cpp\_exportar** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f6598-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="f6598-148">Para simplificar, suponha que cada função receba um único argumento numérico de precisão dupla e retorne o mesmo tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f6598-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="f6598-149">As alternativas para exportar cada função usando cada um desses métodos são descritas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="f6598-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="f6598-150">Usando um arquivo DEF</span><span class="sxs-lookup"><span data-stu-id="f6598-150">Using a DEF file</span></span>

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<br/>

<span data-ttu-id="f6598-151">O arquivo DEF precisa conter essas linhas.</span><span class="sxs-lookup"><span data-stu-id="f6598-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="f6598-152">A sintaxe geral de uma linha que segue uma instrução **EXPORTS** é a seguinte.</span><span class="sxs-lookup"><span data-stu-id="f6598-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="f6598-153">Observe que a função C foi decorada, mas o arquivo DEF explicitamente força o vinculador a expor a função usando o nome do código-fonte original (neste exemplo).</span><span class="sxs-lookup"><span data-stu-id="f6598-153">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example).</span></span> <span data-ttu-id="f6598-154">O vinculador exporta implicitamente a função C ++ usando o nome de código original, para que não seja necessário incluir o nome decorado no arquivo DEF.</span><span class="sxs-lookup"><span data-stu-id="f6598-154">The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="f6598-155">Para chamadas de função da API do Windows de 32 bits, a convenção para a decoração de funções compiladas em C é a seguinte: **function_name** se torna\*\* _ function_name @\*\* _n_ onde _n_ é o número de bytes expressos como um decimal usado por todos os argumentos, com os bytes para cada arredondado para cima até o múltiplo de quatro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="f6598-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f6598-156">Todos os ponteiros são quatro bytes de largura no Win32.</span><span class="sxs-lookup"><span data-stu-id="f6598-156">All pointers are four bytes wide in Win32.</span></span> <span data-ttu-id="f6598-157">O tipo de retorno não terá impacto sobre o nome da decoração.</span><span class="sxs-lookup"><span data-stu-id="f6598-157">The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="f6598-158">É possível forçar o compilador C ++ a expor nomes não-definidos para funções C ++ colocando a função e quaisquer protótipos de função dentro de um "C" externo {…}</span><span class="sxs-lookup"><span data-stu-id="f6598-158">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…}</span></span> <span data-ttu-id="f6598-159">bloqueio, como é mostrado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="f6598-159">block, as shown in this example.</span></span> <span data-ttu-id="f6598-160">(As chaves \*\* {} \*\* foram omitidos aqui porque a declaração refere-se somente ao bloco de código de função que o segue imediatamente).</span><span class="sxs-lookup"><span data-stu-id="f6598-160">(The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="f6598-161">Quando você está colocando protótipos de função C em arquivos de cabeçalho que podem ser incluídos em arquivos de origem C ou C ++, inclua a seguinte diretiva de pré-processador.</span><span class="sxs-lookup"><span data-stu-id="f6598-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="f6598-162">Usando declarador __declspec(dllexport)</span><span class="sxs-lookup"><span data-stu-id="f6598-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="f6598-163">A palavra-chave **__declspec(dllexport)** pode ser usada na declaração de função da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f6598-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="f6598-164">A palavra-chave **__declspec(dllexport)** deve ser adicionada à esquerda da declaração.</span><span class="sxs-lookup"><span data-stu-id="f6598-164">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration.</span></span> <span data-ttu-id="f6598-165">As vantagens dessa abordagem são que a função não precisa ser listada em um arquivo DEF e que o status de exportação está correto com a definição.</span><span class="sxs-lookup"><span data-stu-id="f6598-165">The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="f6598-166">Se você quiser evitar que uma função C ++ seja disponibilizada com a decoração do nome C ++, você deve declarar a função da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f6598-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="f6598-167">O vinculador disponibilizará a função como my_undecorated_Cpp_export, ou seja, o nome como aparece no código-fonte sem decoração.</span><span class="sxs-lookup"><span data-stu-id="f6598-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="f6598-168">Usando uma diretiva de vinculador de pré-processador #pragma</span><span class="sxs-lookup"><span data-stu-id="f6598-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="f6598-169">Versões recentes do Microsoft Visual Studio suportam duas macros predefinidas que, quando usadas em conjunto com uma diretiva **#pragma**, permite que você instrua o vinculador a exportar a função diretamente de dentro do código de função.</span><span class="sxs-lookup"><span data-stu-id="f6598-169">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code.</span></span> <span data-ttu-id="f6598-170">As macros são __FUNCTION__ e __FUNCDNAME__ (observe o sublinhado duplo em cada extremidade) que são expandidas para os nomes das funções não decoradas e decoradas, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f6598-170">The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="f6598-171">Por exemplo, quando você está usando o Microsoft Visual Studio, essas linhas podem ser incorporadas em um arquivo de cabeçalho comum da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f6598-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="f6598-172">Se esse cabeçalho estiver incluído nos arquivos de origem, as duas funções de exemplo poderão ser exportadas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="f6598-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="f6598-173">Código C:</span><span class="sxs-lookup"><span data-stu-id="f6598-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="f6598-174">Código C++:</span><span class="sxs-lookup"><span data-stu-id="f6598-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="f6598-175">Observe que a diretiva deve ser colocada no corpo da função e só está expandida quando nenhuma das opções do compilador **/EP** ou **/p** é definida.</span><span class="sxs-lookup"><span data-stu-id="f6598-175">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set.</span></span> <span data-ttu-id="f6598-176">Essa técnica elimina a necessidade de um arquivo DEF ou declaração **__declspec(dllexport)** e mantém a especificação do seu status de exportação com o código de função.</span><span class="sxs-lookup"><span data-stu-id="f6598-176">This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f6598-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="f6598-177">See also</span></span>

- [<span data-ttu-id="f6598-178">Acessar DLLs no Excel</span><span class="sxs-lookup"><span data-stu-id="f6598-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="f6598-179">Calling into Excel from the DLL or XLL</span><span class="sxs-lookup"><span data-stu-id="f6598-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="f6598-180">Conceitos de programação do Excel</span><span class="sxs-lookup"><span data-stu-id="f6598-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="f6598-181">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="f6598-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

