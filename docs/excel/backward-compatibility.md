---
title: Compatibilidade com versões anteriores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilidade de versão [excel 2007,] compatibilidade XLL [Excel 2007], [Excel 2007] compatibilidade com versões anteriores
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3e1368ef55b96be947527456e0f01918afec6663
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387969"
---
# <a name="backward-compatibility"></a><span data-ttu-id="a789d-104">Compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="a789d-104">Backward Compatibility</span></span>

<span data-ttu-id="a789d-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a789d-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a789d-106">Este tópico aborda os problemas de compatibilidade XLL em diferentes versões do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="a789d-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="a789d-107">Definições de constantes úteis</span><span class="sxs-lookup"><span data-stu-id="a789d-107">Useful constant definitions</span></span>

<span data-ttu-id="a789d-108">Considere incluir definições semelhantes a esses elementos no seu código do project XLL e substituir todas as instâncias de números literais usadas neste contexto.</span><span class="sxs-lookup"><span data-stu-id="a789d-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="a789d-109">Isso irá esclarecer o código específicos da versão e reduzir a probabilidade de bugs relacionados à versão no formulário de números de aparência inofensiva.</span><span class="sxs-lookup"><span data-stu-id="a789d-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
```cpp
#define MAX_XL11_ROWS            65536
#define MAX_XL11_COLS              256
#define MAX_XL12_ROWS          1048576
#define MAX_XL12_COLS            16384
#define MAX_XL11_UDF_ARGS           30
#define MAX_XL12_UDF_ARGS          255
#define MAX_XL4_STR_LEN           255u
#define MAX_XL12_STR_LEN        32767u
```

## <a name="getting-the-running-version"></a><span data-ttu-id="a789d-110">Obter a versão em execução</span><span class="sxs-lookup"><span data-stu-id="a789d-110">Getting the running version</span></span>

