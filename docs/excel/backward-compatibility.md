---
title: Compatibilidade com versões anteriores
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- compatibilidade de versão [excel 2007], compatibilidade XLL [Excel 2007], [Excel 2007] de compatibilidade com versões anteriores
localization_priority: Normal
ms.assetid: ac200824-0620-4f03-8bd2-59226c1e79d7
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 095961fa909a67b354ed43a7e093b79a9ebb4f18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765263"
---
# <a name="backward-compatibility"></a><span data-ttu-id="56091-104">Compatibilidade com versões anteriores</span><span class="sxs-lookup"><span data-stu-id="56091-104">Backward compatibility</span></span>

<span data-ttu-id="56091-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="56091-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="56091-106">Este tópico aborda os problemas de compatibilidade XLL em versões diferentes do Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="56091-106">This topic addresses issues of XLL compatibility in different versions of Microsoft Excel.</span></span>
  
## <a name="useful-constant-definitions"></a><span data-ttu-id="56091-107">Definições constantes úteis</span><span class="sxs-lookup"><span data-stu-id="56091-107">Useful constant definitions</span></span>

<span data-ttu-id="56091-108">Considere incluindo definições semelhantes a estas em seu código de projeto XLL e substituindo todas as instâncias de números literais usadas nesse contexto.</span><span class="sxs-lookup"><span data-stu-id="56091-108">Consider including definitions similar to these in your XLL project code and replacing all instances of literal numbers used in this context.</span></span> <span data-ttu-id="56091-109">Isso esclarecer o código que é específico de versão e reduzir a probabilidade de bugs relacionados à versão no formato dos números inofensiva.</span><span class="sxs-lookup"><span data-stu-id="56091-109">This will clarify code that is version specific, and reduce the likelihood of version-related bugs in the form of innocuous-looking numbers.</span></span>
  
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

## <a name="getting-the-running-version"></a><span data-ttu-id="56091-110">Obtendo a versão em execução</span><span class="sxs-lookup"><span data-stu-id="56091-110">Getting the running version</span></span>

