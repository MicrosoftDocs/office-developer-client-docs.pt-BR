---
title: Acessar DLLs no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- acessar dlls [excel 2007], DLLs [Excel 2007], acessar no Excel
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765376"
---
# <a name="access-dlls-in-excel"></a><span data-ttu-id="d4ef7-104">Acessar DLLs no Excel</span><span class="sxs-lookup"><span data-stu-id="d4ef7-104">How to: Access DLLs in Excel</span></span>

<span data-ttu-id="d4ef7-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d4ef7-105">Applies to: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="d4ef7-106">Você pode acessar um comando ou função DLL no Microsoft Excel de diversas maneiras:</span><span class="sxs-lookup"><span data-stu-id="d4ef7-106">You can access a DLL function or command in Microsoft Excel in several ways:</span></span>
  
- <span data-ttu-id="d4ef7-107">Por meio de um módulo de código Microsoft VBA (Visual Basic for Applications) na qual a função ou comando foi disponibilizada usando uma instrução **Declare**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-107">Through a Microsoft Visual Basic for Applications (VBA) code module in which the function or command has been made available using a **Declare** statement.</span></span> 
    
- <span data-ttu-id="d4ef7-108">Por meio de uma folha de macro XLM usando as funções **CALL** ou **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-108">Through an XLM macro sheet by using the **CALL** or **REGISTER** functions.</span></span> 
    
- <span data-ttu-id="d4ef7-109">Diretamente da planilha ou de um item personalizado na IU (interface do usuário).</span><span class="sxs-lookup"><span data-stu-id="d4ef7-109">Directly from the worksheet or from a customized item in the user interface (UI).</span></span>
    
<span data-ttu-id="d4ef7-p101">Esta documentação não aborda as funções XLM. É recomendável que você use uma das outras duas abordagens.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p101">This documentation does not cover XLM functions. It is recommended that you use either of the other two approaches.</span></span>
  
