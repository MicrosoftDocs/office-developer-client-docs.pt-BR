---
title: Desenvolver DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- DLLs [excel 2007], a criação, criando DLLs [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765284"
---
# <a name="developing-dlls"></a><span data-ttu-id="8f4f0-104">Desenvolver DLLs</span><span class="sxs-lookup"><span data-stu-id="8f4f0-104">Developing DLLs</span></span>

<span data-ttu-id="8f4f0-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8f4f0-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="8f4f0-106">Uma biblioteca é um corpo de código compilado que fornece algumas funcionalidades e os dados para um aplicativo executável.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-106">A library is a body of compiled code that provides some functionality and data to an executable application.</span></span> <span data-ttu-id="8f4f0-107">Bibliotecas podem ser vinculadas estaticamente ou dinamicamente vinculadas e convencionalmente têm o. lib extensões de nome de arquivo e. dll respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-107">Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively.</span></span> <span data-ttu-id="8f4f0-108">Bibliotecas estáticas (por exemplo, a biblioteca de tempo de execução do C) são vinculadas ao aplicativo na compilação e então se torna parte do executável resultante.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-108">Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable.</span></span> <span data-ttu-id="8f4f0-109">O aplicativo carrega uma DLL quando ela for necessária, geralmente quando o aplicativo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-109">The application loads a DLL when it is needed, usually when the application starts up.</span></span> <span data-ttu-id="8f4f0-110">Uma DLL pode carregar e vincular dinamicamente a outro DLL.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-110">One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="8f4f0-111">Benefícios do uso de DLLs</span><span class="sxs-lookup"><span data-stu-id="8f4f0-111">Benefits of using DLLs</span></span>

<span data-ttu-id="8f4f0-112">Os principais benefícios do DLLs são:</span><span class="sxs-lookup"><span data-stu-id="8f4f0-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="8f4f0-113">Todos os aplicativos podem compartilhar uma única cópia no disco.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="8f4f0-114">Arquivos executáveis de nos aplicativos são mantidos menores.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="8f4f0-115">Eles permitem que os projetos de desenvolvimento de grandes sejam divididos.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-115">They enable large development projects to be broken down.</span></span> <span data-ttu-id="8f4f0-116">Os desenvolvedores de aplicativos e DLL precisam concorda apenas uma interface entre seus respectivos papéis.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-116">Application and DLL developers only need agree an interface between their respective parts.</span></span> <span data-ttu-id="8f4f0-117">Esta interface é exportada pela DLL.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-117">This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="8f4f0-118">Os desenvolvedores DLL podem atualizar DLLs — talvez para torná-los mais eficiente ou para corrigir um bug — sem precisar atualizar todos os aplicativos que usá-lo, desde que a interface exportada da DLL não é alterado.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="8f4f0-119">Você pode usar DLLs para adicionar funções de planilha e comandos no Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="8f4f0-120">Recursos para a criação de DLLs</span><span class="sxs-lookup"><span data-stu-id="8f4f0-120">Resources for creating DLLs</span></span>

<span data-ttu-id="8f4f0-121">Para criar uma DLL, você precisará dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="8f4f0-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="8f4f0-122">Um editor de código fonte.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-122">A source code editor.</span></span>
    
- <span data-ttu-id="8f4f0-123">Um compilador para transformar o código-fonte em código do objeto que é compatível com o seu hardware.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="8f4f0-124">Um vinculador para adicionar o código de bibliotecas estáticas, onde usado e para criar o arquivo DLL executável.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="8f4f0-125">Ambientes de desenvolvimento integrado moderno (IDEs), como o Microsoft Visual Studio, fornecem todas essas coisas.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-125">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things.</span></span> <span data-ttu-id="8f4f0-126">Eles também fornecem uma excelente oportunidade mais: inteligente de editores, ferramentas para depurar seu código, ferramentas para gerenciar vários projetos, novos assistentes de projeto e muitas outras ferramentas importantes.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-126">They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="8f4f0-127">Você pode criar DLLs em diversos idiomas, por exemplo, C/C++, Pascal e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-127">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic.</span></span> <span data-ttu-id="8f4f0-128">Considerando que o código-fonte API fornecido com o Excel é C e C++, apenas esses dois idiomas são considerados nesta documentação.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-128">Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="8f4f0-129">Exportando funções e comandos</span><span class="sxs-lookup"><span data-stu-id="8f4f0-129">Exporting functions and commands</span></span>

<span data-ttu-id="8f4f0-130">Ao compilar um projeto DLL, o compilador e vinculador precisam saber quais funções são a ser exportado para que eles podem torná-los disponíveis para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-130">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application.</span></span> <span data-ttu-id="8f4f0-131">Esta seção descreve as maneiras como isso pode ser feito.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-131">This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="8f4f0-132">Quando compiladores compilar código-fonte, em geral, eles alteram os nomes das funções de sua aparência no código-fonte.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-132">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code.</span></span> <span data-ttu-id="8f4f0-133">Eles geralmente fazem isso por meio da adição de início e/ou final do nome, em um processo conhecido como simplificação de nome.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-133">They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration.</span></span> <span data-ttu-id="8f4f0-134">Você deve certificar-se de que a função é exportada com um nome reconhecível para o aplicativo ao carregar a DLL.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-134">You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL.</span></span> <span data-ttu-id="8f4f0-135">Isso pode significar informando o vinculador para associar o nome decorado com um nome de exportação mais simples.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-135">This can mean telling the linker to associate the decorated name with a simpler export name.</span></span> <span data-ttu-id="8f4f0-136">O nome da exportação pode ser o nome como ele apareceu originalmente no código-fonte ou outra coisa.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-136">The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="8f4f0-137">A maneira como o nome é decorado depende do idioma e como o compilador é instruído para disponibilizar a função, ou seja, a convenção de chamada.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-137">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention.</span></span> <span data-ttu-id="8f4f0-138">A convenção de chamada de standard entre processos para Windows usado pelo DLLs é conhecida como a convenção WinAPI.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-138">The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention.</span></span> <span data-ttu-id="8f4f0-139">Ele é definido em arquivos de cabeçalho do Windows como **WINAPI**, que é definido por sua vez usando o declarador do Win32 **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-139">It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="8f4f0-140">Uma função de exportação de DLL para uso com o Excel (se é uma função de planilha, folha de macro de função equivalente ou comando definida pelo usuário) sempre deve usar o **WINAPI** / **__stdcall** convenção de chamada.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-140">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention.</span></span> <span data-ttu-id="8f4f0-141">É necessário incluir o especificador **WINAPI** explicitamente na definição da função como o padrão no Win32 compiladores é usar o **cdecl** chamar convenção, também são definida como **WINAPIV**, se nenhuma estiver especificada.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-141">It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="8f4f0-142">Você pode dizer o vinculador que uma função deve ser exportado e o nome é conhecido por externamente de várias maneiras:</span><span class="sxs-lookup"><span data-stu-id="8f4f0-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="8f4f0-143">Coloque a função em um arquivo DEF após a palavra-chave **exportações** e defina sua configuração de projeto DLL para fazer referência a este arquivo quando vincular.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="8f4f0-144">Use o declarador **__declspec(dllexport)** na definição da função.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="8f4f0-145">Use uma diretiva de pré-processador **#pragma** para enviar uma mensagem para o vinculador.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="8f4f0-146">Embora o seu projeto pode usar todos os três métodos e seu compilador e vinculador oferecer suporte a eles, você não deve tentar uma função em mais de uma dessas maneiras de exportação.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="8f4f0-147">Por exemplo, suponha que uma DLL contém módulos de código fonte dois, um C e um C++, que contêm as duas funções a serem exportados, **Meu\_C\_exportar** e **minha\_Cpp\_exportar** respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="8f4f0-148">Para manter a simplicidade, suponha que cada função usa um único argumento numérico de precisão dupla e retorna o mesmo tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="8f4f0-149">As alternativas para a exportação de cada função usando cada um desses métodos são descritas nas seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="8f4f0-150">Usando um arquivo DEF</span><span class="sxs-lookup"><span data-stu-id="8f4f0-150">Using a DEF file</span></span>

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

<span data-ttu-id="8f4f0-151">O arquivo DEF precisa conter essas linhas.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="8f4f0-152">A sintaxe geral de uma linha que segue uma instrução **exportações** é da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="8f4f0-153">Observe que a função C foi decorada, mas o arquivo DEF explicitamente força o vinculador expor a função usando o nome de código fonte original (neste exemplo).</span><span class="sxs-lookup"><span data-stu-id="8f4f0-153">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example).</span></span> <span data-ttu-id="8f4f0-154">O vinculador implicitamente exporta a função C++ utilizando o nome de código original, para que ele não é necessário incluir o nome decorado no arquivo DEF.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-154">The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="8f4f0-155">Para chamadas de função de API do Windows de 32 bits, a convenção para a decoração de funções compilado C é da seguinte maneira: **nome_da_função** se torna _ **nome_da_função @** _n_ onde _n_ é o número de bytes, expressado como um número decimal ocupado por todos os argumentos, com os bytes para cada arredondado para cima até o múltiplo mais próximo de quatro.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8f4f0-156">Todos os ponteiros são ampla no Win32 de quatro bytes.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-156">All pointers are four bytes wide in Win32.</span></span> <span data-ttu-id="8f4f0-157">O tipo de retorno tem nenhum impacto sobre simplificação de nome.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-157">The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="8f4f0-158">É possível forçar o compilador C++ expor nomes não decorados para funções C++ colocando-se a função e protótipos de função, dentro de um externo "C" {...}</span><span class="sxs-lookup"><span data-stu-id="8f4f0-158">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…}</span></span> <span data-ttu-id="8f4f0-159">bloquear, conforme mostrado neste exemplo.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-159">block, as shown in this example.</span></span> <span data-ttu-id="8f4f0-160">(Das chaves **{}** forem omitidos aqui porque a declaração refere-se apenas para o bloco de código de função que o segue imediatamente).</span><span class="sxs-lookup"><span data-stu-id="8f4f0-160">(The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="8f4f0-161">Quando você está colocando C protótipos de função nos arquivos de cabeçalho que poderiam ser incluídos nos arquivos de origem do C ou C++, você deve incluir a diretiva de pré-processador a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
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

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="8f4f0-162">Usando o declarador __declspec(dllexport)</span><span class="sxs-lookup"><span data-stu-id="8f4f0-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="8f4f0-163">A palavra-chave **__declspec(dllexport)** pode ser usada na declaração de função da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="8f4f0-164">A palavra-chave **__declspec(dllexport)** deve ser adicionada à extrema esquerda da declaração.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-164">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration.</span></span> <span data-ttu-id="8f4f0-165">As vantagens dessa abordagem são que a função não precisa ser listadas em um arquivo de definição e o status de exportação é correta com a definição.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-165">The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="8f4f0-166">Se você deseja evitar uma função C++ sendo disponibilizada com a simplificação de nome de C++, você deve declarar a função da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="8f4f0-167">O vinculador disponibilizarão a função como my_undecorated_Cpp_export, ou seja, o nome como ele aparece no código-fonte com sem decoração.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="8f4f0-168">Usar uma diretiva de pré-processador vinculador #pragma</span><span class="sxs-lookup"><span data-stu-id="8f4f0-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="8f4f0-169">Versões recentes do Microsoft Visual Studio oferecem suporte a duas macros predefinidas que, quando usado em conjunto com uma diretiva **#pragma** , permitem que você instruir o vinculador para exportar a função diretamente de dentro do código de função.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-169">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code.</span></span> <span data-ttu-id="8f4f0-170">As macros são __função__ e __FUNCDNAME__ (Observe o sublinhado duplo em cada extremidade) que são expandidos para os nomes de função não decorado e decorada respectivamente.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-170">The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="8f4f0-171">Por exemplo, quando você estiver usando o Microsoft Visual Studio, essas linhas podem ser incorporadas em um arquivo de cabeçalho comuns da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="8f4f0-172">Se este conector está incluído nos arquivos de origem, as funções de dois exemplo podem ser exportadas da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="8f4f0-173">Código de C:</span><span class="sxs-lookup"><span data-stu-id="8f4f0-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="8f4f0-174">Código de C++:</span><span class="sxs-lookup"><span data-stu-id="8f4f0-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="8f4f0-175">Observe que a diretiva deve ser colocada dentro do corpo da função e é expandida apenas quando nenhuma das opções de compilador **/EP** ou **/P** é definido.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-175">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set.</span></span> <span data-ttu-id="8f4f0-176">Essa técnica remove a necessidade de um arquivo DEF, ou declaração de **__declspec(dllexport)** e mantém a especificação de seu status de exportação com o código de função.</span><span class="sxs-lookup"><span data-stu-id="8f4f0-176">This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8f4f0-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f4f0-177">See also</span></span>

- [<span data-ttu-id="8f4f0-178">Acessar DLLs no Excel</span><span class="sxs-lookup"><span data-stu-id="8f4f0-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="8f4f0-179">Calling into Excel from the DLL or XLL</span><span class="sxs-lookup"><span data-stu-id="8f4f0-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="8f4f0-180">Excel Programming Concepts</span><span class="sxs-lookup"><span data-stu-id="8f4f0-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="8f4f0-181">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="8f4f0-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