<span data-ttu-id="56091-111">Você deve detectar qual versão está sendo executado usando `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, onde `arg` é um **XLOPER** numérico definido como 2 e versão é uma cadeia de caracteres **XLOPER** , que então pode ser forçada como um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="56091-111">You should detect which version is running using  `Excel4(xlfGetWorkspace, &amp;version, 1, &amp;arg)`, where  `arg` is a numeric **XLOPER** set to 2 and version is a string **XLOPER** which can then be coerced to an integer.</span></span> <span data-ttu-id="56091-112">Para o Microsoft Excel 2013, isso é 15.0.</span><span class="sxs-lookup"><span data-stu-id="56091-112">For Microsoft Excel 2013, this is 15.0.</span></span> <span data-ttu-id="56091-113">Você deve fazer isso em ou a função [xlAutoOpen](xlautoopen.md) de.</span><span class="sxs-lookup"><span data-stu-id="56091-113">You should do this in, or from, the [xlAutoOpen](xlautoopen.md) function.</span></span> <span data-ttu-id="56091-114">Em seguida, você pode definir uma variável global que informa que todos os módulos no seu projeto do qual versão do Excel está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="56091-114">You can then set a global variable that informs all of the modules in your project which version of Excel is running.</span></span> <span data-ttu-id="56091-115">Seu código, em seguida, poderá decidir se chame o API C usando **Excel12** e **XLOPER12**s ou **Excel4** usando **XLOPER**s.</span><span class="sxs-lookup"><span data-stu-id="56091-115">Your code can then decide whether to call the C API using **Excel12** and **XLOPER12**s, or using **Excel4** using **XLOPER**s.</span></span>
  
<span data-ttu-id="56091-116">Você pode chamar **XLCallVer** para descobrir a versão do C API, mas isso não indica qual das versões anteriores do Excel 2007 você está executando.</span><span class="sxs-lookup"><span data-stu-id="56091-116">You can call **XLCallVer** to discover the C API version, but this does not indicate which of the pre-Excel 2007 versions you are running.</span></span> 
  
## <a name="creating-add-ins-that-export-dual-interfaces"></a><span data-ttu-id="56091-117">Criando suplementos que exportam interfaces duplas</span><span class="sxs-lookup"><span data-stu-id="56091-117">Creating add-ins that export dual interfaces</span></span>

<span data-ttu-id="56091-118">Considere uma função XLL que utiliza uma cadeia de caracteres e retorna um valor que pode ser qualquer um dos tipos de dados de planilha.</span><span class="sxs-lookup"><span data-stu-id="56091-118">Consider an XLL function that takes a string and returns a value that can be any of the worksheet data types.</span></span> <span data-ttu-id="56091-119">Você pode exportar uma função registrada conforme digita "PD" e com protótipo da seguinte maneira em que a cadeia de caracteres é passada como uma cadeia de caracteres de byte de comprimento contado.</span><span class="sxs-lookup"><span data-stu-id="56091-119">You could export a function registered as type "PD" and prototyped as follows where the string is passed as a length-counted byte string.</span></span>
  
`LPXLOPER WINAPI my_xll_fn(unsigned char *arg);`
  
<span data-ttu-id="56091-120">Embora isso funcione perfeitamente bem, há vários motivos por que isso não é a interface ideal para seu código iniciando no Excel 2007:</span><span class="sxs-lookup"><span data-stu-id="56091-120">Although this works perfectly well, there are several reasons why this is not the ideal interface to your code starting in Excel 2007:</span></span>
  
- <span data-ttu-id="56091-121">Ela está sujeito às limitações de cadeias de caracteres de byte C API e não pode acessar as Unicode cadeias de caracteres longas suportadas iniciada no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="56091-121">It is subject to the limitations of C API byte strings and cannot access the long Unicode strings supported starting in Excel 2007.</span></span>
    
- <span data-ttu-id="56091-122">Embora, começando no Excel 2007, Excel pode passar e aceitar **XLOPER**s, internamente ele os converte em **XLOPER12**s, portanto, há uma sobrecarga de conversão implícita iniciada no Excel 2007 que não existe quando o código é executado em versões anteriores do Excel.</span><span class="sxs-lookup"><span data-stu-id="56091-122">Although, starting in Excel 2007, Excel can pass and accept **XLOPER**s, internally it converts them to **XLOPER12**s, so there is an implicit conversion overhead starting in Excel 2007 that is not there when the code runs in earlier versions of Excel.</span></span>
    
- <span data-ttu-id="56091-123">Pode ser que esta função pode ser feita segmento seguros, mas se o tipo de cadeia de caracteres for alterado para `PD$`, registro falha na inicialização antes do Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="56091-123">It may be that this function can be made thread safe, but if the type string is changed to  `PD$`, registration fails in starting before Excel 2007.</span></span>
    
<span data-ttu-id="56091-124">Por esses motivos, idealmente, iniciando no Excel 2007, você deve exportar uma função para os usuários que foi registrado como `QD%$`, assumindo que seu código é thread segura e com protótipo da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="56091-124">For these reasons, ideally, starting in Excel 2007 you should export a function for your users that was registered as  `QD%$`, assuming your code is thread safe and prototyped as follows.</span></span>
  
`LPXLOPER12 WINAPI my_xll_fn_v12(wchar_t *arg);`
  
<span data-ttu-id="56091-125">Outro motivo por que talvez você queira registrar uma função diferente iniciando no Excel 2007 é que ele permite que funções XLL assumam até 255 argumentos, em vez do limite de 30 de versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="56091-125">Another reason why you might want to register a different function starting in Excel 2007 is that it permits XLL functions to take up to 255 arguments, instead of the 30 limit of earlier versions.</span></span>
  
<span data-ttu-id="56091-126">Felizmente, é possível ter os benefícios de ambas exportando as duas versões do projeto.</span><span class="sxs-lookup"><span data-stu-id="56091-126">Fortunately, you can have the benefits of both by exporting both versions from your project.</span></span> <span data-ttu-id="56091-127">Você pode detectar, em seguida, a versão do Excel em execução e condicionalmente, registra a função mais apropriada.</span><span class="sxs-lookup"><span data-stu-id="56091-127">You can then detect the running Excel version and conditionally register the most appropriate function.</span></span> <span data-ttu-id="56091-128">Para obter mais informações e um exemplo de implementação, consulte [Developing suplementos (XLLs) no Excel 2007](http://msdn.microsoft.com/pt-br/library/aa730920.aspx).</span><span class="sxs-lookup"><span data-stu-id="56091-128">For more information and an example implementation, see [Developing Add-ins (XLLs) in Excel 2007](http://msdn.microsoft.com/pt-br/library/aa730920.aspx).</span></span>
  
<span data-ttu-id="56091-129">Essa abordagem leva à possibilidade de que uma planilha executada no Excel 2003 poderia exibir resultados diferentes da mesma planilha executando iniciada no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="56091-129">This approach leads to the possibility that a worksheet running in Excel 2003 could display different results than the same sheet running starting in Excel 2007.</span></span> <span data-ttu-id="56091-130">Por exemplo, o Excel 2003 seria mapear uma cadeia de caracteres Unicode em uma célula de planilha do Excel 2003 para uma sequência de byte ASCII e truncá-lo antes de passá-la para uma função XLL.</span><span class="sxs-lookup"><span data-stu-id="56091-130">For example, Excel 2003 would map a Unicode string in an Excel 2003 worksheet cell to an ASCII byte-string and truncate it before passing it to an XLL function.</span></span> <span data-ttu-id="56091-131">Iniciando no Excel 2007, Excel passará uma sequência de caracteres Unicode não convertida para uma função XLL registrada da forma correta.</span><span class="sxs-lookup"><span data-stu-id="56091-131">Starting in Excel 2007, Excel will pass an unconverted Unicode string to an XLL function registered in the right way.</span></span> <span data-ttu-id="56091-132">Isso pode implicar um resultado diferente.</span><span class="sxs-lookup"><span data-stu-id="56091-132">This could lead to a different result.</span></span> <span data-ttu-id="56091-133">Você deve estar ciente dessa possibilidade e as consequências para seus usuários, não apenas na atualização.</span><span class="sxs-lookup"><span data-stu-id="56091-133">You should be aware of this possibility and the consequences to your users, not just in the upgrade.</span></span> <span data-ttu-id="56091-134">Por exemplo, algumas funções numéricas internas foram aperfeiçoadas entre o Excel 2000 e o Excel 2003.</span><span class="sxs-lookup"><span data-stu-id="56091-134">For example, some built-in numeric functions were improved between Excel 2000 and Excel 2003.</span></span>
  
## <a name="new-worksheet-functions-and-analysis-toolpak-functions"></a><span data-ttu-id="56091-135">Novas funções de planilha e ferramentas de análise</span><span class="sxs-lookup"><span data-stu-id="56091-135">New Worksheet functions and Analysis Toolpak functions</span></span>

<span data-ttu-id="56091-136">Funções do análise (ATP) de ferramentas fazem parte do Excel iniciada no Excel 2007.</span><span class="sxs-lookup"><span data-stu-id="56091-136">Analysis Toolpak (ATP) functions are part of Excel starting in Excel 2007.</span></span> <span data-ttu-id="56091-137">Anteriormente, um XLL somente poderia chamar uma função ATP usando [xlUDF](xludf.md).</span><span class="sxs-lookup"><span data-stu-id="56091-137">Previously, an XLL could only call an ATP function by using [xlUDF](xludf.md).</span></span> <span data-ttu-id="56091-138">Iniciando no Excel 2007, as funções ATP devem ser chamadas usando as enumerações de função definidas no xlcall. h.</span><span class="sxs-lookup"><span data-stu-id="56091-138">Starting in Excel 2007, the ATP functions should be called using the function enumerations defined in xlcall.h.</span></span> <span data-ttu-id="56091-139">O exemplo em funções definidas pelo usuário chamando a partir de DLLs demonstra os dois métodos diferentes.</span><span class="sxs-lookup"><span data-stu-id="56091-139">The example in Calling User-defined Functions from DLLs demonstrates the two different methods.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="56091-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="56091-140">See also</span></span>

- [<span data-ttu-id="56091-141">C API Callback Functions Excel4, Excel12</span><span class="sxs-lookup"><span data-stu-id="56091-141">C API Callback Functions Excel4, Excel12</span></span>](c-api-callback-functions-excel4-excel12.md) 
- [<span data-ttu-id="56091-142">Programando com a API C no Excel</span><span class="sxs-lookup"><span data-stu-id="56091-142">Programming with the C API in Excel</span></span>](programming-with-the-c-api-in-excel.md)
- [<span data-ttu-id="56091-143">What's New in the C API for Excel</span><span class="sxs-lookup"><span data-stu-id="56091-143">What's New in the C API for Excel</span></span>](what-s-new-in-the-c-api-for-excel.md)