<span data-ttu-id="d4ef7-p102">Para acessar diretamente na planilha ou em um item personalizado na interface de usuário, primeiro a função ou o comando deve ser registrado no Excel. Confira mais informações sobre como registrar os comandos e as funções, veja [Acessar código XLL no Excel](accessing-xll-code-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p102">To be accessed directly from the worksheet or from a customized item in the UI, the function or command must first be registered with Excel. For information about registering commands and functions, see [Accessing XLL Code in Excel](accessing-xll-code-in-excel.md).</span></span>
  
## <a name="calling-dll-functions-and-commands-from-vba"></a><span data-ttu-id="d4ef7-114">Chamar funções e comandos DLL do VBA</span><span class="sxs-lookup"><span data-stu-id="d4ef7-114">Calling DLL Functions and Commands from VBA</span></span>

<span data-ttu-id="d4ef7-p103">Você pode acessar os comandos e as funções DLL do VBA usando a instrução **Declare**. Essa instrução tem uma sintaxe para comandos e uma para funções.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p103">You can access DLL functions and commands in VBA by using the **Declare** statement. This statement has one syntax for commands and one for functions.</span></span> 
  
- <span data-ttu-id="d4ef7-117">**Sintaxe 1 – comandos**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-117">**Syntax 1 - commands**</span></span>
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- <span data-ttu-id="d4ef7-118">**Sintaxe 2 – funções**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-118">**Syntax 2 - functions**</span></span>
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

<span data-ttu-id="d4ef7-p104">As palavras-chave opcionais **Public** e **Private** especificam o escopo da função importada: todo o projeto do Visual Basic ou apenas o módulo do Visual Basic, respectivamente. O nome é aquele que você deseja usar no código VBA. Se for diferente do nome da DLL, você deve usar o especificador de Alias "nomedoalias" e deve fornecer o nome da função como exportado pela DLL. Se quiser acessar uma função DLL por referência para um número ordinal de DLL, você deve fornecer um nome de alias, que é o ordinal precedido por **#**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p104">The optional **Public** and **Private** keywords specify the scope of the imported function: the entire Visual Basic project or just the Visual Basic module, respectively. The name is the name that you want to use in the VBA code. If this differs from the name in the DLL, you must use the Alias "aliasname" specifier, and you should give the name of the function as exported by the DLL. If you want to access a DLL function by reference to a DLL ordinal number, you must provide an alias name, which is the ordinal prefixed by **#**.</span></span>
  
<span data-ttu-id="d4ef7-p105">Os comandos devem retornar **void**. As funções devem retornar tipos que o VBA pode reconhecer **ByVal**. Isso significa que alguns tipos são retornados com maior facilidade ao modificar os argumentos no lugar: cadeias de caracteres, matrizes, objetos e tipos definidos pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p105">Commands should return **void**. Functions should return types that VBA can recognize **ByVal**. This means that some types are more easily returned by modifying arguments in place: strings, arrays, user-defined types, and objects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d4ef7-p106">O VBA não pode verificar se a lista de argumentos e o retorno declarado no módulo do Visual Basic são os mesmos codificados na DLL. Você deve verificar isso sozinho com muito cuidado, pois um erro pode causar uma falha no Excel.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p106">VBA cannot check that the argument list and return stated in the Visual Basic module are the same as coded in the DLL. You should check this yourself very carefully, because a mistake could cause Excel to crash.</span></span> 
  
<span data-ttu-id="d4ef7-p107">Quando os argumentos do comando ou da função não são passados por ponteiro ou referência, devem ser precedidos pela palavra-chave **ByVal** com a declaração **arglist**. Quando uma função C/C++ tem os argumentos de ponteiro ou quando uma função C++ tem os argumentos de referência, eles deveriam passar por **ByRef**. A palavra-chave **ByRef** pode ser omitida das listas de argumentos porque é o padrão no VBA.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p107">When the function or command's arguments are not passed by reference or pointer, they must be preceded by the **ByVal** keyword in the **arglist** declaration. When a C/C++ function takes pointer arguments, or a C++ function takes reference arguments, they should be passed **ByRef**. The keyword **ByRef** can be omitted from argument lists because it is the default in VBA.</span></span> 
  
### <a name="argument-types-in-cc-and-vba"></a><span data-ttu-id="d4ef7-131">Tipos de argumento no C/C++ e no VBA</span><span class="sxs-lookup"><span data-stu-id="d4ef7-131">Argument Types in C/C++ and VBA</span></span>

<span data-ttu-id="d4ef7-132">Você deve observar o seguinte ao comparar as declarações dos tipos de argumentos no C/C++ e VBA.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-132">You should note the following when you compare the declarations of argument types in C/C++ and VBA.</span></span>
  
- <span data-ttu-id="d4ef7-133">Uma **String** do VBA é passada como um ponteiro para uma estrutura BSTR de cadeia de caracteres de bytes quando houver passado por ByVal e como um ponteiro para um ponteiro quando passada por **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-133">A VBA **String** is passed as a pointer to a byte-string BSTR structure when passed ByVal, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="d4ef7-134">Uma **Variant** do VBA que contém uma cadeia de caracteres é passada como um ponteiro para uma estrutura BSTR de cadeia de caracteres largos Unicode quando passada por **ByVal** e como um ponteiro para um ponteiro quando passada por **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-134">A VBA **Variant** that contains a string is passed as a pointer to a Unicode wide-character string BSTR structure when passed **ByVal**, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="d4ef7-135">O **Integer** do VBA é um tipo de 16 bits equivalente a um curto assinado no C/C++.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-135">The VBA **Integer** is a 16-bit type equivalent to a signed short in C/C++.</span></span> 
    
- <span data-ttu-id="d4ef7-136">O **Long** do VBA é um tipo de 32 bits equivalente a um curto assinado no C/C++.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-136">The VBA **Long** is a 32-bit type equivalent to a signed int in C/C++.</span></span> 
    
- <span data-ttu-id="d4ef7-137">O VBA e o C++ permitem a definição de tipos de dados definidos pelo usuário, usando respectivamente as instruções **Type** e **struct**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-137">Both VBA and C/C++ allow the definition of user-defined data types, using the **Type** and **struct** statements respectively.</span></span> 
    
- <span data-ttu-id="d4ef7-138">O VBA e o C++ oferecem suporte ao tipo de dados **Variant**, definido para o C++ nos arquivos de cabeçalho Windows OLE/COM, como VARIANT.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-138">Both VBA and C/C++ support the **Variant** data type, defined for C/C++ in the Windows OLE/COM header files as VARIANT.</span></span> 
    
- <span data-ttu-id="d4ef7-139">As matrizes do VBA são **SafeArrays** OLE, definidas para o C++ nos arquivos de cabeçalho Windows OLE/COM, como **SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-139">VBA arrays are OLE **SafeArrays**, defined for C/C++ in the Windows OLE/COM header files as **SAFEARRAY**.</span></span>
    
- <span data-ttu-id="d4ef7-140">O tipo de dados **Currency** do VBA é passado como uma estrutura de tipo **CY**, definido no arquivo de cabeçalho de Windows wtypes.h, quando passado por **ByVal** e como um ponteiro para isso quando passado por **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-140">The VBA **Currency** data type is passed as a structure of type **CY**, defined in the Windows header file wtypes.h, when passed **ByVal**, and as a pointer to this when passed **ByRef**.</span></span>
    
<span data-ttu-id="d4ef7-141">No VBA, os elementos de dados nos tipos de dados definidos pelo usuário são compactados nos limites de 4 bytes, enquanto no Visual Studio, por padrão, eles são compactados nos limites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-141">In VBA, data elements in user-defined data types are packed to 4-byte boundaries, whereas in Visual Studio, by default, they are packed to 8-byte boundaries.</span></span> <span data-ttu-id="d4ef7-142">Dessa forma, você deve inserir a definição de estrutura do C/C++ em um bloco `#pragma pack(4) … #pragma pack()` para evitar erros de alinhamento de elementos.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-142">Therefore you must enclose the C/C++ structure definition in a  `#pragma pack(4) … #pragma pack()` block to avoid elements being misaligned.</span></span> 
  
<span data-ttu-id="d4ef7-143">A seguir, um exemplo de definições de tipo de usuário equivalentes.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-143">The following is an example of equivalent user type definitions.</span></span>
  
```vb
Type VB_User_Type
    i As Integer
    d As Double
    s As String
End Type

```

```cpp
#pragma pack(4)
struct C_user_type
{
    short iVal;
    double dVal;
    BSTR bstr; // VBA String type is a byte string
}
#pragma pack() // restore default

```

<span data-ttu-id="d4ef7-p109">Em alguns casos, o VBA dá suporte a um intervalo maior de valores do que o Excel. O VBA duplo é compatível com IEEE e dá suporte a números subnormais que atualmente são arredondados para zero na planilha. O tipo **Date** do VBA pode representar datas a partir de 1-Jan-0100 usando datas serializadas negativas. O Excel permite somente datas serializadas maiores ou iguais a zero. O tipo **Date** do VBA, um número inteiro de 64 bits em escala, pode alcançar uma precisão que não tem suporte em 8 bytes duplos e, portanto, não tem correspondência na planilha.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p109">VBA supports a greater range of values in some cases than Excel supports. The VBA double is IEEE compliant, supporting subnormal numbers that are currently rounded down to zero on the worksheet. The VBA **Date** type can represent dates as early as 1-Jan-0100 using negative serialized dates. Excel only allows serialized dates greater than or equal to zero. The VBA **Currency** type—a scaled 64-bit integer—can achieve accuracy not supported in 8-byte doubles, and so is not matched in the worksheet.</span></span> 
  
<span data-ttu-id="d4ef7-149">O Excel somente passa Variants dos seguintes tipos para uma função definida pelo usuário do VBA.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-149">Excel only passes Variants of the following types to a VBA user-defined function.</span></span>
  
|<span data-ttu-id="d4ef7-150">**Tipo de dados do VBA**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-150">**VBA data type**</span></span>|<span data-ttu-id="d4ef7-151">**Sinalizadores de bit do tipo Variant do C/C++**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-151">**C/C++ Variant type bit flags**</span></span>|<span data-ttu-id="d4ef7-152">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-152">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4ef7-153">Duplo</span><span class="sxs-lookup"><span data-stu-id="d4ef7-153">Double</span></span>  <br/> |<span data-ttu-id="d4ef7-154">**VT_R8**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-154">**VT_R8**</span></span> <br/> ||
|<span data-ttu-id="d4ef7-155">Boolean</span><span class="sxs-lookup"><span data-stu-id="d4ef7-155">Boolean</span></span>  <br/> |<span data-ttu-id="d4ef7-156">**VT_BOOL**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-156">**VT_BOOL**</span></span> <br/> ||
|<span data-ttu-id="d4ef7-157">Data</span><span class="sxs-lookup"><span data-stu-id="d4ef7-157">Date</span></span>  <br/> |<span data-ttu-id="d4ef7-158">**VT_DATE**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-158">**VT_DATE**</span></span> <br/> ||
|<span data-ttu-id="d4ef7-159">Cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="d4ef7-159">String</span></span>  <br/> |<span data-ttu-id="d4ef7-160">**VT_BSTR**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-160">**VT_BSTR**</span></span> <br/> |<span data-ttu-id="d4ef7-161">Cadeia de caracteres de byte Bstr OLE</span><span class="sxs-lookup"><span data-stu-id="d4ef7-161">OLE Bstr byte string</span></span>  <br/> |
|<span data-ttu-id="d4ef7-162">Intervalo</span><span class="sxs-lookup"><span data-stu-id="d4ef7-162">Range</span></span>  <br/> |<span data-ttu-id="d4ef7-163">**VT_DISPATCH**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-163">**VT_DISPATCH**</span></span> <br/> |<span data-ttu-id="d4ef7-164">Referências de intervalos e células</span><span class="sxs-lookup"><span data-stu-id="d4ef7-164">Range and cell references</span></span>  <br/> |
|<span data-ttu-id="d4ef7-165">Variant com uma matriz</span><span class="sxs-lookup"><span data-stu-id="d4ef7-165">Variant containing an array</span></span>  <br/> |<span data-ttu-id="d4ef7-166">**VT_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-166">**VT_ARRAY**</span></span> | <span data-ttu-id="d4ef7-167">**VT_VARIANT**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-167">**VT_VARIANT**</span></span> <br/> |<span data-ttu-id="d4ef7-168">Matrizes literais</span><span class="sxs-lookup"><span data-stu-id="d4ef7-168">Literal arrays</span></span>  <br/> |
|<span data-ttu-id="d4ef7-169">Ccy</span><span class="sxs-lookup"><span data-stu-id="d4ef7-169">Ccy</span></span>  <br/> |<span data-ttu-id="d4ef7-170">**VT_CY**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-170">**VT_CY**</span></span> <br/> |<span data-ttu-id="d4ef7-171">Número inteiro de 64 bits dimensionado para permitir 4 casas decimais de precisão.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-171">64-bit integer scaled to permit 4 decimal places of accuracy.</span></span>  <br/> |
|<span data-ttu-id="d4ef7-172">Variant com erro</span><span class="sxs-lookup"><span data-stu-id="d4ef7-172">Variant containing an error</span></span>  <br/> |<span data-ttu-id="d4ef7-173">**VT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-173">**VT_ERROR**</span></span> <br/> ||
||<span data-ttu-id="d4ef7-174">**VT_EMPTY**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-174">**VT_EMPTY**</span></span> <br/> |<span data-ttu-id="d4ef7-175">Argumentos omitidos ou células vazias</span><span class="sxs-lookup"><span data-stu-id="d4ef7-175">Empty cells or omitted arguments</span></span>  <br/> |
   
<span data-ttu-id="d4ef7-p110">Você pode verificar o tipo de uma Variant passada no VBA usando o **VarType**, com a exceção que a função retorna o tipo dos valores de intervalo quando chamado com referências. Para determinar se um **Variant** é um objeto **Range** de referência, você pode usar a função **IsObject**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p110">You can check the type of a passed-in Variant in VBA using the **VarType**, except that the function returns the type of the range's values when called with references. To determine if a **Variant** is a **Range** reference object, you can use the **IsObject** function.</span></span> 
  
<span data-ttu-id="d4ef7-p111">Você pode criar **Variants** que contêm matrizes de variantes do VBA de um **Range** atribuindo suas propriedades **Value** para uma **Variant**. Todas as células no intervalo de origem que são formatadas usando o formato de moeda padrão das configurações regionais em vigor no momento são convertidas em elementos de matriz do tipo **Currency**. Todas as células formatadas como datas são convertidas em elementos de matriz do tipo **Date**. As células que contêm cadeias de caracteres são convertidas em Variants **BSTR** de caracteres largos. As células que contêm erros são convertidas em **Variants** do tipo **VT_ERROR**. As células contendo **Boolean** **True** ou **False** são convertidas em **Variants** do tipo **VT_BOOL**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p111">You can create **Variants** that contain arrays of variants in VBA from a **Range** by assigning its **Value** property to a **Variant**. Any cells in the source range that are formatted using the standard currency format for the regional settings in force at the time are converted to array elements of type **Currency**. Any cells formatted as dates are converted to array elements of type **Date**. Cells containing strings are converted to wide-character **BSTR** Variants. Cells containing errors are converted to **Variants** of type **VT_ERROR**. Cells containing **Boolean** **True** or **False** are converted to **Variants** of type **VT_BOOL**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d4ef7-p112">A **Variant** armazena **True** como -1 e **False** como 0. Os números não formatados, como datas ou valores de moedas, são convertidos em Variants do tipo **VT_R8**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p112">The **Variant** stores **True** as -1 and **False** as 0. Numbers not formatted as dates or currency amounts are converted to Variants of type **VT_R8**.</span></span> 
  
### <a name="variant-and-string-arguments"></a><span data-ttu-id="d4ef7-186">Argumentos de variant ou de cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="d4ef7-186">Variant and String Arguments</span></span>

<span data-ttu-id="d4ef7-p113">O Excel funciona internamente com cadeias de caracteres Unicode de caracteres largos. Quando se declara que uma função definida pelo usuário do VBA obtém um argumento **String**, o Excel converte a cadeia de caracteres fornecida em uma cadeia de caracteres de bytes em forma específica do local. Se quiser que a função seja passada em uma cadeia de caracteres Unicode, a função definida pelo usuário do VBA deve aceitar um argumento **Variant**, em vez de um **String**. A função DLL pode aceitar aquela **Variant** da cadeia de caracteres larga de BSTR do VBA.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p113">Excel works internally with wide-character Unicode strings. When a VBA user-defined function is declared as taking a **String** argument, Excel converts the supplied string to a byte-string in a locale-specific way. If you want your function to be passed a Unicode string, your VBA user-defined function should accept a **Variant** instead of a **String** argument. Your DLL function can then accept that **Variant** BSTR wide-character string from VBA.</span></span> 
  
<span data-ttu-id="d4ef7-p114">Para retornar cadeias de caracteres Unicode de uma DLL para o VBA, você deve modificar um argumento de cadeia de caracteres **Variant** no local. Para fazer isto, declare a função DLL como fazendo um ponteiro para a **Variant** e no seu código C/C++, e declare o argumento no código VBA como `ByRef varg As Variant`. A memória da cadeia de caracteres antiga deve ser liberada e o novo valor da cadeia de caracteres deve ser criado usando a as funções de cadeia de caracteres OLE Bstr somente na DLL.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p114">To return Unicode strings to VBA from a DLL, you should modify a **Variant** string argument in place. For this to work, you must declare the DLL function as taking a pointer to the **Variant** and in your C/C++ code, and declare the argument in the VBA code as  `ByRef varg As Variant`. The old string memory should be released, and the new string value created by using the OLE Bstr string functions only in the DLL.</span></span>
  
<span data-ttu-id="d4ef7-p115">Para retornar uma cadeia de caracteres de bytes em VBA de uma DLL, você deve modificar um argumento BSTR da cadeia de caracteres de bytes no local. Para fazer isto, você deve declarar a função DLL como fazendo um ponteiro para um ponteiro para o BSTR e no seu código C/C++, e declarar o argumentos no código VBA como ' **ByRef varg As String**'.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p115">To return a byte string to VBA from a DLL, you should modify a byte-string BSTR argument in place. For this to work, you must declare the DLL function as taking a pointer to a pointer to the BSTR and in your C/C++ code, and declare the argument in the VBA code as ' **ByRef varg As String**'.</span></span>
  
<span data-ttu-id="d4ef7-p116">Você só deve manusear as cadeias de caracteres que são passadas dessa maneira do VBA usando as funções de cadeia de caracteres BSTR OLE para evitar problemas de memória. Por exemplo, você deverá chamar **SysFreeString** para liberar a memória antes de sobrescrever a cadeia de caracteres passada, e **SysAllocStringByteLen** ou **SysAllocStringLen** para alocar espaço para uma nova cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p116">You should only handle strings that are passed in these ways from VBA using the OLE BSTR string functions to avoid memory-related problems. For example, you must call **SysFreeString** to free the memory before overwriting the passed in string, and **SysAllocStringByteLen** or **SysAllocStringLen** to allocate space for a new string.</span></span> 
  
<span data-ttu-id="d4ef7-p117">Você pode criar erros de planilha do Excel como **Variants** em VBA usando a função **CVerr** com argumentos, como mostrado na tabela a seguir. Os erros de planilha também podem ser retornados em VBA para uma DLL que usa **Variants** do tipo **VT_ERROR** e com os seguintes valores no campo **ulVal**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p117">You can create Excel worksheet errors as **Variants** in VBA by using the **CVerr** function with arguments as shown in the following table. Worksheet errors can also be returned to VBA from a DLL using **Variants** of type **VT_ERROR**, and with the following values in the **ulVal** field.</span></span> 
  
|<span data-ttu-id="d4ef7-200">**Erro**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-200">**Error**</span></span>|<span data-ttu-id="d4ef7-201">**Valor da Variant ulVal**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-201">**Variant ulVal value**</span></span>|<span data-ttu-id="d4ef7-202">**Argumento CVerr**</span><span class="sxs-lookup"><span data-stu-id="d4ef7-202">**CVerr argument**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d4ef7-203">#NULL!</span><span class="sxs-lookup"><span data-stu-id="d4ef7-203">#NULL!</span></span>  <br/> |<span data-ttu-id="d4ef7-204">2148141008</span><span class="sxs-lookup"><span data-stu-id="d4ef7-204">2148141008</span></span>  <br/> |<span data-ttu-id="d4ef7-205">2000</span><span class="sxs-lookup"><span data-stu-id="d4ef7-205">Windows 2000</span></span>  <br/> |
|<span data-ttu-id="d4ef7-206">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="d4ef7-206">#DIV/0!</span></span>  <br/> |<span data-ttu-id="d4ef7-207">2148141015</span><span class="sxs-lookup"><span data-stu-id="d4ef7-207">2148141015</span></span>  <br/> |<span data-ttu-id="d4ef7-208">2007</span><span class="sxs-lookup"><span data-stu-id="d4ef7-208">Word 2007</span></span>  <br/> |
|<span data-ttu-id="d4ef7-209">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="d4ef7-209">#VALUE!</span></span>  <br/> |<span data-ttu-id="d4ef7-210">2148141023</span><span class="sxs-lookup"><span data-stu-id="d4ef7-210">2148141023</span></span>  <br/> |<span data-ttu-id="d4ef7-211">2015</span><span class="sxs-lookup"><span data-stu-id="d4ef7-211">September 2015</span></span>  <br/> |
|<span data-ttu-id="d4ef7-212">#REF!</span><span class="sxs-lookup"><span data-stu-id="d4ef7-212">#REF!</span></span>  <br/> |<span data-ttu-id="d4ef7-213">2148141031</span><span class="sxs-lookup"><span data-stu-id="d4ef7-213">2148141031</span></span>  <br/> |<span data-ttu-id="d4ef7-214">2023</span><span class="sxs-lookup"><span data-stu-id="d4ef7-214">2023</span></span>  <br/> |
|<span data-ttu-id="d4ef7-215">#NAME?</span><span class="sxs-lookup"><span data-stu-id="d4ef7-215">#NAME?</span></span>  <br/> |<span data-ttu-id="d4ef7-216">2148141037</span><span class="sxs-lookup"><span data-stu-id="d4ef7-216">2148141037</span></span>  <br/> |<span data-ttu-id="d4ef7-217">2029</span><span class="sxs-lookup"><span data-stu-id="d4ef7-217">2029</span></span>  <br/> |
|<span data-ttu-id="d4ef7-218">#NUM!</span><span class="sxs-lookup"><span data-stu-id="d4ef7-218">#NUM!</span></span>  <br/> |<span data-ttu-id="d4ef7-219">2148141044</span><span class="sxs-lookup"><span data-stu-id="d4ef7-219">2148141044</span></span>  <br/> |<span data-ttu-id="d4ef7-220">2036</span><span class="sxs-lookup"><span data-stu-id="d4ef7-220">2036</span></span>  <br/> |
|<span data-ttu-id="d4ef7-221">#N/A</span><span class="sxs-lookup"><span data-stu-id="d4ef7-221">#N/A</span></span>  <br/> |<span data-ttu-id="d4ef7-222">2148141050</span><span class="sxs-lookup"><span data-stu-id="d4ef7-222">2148141050</span></span>  <br/> |<span data-ttu-id="d4ef7-223">2042</span><span class="sxs-lookup"><span data-stu-id="d4ef7-223">2042</span></span>  <br/> |
   
<span data-ttu-id="d4ef7-224">Observe que o valor fornecido de Variant **ulVal** é equivalente ao valor do argumento **CVerr** mais o hexadecimal x800A0000.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-224">Note that the Variant **ulVal** value given is equivalent to the **CVerr** argument value plus x800A0000 hexadecimal.</span></span> 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a><span data-ttu-id="d4ef7-225">Como chamar funções DLL diretamente da planilha</span><span class="sxs-lookup"><span data-stu-id="d4ef7-225">Calling DLL Functions Directly from the Worksheet</span></span>

<span data-ttu-id="d4ef7-p118">Não é possível acessar as funções Win32 DLL da planilha sem, por exemplo, usar o VBA ou XLM como interfaces, ou sem informar o Excel com antecedência sobre o tipo de função, seus argumentos e o tipo de retorno. Esse processo é chamado de registro.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p118">You cannot access Win32 DLL functions from the worksheet without, for example, using VBA or XLM as interfaces, or without letting Excel know about the function, its arguments, and its return type in advance. The process of doing this is called registration.</span></span>
  
<span data-ttu-id="d4ef7-228">Veja a seguir as maneiras para acessar as funções de uma DLL na planilha:</span><span class="sxs-lookup"><span data-stu-id="d4ef7-228">The ways in which the functions of a DLL can be accessed in the worksheet are as follows:</span></span>
  
- <span data-ttu-id="d4ef7-229">Declare a função em VBA, como descrito anteriormente, e acesse-a por meio de uma função VBA definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-229">Declare the function in VBA as described previously and access it via a VBA user-defined function.</span></span>
    
- <span data-ttu-id="d4ef7-230">Chame a função DLL usando CALL em uma planilha de macro XLM e acesse-a por uma função XLM definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-230">Call the DLL function using CALL on an XLM macro sheet, and access it via an XLM user-defined function.</span></span>
    
- <span data-ttu-id="d4ef7-231">Use um comando XLM ou VBA para chamar a função XLM **REGISTER**, que fornece as informações que o Excel precisa para reconhecer a função quando ela é inserida em uma célula da planilha.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-231">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information that Excel needs to recognize the function when it is entered into a worksheet cell.</span></span> 
    
- <span data-ttu-id="d4ef7-232">Transforme a DLL em um XLL e registre a função usando a função API de C **xlfRegister** quando o XLL estiver ativado.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-232">Turn the DLL into an XLL and register the function using the C API **xlfRegister** function when the XLL is activated.</span></span> 
    
<span data-ttu-id="d4ef7-p119">A quarta abordagem é autocontida: o código que registra as funções e o código da função estão contidos no mesmo projeto de código. Fazer alterações no suplemento não inclui fazer alterações em uma planilha XLM ou em um módulo de código do VBA. Para fazer isso de maneira bem gerenciada enquanto permanece dentro dos recursos da API de C, é necessário transformar a DLL em um XLL e carregar o suplemento resultante usando o Gerenciador de Suplemento, o que permite que o Excel chame uma função exposta pelo seu DLL quando o suplemento é carregado ou ativado, na qual você pode registrar todas as funções contidas na sua XLL e executar qualquer outra inicialização de DLL.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p119">The fourth approach is self-contained: the code that registers the functions and the function code are both contained in the same code project. Making changes to the add-in does not involve making changes to an XLM sheet or to a VBA code module. To do this in a well-managed way while still staying within the capabilities of the C API, you must turn your DLL into an XLL and load the resulting add-in by using the Add-in Manager. This enables Excel to call a function that your DLL exposes when the add-in is loaded or activated, from which you can register all of the functions your XLL contains, and carry out any other DLL initialization.</span></span>
  
## <a name="calling-dll-commands-directly-from-excel"></a><span data-ttu-id="d4ef7-237">Chamando comandos de DLL diretamente do Excel</span><span class="sxs-lookup"><span data-stu-id="d4ef7-237">Calling DLL Commands Directly from Excel</span></span>

<span data-ttu-id="d4ef7-238">Os comandos Win32 DLL não são acessíveis diretamente nos menus e caixas de diálogo do Excel sem a existência de uma interface, como o VBA, ou sem os comandos serem registrados com antecedência.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-238">Win32 DLL commands are not accessible directly from Excel dialog boxes and menus without there being an interface, such as VBA, or without the commands being registered in advance.</span></span>
  
<span data-ttu-id="d4ef7-239">Estas são as maneiras para acessar os comandos de uma DLL:</span><span class="sxs-lookup"><span data-stu-id="d4ef7-239">The ways in which you can access the commands of a DLL are as follows:</span></span>
  
- <span data-ttu-id="d4ef7-240">Declare o comando no VBA como descrito anteriormente e acesse-o por meio de uma macro do VBA.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-240">Declare the command in VBA as described previously and access it via a VBA macro.</span></span>
    
- <span data-ttu-id="d4ef7-241">Chame o comando da DLL usando **CALL** em uma folha de macros XLM e acesse-o por meio de uma macro XLM.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-241">Call the DLL command using **CALL** on an XLM macro sheet, and access it via an XLM macro.</span></span> 
    
- <span data-ttu-id="d4ef7-242">Use um comando XLM ou VBA para chamar a função de XLM **REGISTER**, que fornece as informações que o Excel precisa para reconhecer o comando quando ele é inserido na caixa de diálogo que espera o nome de um comando de macro.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-242">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information Excel needs to recognize the command when it is entered into a dialog box that expects the name of a macro command.</span></span> 
    
- <span data-ttu-id="d4ef7-243">Transforme a DLL em XLL e registre o comando usando a função API de C **xlfRegister**.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-243">Turn the DLL into an XLL and register the command using the C API **xlfRegister** function.</span></span> 
    
<span data-ttu-id="d4ef7-p120">Como discutido anteriormente no contexto das funções DLL, a quarta abordagem é a mais autocontida, mantendo o código de registro parecido com o código de comando. Para isso, você deve transformar a DLL em um XLL e carregar o suplemento resultante usando o Gerenciador de Suplemento. Registrar os comandos dessa maneira também permite anexar o comando a um elemento da interface do usuário, como um menu personalizado, ou configurar um ajuste de registro de evento que chama o comando em um determinado pressionamento de tecla ou outro evento.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p120">As discussed earlier in the context of DLL functions, the fourth approach is the most self-contained, keeping the registration code close to the command code. To do this, you must turn your DLL into an XLL and load the resulting add-in using the Add-in Manager. Registering commands in this way also lets you attach the command to an element of the user interface, such as a custom menu, or to set up an event trap that calls the command on a given keystroke or other event.</span></span>
  
<span data-ttu-id="d4ef7-247">Todos os comandos do XLL registrados com o Excel são considerados pelo Excel da forma a seguir.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-247">All XLL commands that are registered with Excel are assumed by Excel to be of the following form.</span></span>
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> <span data-ttu-id="d4ef7-p121">O Excel ignora o valor de retorno, a menos que ele seja chamado de uma planilha de macro XLM; neste caso, o valor de retorno é convertido para **TRUE** ou **FALSE**. Portanto, você deve retornar 1 se o comando foi executado com sucesso e 0 se falhou ou foi cancelado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p121">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span> 
  
## <a name="dll-memory-and-multiple-dll-instances"></a><span data-ttu-id="d4ef7-250">Memória de DLL e várias instâncias de DLL</span><span class="sxs-lookup"><span data-stu-id="d4ef7-250">DLL Memory and Multiple DLL Instances</span></span>

<span data-ttu-id="d4ef7-p122">Quando um aplicativo carrega uma DLL, o código executável da DLL é carregado na pilha global para que possa ser executado e o espaço é alocado na pilha global das suas estruturas de dados. O Windows usa o mapeamento de memória para fazer com que essas áreas de memória apareçam como se estivessem no processo do aplicativo para que o aplicativo possa acessá-las.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p122">When an application loads a DLL, the DLL's executable code is loaded into the global heap so that it can be run, and space is allocated on the global heap for its data structures. Windows uses memory mapping to make these areas of memory appear as if they are in the application's process so that the application can access them.</span></span>
  
<span data-ttu-id="d4ef7-p123">Se um segundo aplicativo em seguida carrega a DLL, o Windows não faz outra cópia do código executável de DLL, pois essa memória é somente leitura. O Windows mapeia a memória de códigos executáveis DLL para os processos dos dois aplicativos, mas aloca um segundo espaço para uma cópia particular das estruturas de dados da DLL e mapeia esta cópia ao segundo processo. Isso garante que nenhum aplicativo possa interferir nos dados de DLL dos outros.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p123">If a second application then loads the DLL, Windows does not make another copy of the DLL executable code, as that memory is read-only. Windows maps the DLL executable code memory to the processes of both applications. It does, however, allocate a second space for a private copy of the DLL's data structures and maps this copy to the second process only. This ensures that neither application can interfere with the DLL data of the other.</span></span>
  
<span data-ttu-id="d4ef7-p124">Ou seja, os desenvolvedores DLL não precisam se preocupar com as variáveis globais e estáticas, e as estruturas de dados acessadas por mais de um aplicativo ou mais de uma instância do mesmo aplicativo. Todas as instâncias de todos os aplicativos obtêm sua própria cópia dos dados da DLL.</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p124">This means that DLL developers do not have to be concerned about static and global variables and data structures being accessed by more than one application, or more than one instance of the same application. Every instance of every application gets its own copy of the DLL's data.</span></span>
  
<span data-ttu-id="d4ef7-p125">Os desenvolvedores de DLL precisam se preocupar com a mesma instância de um aplicativo chamando sua DLL várias vezes de threads diferentes, porque isso pode resultar em contenção dos dados dessa instância. Para saber mais, confira [Gerenciamento de memória no Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="d4ef7-p125">DLL developers do need to be concerned about the same instance of an application calling their DLL many times from different threads, because this can result in contention for that instance's data. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d4ef7-261">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4ef7-261">See also</span></span>

- [<span data-ttu-id="d4ef7-262">Desenvolver DLLs</span><span class="sxs-lookup"><span data-stu-id="d4ef7-262">Developing DLLs</span></span>](developing-dlls.md) 
- [<span data-ttu-id="d4ef7-263">Calling into Excel from the DLL or XLL</span><span class="sxs-lookup"><span data-stu-id="d4ef7-263">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)