<span data-ttu-id="a789d-111">Você deve detectar qual versão está sendo executada usando `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, que é `arg` uma definição numérico **XLOPER** como o 2. A versão é uma cadeia de caracteres **XLOPER** que pode ser forçada a um numérico inteiro.</span><span class="sxs-lookup"><span data-stu-id="a789d-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="a789d-112">Para o Microsoft Excel 2013, ele é 15.0.</span><span class="sxs-lookup"><span data-stu-id="a789d-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="a789d-113">Fazer isso em ou a partir da função, [xlAutoOpen](xlautoopen.md).</span><span class="sxs-lookup"><span data-stu-id="a789d-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="a789d-114">Em seguida, você pode definir uma variável global que informe todos os módulos do seu projeto em que a versão do Excel está em execução.</span><span class="sxs-lookup"><span data-stu-id="a789d-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="a789d-115">O código pode decidir se vai acionar usando a API C **Excel12** e **XLOPER12**s ou usando **Excel4** usando **XLOPER**s.</span><span class="sxs-lookup"><span data-stu-id="a789d-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="a789d-116">Você pode acionar **XLCallVer** para descobrir a versão API C, mas isso não indica qual das versões anteriores do Excel 2007 você está executando.</span><span class="sxs-lookup"><span data-stu-id="a789d-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="a789d-117">Criar suplementos que exportam interfaces duplas</span><span class="sxs-lookup"><span data-stu-id="a789d-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="a789d-118">Considere uma função XLL que leva de uma cadeia de caracteres e retorna um valor que pode ser qualquer um dos tipos de dados de planilha.</span><span class="sxs-lookup"><span data-stu-id="a789d-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="a789d-119">Você pode exportar uma função registrada como tipo PD e com o protótipo a seguir, onde a cadeia é passada como uma cadeia de comprimento contados em bytes. </span><span class="sxs-lookup"><span data-stu-id="a789d-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="a789d-120">Embora isso funcione muito bem, há vários motivos para que ela não seja a interface ideal para o código a partir do Excel 2007:</span><span class="sxs-lookup"><span data-stu-id="a789d-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="a789d-121">Ele está sujeito às limitações de cadeias de caracteres de bytes C API e não é possível acessar as longas cadeias de caracteres Unicode com suporte a partir do Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="a789d-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="a789d-122">No entanto, a partir do Excel 2007, o Excel pode passar e aceitar o **XLOPER**s. Internamente ele os converte para **XLOPER12**s. Portanto, há uma conversão implícita de sobrecarga a partir do Excel 2007 que não estará lá quando o código for executado em versões anteriores do Excel.</span><span class="sxs-lookup"><span data-stu-id="a789d-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="a789d-123">Talvez esta função possa ser feita com thread de segurança, mas se a cadeia de caracteres é alterada para `PD$`, o registro falhará em Iniciar antes do Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="a789d-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="a789d-124">Por esse motivo, idealmente, a partir do Excel 2007, você deve exportar uma função para os usuários que foram registrado como `QD%$`, supondo que o código tenha thread de segurança, como no protótipo a seguir.</span><span class="sxs-lookup"><span data-stu-id="a789d-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="a789d-125">Outro motivo, para que você querer registrar uma função diferente a partir do Excel 2007 é o fato das funções XLL permitir acima de 255 argumentos, em vez do limite de 30 das versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a789d-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="a789d-126">Felizmente, você pode ter os benefícios de ambos ao exportar as duas versões do seu projeto.</span><span class="sxs-lookup"><span data-stu-id="a789d-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="a789d-127">Você pode detectar a versão do Excel em execução e inscrever condicionalmente a função mais apropriada.</span><span class="sxs-lookup"><span data-stu-id="a789d-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="a789d-128">Para mais informações e para um exemplo de implementação, confira [desenvolvendo suplementos (XLLs) no Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="a789d-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](https://msdn.microsoft.com/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="a789d-129">Essa abordagem traz a possibilidade de uma planilha em execução no Excel 2003 poder exibir resultados diferentes do que a execução da mesma planilha a partir do Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="a789d-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="a789d-130">Por exemplo, o Excel 2003 mapearia uma cadeia Unicode em uma célula de planilha do Excel 2003 para uma cadeia de bytes ASCII e truncaria antes de passar para uma função XLL.</span><span class="sxs-lookup"><span data-stu-id="a789d-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="a789d-131">A partir do Excel 2007, o Excel passará uma cadeia Unicode não convertida para uma função XLL registrada da maneira certa.</span><span class="sxs-lookup"><span data-stu-id="a789d-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="a789d-132">Isso pode levar a um resultado diferente.</span><span class="sxs-lookup"><span data-stu-id="a789d-132">This could lead to a different result.</span></span> <span data-ttu-id="a789d-133">Você deve estar ciente dessa possibilidade e das consequências aos seus usuários, não apenas na atualização.</span><span class="sxs-lookup"><span data-stu-id="a789d-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="a789d-134">Por exemplo, algumas funções internas numéricas foram aprimoradas entre o Excel 2003 e o Excel 2000.</span><span class="sxs-lookup"><span data-stu-id="a789d-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="a789d-135">Novas funções de planilha e funções de análise</span><span class="sxs-lookup"><span data-stu-id="a789d-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="a789d-136">Funções de análise de ferramentas (ATP) fazem parte do Excel a partir do Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="a789d-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="a789d-137">Anteriormente, um XLL apenas poderia acionar uma função ATP usando [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="a789d-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="a789d-138">A partir do Excel 2007, funções ATP devem ser acionadas usando enumerações de função estipuladas em xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="a789d-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="a789d-139">O exemplo em Chamar funções definidas pelo usuário a partir de DLLs demonstra dois métodos diferentes.</span><span class="sxs-lookup"><span data-stu-id="a789d-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a789d-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="a789d-140">See also</span></span>

- [<span data-ttu-id="a789d-141">Retorno de chamada da API de C: funções Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="a789d-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="a789d-142">Programação com a API de C no Excel</span><span class="sxs-lookup"><span data-stu-id="a789d-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="a789d-143">Novidades na API de C do Excel</span><span class="sxs-lookup"><span data-stu-id="a789d-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

