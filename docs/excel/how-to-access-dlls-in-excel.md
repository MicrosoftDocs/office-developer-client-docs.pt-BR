---
title: Acesso DLLs no Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- accessing dlls [excel 2007],DLLs [Excel 2007], accessing in Excel
localization_priority: Normal
ms.assetid: e2bfd6ea-efa3-45c1-a5b8-2ccb8650c6ab
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: bfb562b6bbe824124c6b5a691745d076720ee004
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765376"
---
# <a name="access-dlls-in-excel"></a><span data-ttu-id="3f77a-104">Acesso DLLs no Excel</span><span class="sxs-lookup"><span data-stu-id="3f77a-104">Access DLLs in Excel</span></span>

<span data-ttu-id="3f77a-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="3f77a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="3f77a-106">Voc� pode acessar uma fun��o ou um comando DLL no Microsoft Excel de diversas maneiras:</span><span class="sxs-lookup"><span data-stu-id="3f77a-106">You can access a DLL function or command in Microsoft Excel in several ways:</span></span>
  
- <span data-ttu-id="3f77a-107">Por meio de um m�dulo de c�digo do Microsoft Visual Basic for Applications (VBA) no qual a fun��o ou o comando foi disponibilizado usando uma instru��o **Declare**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-107">Through a Microsoft Visual Basic for Applications (VBA) code module in which the function or command has been made available using a **Declare** statement.</span></span> 
    
- <span data-ttu-id="3f77a-108">Por meio de uma folha de macro XLM usando as fun��es **CALL** ou **REGISTER**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-108">Through an XLM macro sheet by using the **CALL** or **REGISTER** functions.</span></span> 
    
- <span data-ttu-id="3f77a-109">Diretamente da planilha ou de um item personalizado na interface do usu�rio (IU).</span><span class="sxs-lookup"><span data-stu-id="3f77a-109">Directly from the worksheet or from a customized item in the user interface (UI).</span></span>
    
<span data-ttu-id="3f77a-p101">Esta documenta��o n�o aborda as fun��es XLM. � recomend�vel que voc� use uma das duas outras abordagens.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p101">This documentation does not cover XLM functions. It is recommended that you use either of the other two approaches.</span></span>
  
<span data-ttu-id="3f77a-p102">Para ser acessada diretamente da planilha ou de um item personalizado na IU, primeiro a fun��o ou o comando dever�o ser registrados no Excel. Para saber mais sobre o registro de comandos e de fun��es, consulte [Accessing XLL Code in Excel](accessing-xll-code-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="3f77a-p102">To be accessed directly from the worksheet or from a customized item in the UI, the function or command must first be registered with Excel. For information about registering commands and functions, see [Accessing XLL Code in Excel](accessing-xll-code-in-excel.md).</span></span>
  
## <a name="calling-dll-functions-and-commands-from-vba"></a><span data-ttu-id="3f77a-114">Chamando funções DLL e comandos do VBA</span><span class="sxs-lookup"><span data-stu-id="3f77a-114">Calling DLL functions and commands from VBA</span></span>

<span data-ttu-id="3f77a-p103">Voc� pode acessar fun��es e comandos DLL no VBA usando a instru��o **Declare**. Essa instru��o tem uma sintaxe para os comandos e outra para as fun��es.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p103">You can access DLL functions and commands in VBA by using the **Declare** statement. This statement has one syntax for commands and one for functions.</span></span> 
  
- <span data-ttu-id="3f77a-117">**Sintaxe 1 � comandos**</span><span class="sxs-lookup"><span data-stu-id="3f77a-117">**Syntax 1 - commands**</span></span>
    
  ```vb
  [Public | Private] Declare Sub name Lib "libname" [Alias "aliasname"] [([arglist])]
  ```

- <span data-ttu-id="3f77a-118">**Sintaxe 2 � fun��es**</span><span class="sxs-lookup"><span data-stu-id="3f77a-118">**Syntax 2 - functions**</span></span>
    
  ```vb
  [Public | Private] Declare Function name Lib "libname" [Alias "aliasname"] [([arglist])] [As type]
  ```

<span data-ttu-id="3f77a-p104">As palavras-chave **Public** e **Private** especificam o escopo da fun��o importada: o projeto inteiro do Visual Basic ou apenas o m�dulo do Visual Basic, respectivamente. O nome � o que voc� deseja usar no c�digo VBA. Se ele for diferente do nome na DLL, ser� necess�rio usar o especificador "nomedoalias" do Alias e nomear a fun��o como exportada pela DLL. Se voc� quiser acessar uma fun��o de DLL por refer�ncia a um n�mero ordinal de DLL, dever� fornecer um nome de alias, que � o ordinal com o prefixo **#**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p104">The optional **Public** and **Private** keywords specify the scope of the imported function: the entire Visual Basic project or just the Visual Basic module, respectively. The name is the name that you want to use in the VBA code. If this differs from the name in the DLL, you must use the Alias "aliasname" specifier, and you should give the name of the function as exported by the DLL. If you want to access a DLL function by reference to a DLL ordinal number, you must provide an alias name, which is the ordinal prefixed by **#**.</span></span>
  
<span data-ttu-id="3f77a-p105">Os comandos devem retornar **void**. As fun��es devem retornar tipos que o VBA possa reconhecer **ByVal**. Isso significa que alguns tipos s�o retornados com mais facilidade pela modifica��o dos argumentos existentes: cadeias de caracteres, matrizes, tipos definidos pelo usu�rio e objetos.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p105">Commands should return **void**. Functions should return types that VBA can recognize **ByVal**. This means that some types are more easily returned by modifying arguments in place: strings, arrays, user-defined types, and objects.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3f77a-p106">O VBA n�o pode verificar se a lista de argumentos e os estados retornados no m�dulo do Visual Basic s�o iguais aos codificados na DLL. Verifique isso com muito cuidado, pois um erro pode causar uma falha no Excel.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p106">VBA cannot check that the argument list and return stated in the Visual Basic module are the same as coded in the DLL. You should check this yourself very carefully, because a mistake could cause Excel to crash.</span></span> 
  
<span data-ttu-id="3f77a-p107">Quando os argumentos da fun��o ou do comando n�o forem passados por refer�ncia ou por ponteiro, dever�o ser precedidos pela palavra-chave **ByVal** na declara��o **arglist**. Quando uma fun��o C/C++ obtiver argumentos do ponteiro, ou quando uma fun��o C++ obtiver argumentos de refer�ncia, dever�o ser passados **ByRef**. A palavra-chave **ByRef** pode ser omitida das listas de argumentos porque � o padr�o no VBA.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p107">When the function or command's arguments are not passed by reference or pointer, they must be preceded by the **ByVal** keyword in the **arglist** declaration. When a C/C++ function takes pointer arguments, or a C++ function takes reference arguments, they should be passed **ByRef**. The keyword **ByRef** can be omitted from argument lists because it is the default in VBA.</span></span> 
  
### <a name="argument-types-in-cc-and-vba"></a><span data-ttu-id="3f77a-131">Tipos de argumento em C/C++ e VBA</span><span class="sxs-lookup"><span data-stu-id="3f77a-131">Argument types in C/C++ and VBA</span></span>

<span data-ttu-id="3f77a-132">Voc� deve observar o seguinte ao comparar as declara��es de tipos de argumento no C/C++ e no VBA.</span><span class="sxs-lookup"><span data-stu-id="3f77a-132">You should note the following when you compare the declarations of argument types in C/C++ and VBA.</span></span>
  
- <span data-ttu-id="3f77a-133">Uma **String** do VBA � passada como um ponteiro para uma estrutura BSTR byte-cadeia de caracteres quando passada ByVal e como um ponteiro para um ponteiro quando passada **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-133">A VBA **String** is passed as a pointer to a byte-string BSTR structure when passed ByVal, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="3f77a-134">Uma **Variant** do VBA que cont�m uma cadeia de caracteres � passada como um ponteiro para uma cadeia de caracteres de caractere largo Unicode usando a estrutura BSTR quando passada **ByVal** e como um ponteiro para um ponteiro quando passada **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-134">A VBA **Variant** that contains a string is passed as a pointer to a Unicode wide-character string BSTR structure when passed **ByVal**, and as a pointer to a pointer when passed **ByRef**.</span></span>
    
- <span data-ttu-id="3f77a-135">O **Integer** do VBA � um equivalente do tipo de 16 bits para um signed short no C/C++.</span><span class="sxs-lookup"><span data-stu-id="3f77a-135">The VBA **Integer** is a 16-bit type equivalent to a signed short in C/C++.</span></span> 
    
- <span data-ttu-id="3f77a-136">O **Long** do VBA � um tipo de 32 bits equivalente a um signed int no C/C++.</span><span class="sxs-lookup"><span data-stu-id="3f77a-136">The VBA **Long** is a 32-bit type equivalent to a signed int in C/C++.</span></span> 
    
- <span data-ttu-id="3f77a-137">O VBA e o C/C++ permitem a defini��o de tipos de dados definidos pelo usu�rio usando as instru��es **Type** e **struct**, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="3f77a-137">Both VBA and C/C++ allow the definition of user-defined data types, using the **Type** and **struct** statements respectively.</span></span> 
    
- <span data-ttu-id="3f77a-138">O VBA e o C/C++ d�o suporte ao tipo de dados **Variant**, definido para o C/C++ nos arquivos de cabe�alho do OLE/COM do Windows como VARIANT.</span><span class="sxs-lookup"><span data-stu-id="3f77a-138">Both VBA and C/C++ support the **Variant** data type, defined for C/C++ in the Windows OLE/COM header files as VARIANT.</span></span> 
    
- <span data-ttu-id="3f77a-139">As matrizes do VBA s�o **SafeArrays** OLE, definidos para o C/C++ no arquivo de cabe�alho OLE/COM do Windows como **SAFEARRAY**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-139">VBA arrays are OLE **SafeArrays**, defined for C/C++ in the Windows OLE/COM header files as **SAFEARRAY**.</span></span>
    
- <span data-ttu-id="3f77a-140">O tipo de dados **Currency** do VBA � passado como uma estrutura do tipo **CY**, definida no arquivo de cabe�alho wtypes.h do Windows, quando passado **ByVal**, e como um ponteiro para ponteiro para isso quando passado **ByRef**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-140">The VBA **Currency** data type is passed as a structure of type **CY**, defined in the Windows header file wtypes.h, when passed **ByVal**, and as a pointer to this when passed **ByRef**.</span></span>
    
<span data-ttu-id="3f77a-141">No VBA, os elementos de dados em tipos de dados definidos pelo usu�rio s�o empacotados em limites de 4 bytes, enquanto que, no Visual Studio, por padr�o, eles s�o empacotados em limites de 8 bytes.</span><span class="sxs-lookup"><span data-stu-id="3f77a-141">In VBA, data elements in user-defined data types are packed to 4-byte boundaries, whereas in Visual Studio, by default, they are packed to 8-byte boundaries.</span></span> <span data-ttu-id="3f77a-142">Portanto, você deve colocar a definição da estrutura de C/C++ em um `#pragma pack(4) … #pragma pack()` bloco para evitar elementos sendo fora de alinhamento.</span><span class="sxs-lookup"><span data-stu-id="3f77a-142">Therefore you must enclose the C/C++ structure definition in a `#pragma pack(4) … #pragma pack()` block to avoid elements being misaligned.</span></span> 
  
<span data-ttu-id="3f77a-143">A seguir, um exemplo de defini��es de tipo de usu�rio equivalentes.</span><span class="sxs-lookup"><span data-stu-id="3f77a-143">The following is an example of equivalent user type definitions.</span></span>
  
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

<span data-ttu-id="3f77a-p109">O VBA d� suporte a uma s�rie de valores maior em alguns casos ao que o Excel consegue dar suporte. O double do VBA � compat�vel com IEEE, dando suporte a n�meros subnormais atualmente arredondados para baixo para zero na planilha. O tipo **Date** do VBA pode representar datas desde 1-Jan-0100 usando datas serializadas negativas. O Excel s� permite datas serializadas maiores ou iguais a zero. O tipo **Currency** do VBA � um inteiro de 64 bits dimensionado � pode obter precis�o sem suporte em doubles de 8 bytes e, portanto, n�o tem correspond�ncia na planilha.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p109">VBA supports a greater range of values in some cases than Excel supports. The VBA double is IEEE compliant, supporting subnormal numbers that are currently rounded down to zero on the worksheet. The VBA **Date** type can represent dates as early as 1-Jan-0100 using negative serialized dates. Excel only allows serialized dates greater than or equal to zero. The VBA **Currency** type—a scaled 64-bit integer—can achieve accuracy not supported in 8-byte doubles, and so is not matched in the worksheet.</span></span> 
  
<span data-ttu-id="3f77a-149">O Excel s� passa Variants dos tipos a seguir para uma fun��o definida pelo usu�rio do VBA.</span><span class="sxs-lookup"><span data-stu-id="3f77a-149">Excel only passes Variants of the following types to a VBA user-defined function.</span></span>
  
|<span data-ttu-id="3f77a-150">**Tipo de dados do VBA**</span><span class="sxs-lookup"><span data-stu-id="3f77a-150">**VBA data type**</span></span>|<span data-ttu-id="3f77a-151">**Sinalizadores de bit do tipo Variant do C/C++**</span><span class="sxs-lookup"><span data-stu-id="3f77a-151">**C/C++ Variant type bit flags**</span></span>|<span data-ttu-id="3f77a-152">**Descri��o**</span><span class="sxs-lookup"><span data-stu-id="3f77a-152">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f77a-153">Double</span><span class="sxs-lookup"><span data-stu-id="3f77a-153">Double</span></span>  <br/> |<span data-ttu-id="3f77a-154">**VT_R8**</span><span class="sxs-lookup"><span data-stu-id="3f77a-154">**VT_R8**</span></span> <br/> ||
|<span data-ttu-id="3f77a-155">Booliano</span><span class="sxs-lookup"><span data-stu-id="3f77a-155">Boolean</span></span>  <br/> |<span data-ttu-id="3f77a-156">**VT_BOOL**</span><span class="sxs-lookup"><span data-stu-id="3f77a-156">**VT_BOOL**</span></span> <br/> ||
|<span data-ttu-id="3f77a-157">Data</span><span class="sxs-lookup"><span data-stu-id="3f77a-157">Date</span></span>  <br/> |<span data-ttu-id="3f77a-158">**VT_DATE**</span><span class="sxs-lookup"><span data-stu-id="3f77a-158">**VT_DATE**</span></span> <br/> ||
|<span data-ttu-id="3f77a-159">String</span><span class="sxs-lookup"><span data-stu-id="3f77a-159">String</span></span>  <br/> |<span data-ttu-id="3f77a-160">**VT_BSTR**</span><span class="sxs-lookup"><span data-stu-id="3f77a-160">**VT_BSTR**</span></span> <br/> |<span data-ttu-id="3f77a-161">Cadeia de caracteres de byte Bstr OLE</span><span class="sxs-lookup"><span data-stu-id="3f77a-161">OLE Bstr byte string</span></span>  <br/> |
|<span data-ttu-id="3f77a-162">Intervalo</span><span class="sxs-lookup"><span data-stu-id="3f77a-162">Range</span></span>  <br/> |<span data-ttu-id="3f77a-163">**VT_DISPATCH**</span><span class="sxs-lookup"><span data-stu-id="3f77a-163">**VT_DISPATCH**</span></span> <br/> |<span data-ttu-id="3f77a-164">Refer�ncias de intervalo e de c�lula</span><span class="sxs-lookup"><span data-stu-id="3f77a-164">Range and cell references</span></span>  <br/> |
|<span data-ttu-id="3f77a-165">Variant com uma matriz</span><span class="sxs-lookup"><span data-stu-id="3f77a-165">Variant containing an array</span></span>  <br/> |<span data-ttu-id="3f77a-166">**VT_ARRAY**</span><span class="sxs-lookup"><span data-stu-id="3f77a-166">**VT_ARRAY**</span></span> | <span data-ttu-id="3f77a-167">**VT_VARIANT**</span><span class="sxs-lookup"><span data-stu-id="3f77a-167">**VT_VARIANT**</span></span> <br/> |<span data-ttu-id="3f77a-168">Matrizes literais</span><span class="sxs-lookup"><span data-stu-id="3f77a-168">Literal arrays</span></span>  <br/> |
|<span data-ttu-id="3f77a-169">Ccy</span><span class="sxs-lookup"><span data-stu-id="3f77a-169">Ccy</span></span>  <br/> |<span data-ttu-id="3f77a-170">**VT_CY**</span><span class="sxs-lookup"><span data-stu-id="3f77a-170">**VT_CY**</span></span> <br/> |<span data-ttu-id="3f77a-171">Inteiro de 64 bits dimensionado para permitir quatro casas decimais de precis�o.</span><span class="sxs-lookup"><span data-stu-id="3f77a-171">64-bit integer scaled to permit 4 decimal places of accuracy.</span></span>  <br/> |
|<span data-ttu-id="3f77a-172">Variant com erro</span><span class="sxs-lookup"><span data-stu-id="3f77a-172">Variant containing an error</span></span>  <br/> |<span data-ttu-id="3f77a-173">**VT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="3f77a-173">**VT_ERROR**</span></span> <br/> ||
||<span data-ttu-id="3f77a-174">**VT_EMPTY**</span><span class="sxs-lookup"><span data-stu-id="3f77a-174">**VT_EMPTY**</span></span> <br/> |<span data-ttu-id="3f77a-175">C�lulas vazias ou argumentos omitidos</span><span class="sxs-lookup"><span data-stu-id="3f77a-175">Empty cells or omitted arguments</span></span>  <br/> |
   
<span data-ttu-id="3f77a-p110">Voc� pode verificar o tipo de uma Variant passado no VBA usando o **VarType**, exceto que a fun��o retorna o tipo dos valores do intervalo quando chamado com refer�ncias. Para determinar se uma **Variant** � um objeto de refer�ncia **Range**, voc� poder� usar a fun��o **IsObject**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p110">You can check the type of a passed-in Variant in VBA using the **VarType**, except that the function returns the type of the range's values when called with references. To determine if a **Variant** is a **Range** reference object, you can use the **IsObject** function.</span></span> 
  
<span data-ttu-id="3f77a-p111">Voc� pode criar **Variants** com matrizes de variantes no VBA de um **Range** ao atribuir sua propriedade **Value** a uma **Variant**. Todas as c�lulas no intervalo de origem formatadas como a moeda padr�o para as configura��es regionais em vigor no momento ser�o convertidas em elementos da matriz do tipo **Currency**. Todas as c�lulas formatadas como datas ser�o convertidas em elementos de matriz do tipo **Date**. As c�lulas com cadeias de caracteres ser�o convertidas em Variants **BSTR** de caractere longo. As c�lulas com erros ser�o convertidas em **Variants** do tipo **VT_ERROR**. As c�lulas com **Boolean** **True** ou **False** ser�o convertidas em **Variants** do tipo **VT_BOOL**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p111">You can create **Variants** that contain arrays of variants in VBA from a **Range** by assigning its **Value** property to a **Variant**. Any cells in the source range that are formatted using the standard currency format for the regional settings in force at the time are converted to array elements of type **Currency**. Any cells formatted as dates are converted to array elements of type **Date**. Cells containing strings are converted to wide-character **BSTR** Variants. Cells containing errors are converted to **Variants** of type **VT_ERROR**. Cells containing **Boolean** **True** or **False** are converted to **Variants** of type **VT_BOOL**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3f77a-p112">A **Variant** armazena **True** como �1 e **False** como 0. Os n�meros n�o s�o formatados como datas ou valores monet�rios s�o convertidos em Variants do tipo **VT_R8**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p112">The **Variant** stores **True** as -1 and **False** as 0. Numbers not formatted as dates or currency amounts are converted to Variants of type **VT_R8**.</span></span> 
  
### <a name="variant-and-string-arguments"></a><span data-ttu-id="3f77a-186">Argumentos Variant e a cadeia de caracteres</span><span class="sxs-lookup"><span data-stu-id="3f77a-186">Variant and string arguments</span></span>

<span data-ttu-id="3f77a-p113">O Excel funciona internamente com cadeias de caracteres Unicode de caractere longo. Quando uma fun��o definida pelo usu�rio do VBA � declarada como obtendo um argumento de **String**, o Excel converte a cadeia de caracteres fornecida em uma cadeia de caracteres de byte de uma forma espec�fica da localidade. Se voc� quiser que uma cadeia de caracteres Unicode seja passada para sua fun��o, sua fun��o definida pelo usu�rio do VBA dever� aceitar um argumento de **Variant** em vez de um de **String**. Sua fun��o DLL poder� ent�o aceitar a cadeia de caracteres de caractere longo BSTR **Variant** do VBA.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p113">Excel works internally with wide-character Unicode strings. When a VBA user-defined function is declared as taking a **String** argument, Excel converts the supplied string to a byte-string in a locale-specific way. If you want your function to be passed a Unicode string, your VBA user-defined function should accept a **Variant** instead of a **String** argument. Your DLL function can then accept that **Variant** BSTR wide-character string from VBA.</span></span> 
  
<span data-ttu-id="3f77a-p114">Para retornar cadeias de caracteres Unicode para o VBA de uma DLL, modifique um argumento de cadeia de caracteres **Variant** no local. Para que isso funcione, voc� dever� declarar a fun��o DLL como obtendo um ponteiro para a **Variant** em seu c�digo C/C++ e declarar o argumento no c�digo VBA como  `ByRef varg As Variant`. A mem�ria da cadeia de caracteres antiga dever� ser liberada e o valor da nova cadeia de caracteres criado usando o OLE. A cadeia de caracteres Bstr s� funciona na DLL.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p114">To return Unicode strings to VBA from a DLL, you should modify a **Variant** string argument in place. For this to work, you must declare the DLL function as taking a pointer to the **Variant** and in your C/C++ code, and declare the argument in the VBA code as  `ByRef varg As Variant`. The old string memory should be released, and the new string value created by using the OLE Bstr string functions only in the DLL.</span></span>
  
<span data-ttu-id="3f77a-p115">Para retornar uma cadeia de caracteres de byte para o VBA de uma DLL, voc� dever� modificar um argumento BSTR de cadeia de caracteres de byte existente. Para que isso funcione, voc� dever� declarar a fun��o DLL como obtendo um ponteiro para um ponteiro para o BSTR e em seu c�digo C/C++ e declarar o argumento no c�digo VBA como " **ByRef varg As String**".</span><span class="sxs-lookup"><span data-stu-id="3f77a-p115">To return a byte string to VBA from a DLL, you should modify a byte-string BSTR argument in place. For this to work, you must declare the DLL function as taking a pointer to a pointer to the BSTR and in your C/C++ code, and declare the argument in the VBA code as ' **ByRef varg As String**'.</span></span>
  
<span data-ttu-id="3f77a-p116">Voc� s� deve manipular as cadeias de caracteres passadas dessas maneiras do VBA usando as fun��es de cadeia de caracteres BSTR OLE para evitar problemas relacionados � mem�ria. Por exemplo, ser� necess�rio chamar **SysFreeString** para liberar a mem�ria antes de substituir o que foi passado na cadeia de caracteres e **SysAllocStringByteLen** ou **SysAllocStringLen** para alocar espa�o para uma nova cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p116">You should only handle strings that are passed in these ways from VBA using the OLE BSTR string functions to avoid memory-related problems. For example, you must call **SysFreeString** to free the memory before overwriting the passed in string, and **SysAllocStringByteLen** or **SysAllocStringLen** to allocate space for a new string.</span></span> 
  
<span data-ttu-id="3f77a-p117">Voc� pode criar erros de planilha do Excel como **Variants** no VBA usando a fun��o **CVerr** com argumentos como os mostrados na tabela a seguir. Os erros de planilha tamb�m pode ser retornados para o VBA de uma DLL usando **Variants** do tipo **VT_ERROR** e com os valores a seguir no campo **ulVal**.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p117">You can create Excel worksheet errors as **Variants** in VBA by using the **CVerr** function with arguments as shown in the following table. Worksheet errors can also be returned to VBA from a DLL using **Variants** of type **VT_ERROR**, and with the following values in the **ulVal** field.</span></span> 
  
|<span data-ttu-id="3f77a-200">**Erro**</span><span class="sxs-lookup"><span data-stu-id="3f77a-200">**Error**</span></span>|<span data-ttu-id="3f77a-201">**Valor da Variant ulVal**</span><span class="sxs-lookup"><span data-stu-id="3f77a-201">**Variant ulVal value**</span></span>|<span data-ttu-id="3f77a-202">**Argumento CVerr**</span><span class="sxs-lookup"><span data-stu-id="3f77a-202">**CVerr argument**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3f77a-203">#NULL!</span><span class="sxs-lookup"><span data-stu-id="3f77a-203">#NULL!</span></span>  <br/> |<span data-ttu-id="3f77a-204">2148141008</span><span class="sxs-lookup"><span data-stu-id="3f77a-204">2148141008</span></span>  <br/> |<span data-ttu-id="3f77a-205">2000</span><span class="sxs-lookup"><span data-stu-id="3f77a-205">2000</span></span>  <br/> |
|<span data-ttu-id="3f77a-206">#DIV/0!</span><span class="sxs-lookup"><span data-stu-id="3f77a-206">#DIV/0!</span></span>  <br/> |<span data-ttu-id="3f77a-207">2148141015</span><span class="sxs-lookup"><span data-stu-id="3f77a-207">2148141015</span></span>  <br/> |<span data-ttu-id="3f77a-208">2007</span><span class="sxs-lookup"><span data-stu-id="3f77a-208">2007</span></span>  <br/> |
|<span data-ttu-id="3f77a-209">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="3f77a-209">#VALUE!</span></span>  <br/> |<span data-ttu-id="3f77a-210">2148141023</span><span class="sxs-lookup"><span data-stu-id="3f77a-210">2148141023</span></span>  <br/> |<span data-ttu-id="3f77a-211">2015</span><span class="sxs-lookup"><span data-stu-id="3f77a-211">2015</span></span>  <br/> |
|<span data-ttu-id="3f77a-212">#REF!</span><span class="sxs-lookup"><span data-stu-id="3f77a-212">#REF!</span></span>  <br/> |<span data-ttu-id="3f77a-213">2148141031</span><span class="sxs-lookup"><span data-stu-id="3f77a-213">2148141031</span></span>  <br/> |<span data-ttu-id="3f77a-214">2023</span><span class="sxs-lookup"><span data-stu-id="3f77a-214">2023</span></span>  <br/> |
|<span data-ttu-id="3f77a-215">#NAME?</span><span class="sxs-lookup"><span data-stu-id="3f77a-215">#NAME?</span></span>  <br/> |<span data-ttu-id="3f77a-216">2148141037</span><span class="sxs-lookup"><span data-stu-id="3f77a-216">2148141037</span></span>  <br/> |<span data-ttu-id="3f77a-217">2029</span><span class="sxs-lookup"><span data-stu-id="3f77a-217">2029</span></span>  <br/> |
|<span data-ttu-id="3f77a-218">#NUM!</span><span class="sxs-lookup"><span data-stu-id="3f77a-218">#NUM!</span></span>  <br/> |<span data-ttu-id="3f77a-219">2148141044</span><span class="sxs-lookup"><span data-stu-id="3f77a-219">2148141044</span></span>  <br/> |<span data-ttu-id="3f77a-220">2036</span><span class="sxs-lookup"><span data-stu-id="3f77a-220">2036</span></span>  <br/> |
|<span data-ttu-id="3f77a-221">#N/A</span><span class="sxs-lookup"><span data-stu-id="3f77a-221">#N/A</span></span>  <br/> |<span data-ttu-id="3f77a-222">2148141050</span><span class="sxs-lookup"><span data-stu-id="3f77a-222">2148141050</span></span>  <br/> |<span data-ttu-id="3f77a-223">2042</span><span class="sxs-lookup"><span data-stu-id="3f77a-223">2042</span></span>  <br/> |
   
<span data-ttu-id="3f77a-224">Observe que o valor da Variant **ulVal** dado � equivalente ao valor do argumento de **CVerr** mais x800A0000 hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="3f77a-224">Note that the Variant **ulVal** value given is equivalent to the **CVerr** argument value plus x800A0000 hexadecimal.</span></span> 
  
## <a name="calling-dll-functions-directly-from-the-worksheet"></a><span data-ttu-id="3f77a-225">Chamando funções DLL diretamente a partir de planilha</span><span class="sxs-lookup"><span data-stu-id="3f77a-225">Calling DLL functions directly from the worksheet</span></span>

<span data-ttu-id="3f77a-p118">Voc� n�o pode acessar fun��es DLL Win32 da planilha sem, por exemplo, usar o VBA ou o XLM como interfaces ou sem permitir que o Excel conhe�a a fun��o, seus argumentos e seu tipo de retorno com anteced�ncia. O processo de fazer isso se chama registro.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p118">You cannot access Win32 DLL functions from the worksheet without, for example, using VBA or XLM as interfaces, or without letting Excel know about the function, its arguments, and its return type in advance. The process of doing this is called registration.</span></span>
  
<span data-ttu-id="3f77a-228">As maneiras nas quais as fun��es de uma DLL podem ser acessadas na planilha s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="3f77a-228">The ways in which the functions of a DLL can be accessed in the worksheet are as follows:</span></span>
  
- <span data-ttu-id="3f77a-229">Declare a fun��o no VBA como descrito anteriormente e acesse-a por meio de uma fun��o definida pelo usu�rio do VBA.</span><span class="sxs-lookup"><span data-stu-id="3f77a-229">Declare the function in VBA as described previously and access it via a VBA user-defined function.</span></span>
    
- <span data-ttu-id="3f77a-230">Chame a fun��o DLL usando CALL em uma folha de macro XLM ou acesse-a por meio de uma fun��o definida pelo usu�rio XLM.</span><span class="sxs-lookup"><span data-stu-id="3f77a-230">Call the DLL function using CALL on an XLM macro sheet, and access it via an XLM user-defined function.</span></span>
    
- <span data-ttu-id="3f77a-231">Use um comando XLM ou VBA para chamar a fun��o **REGISTER** XLM, que fornece as informa��es de que o Excel precisa para reconhecer a fun��o quando ela for inserida em uma c�lula de planilha.</span><span class="sxs-lookup"><span data-stu-id="3f77a-231">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information that Excel needs to recognize the function when it is entered into a worksheet cell.</span></span> 
    
- <span data-ttu-id="3f77a-232">Transforme a DLL em um XLL e registre a fun��o usando a fun��o **xlfRegister** da API do C quando o XLL for ativado.</span><span class="sxs-lookup"><span data-stu-id="3f77a-232">Turn the DLL into an XLL and register the function using the C API **xlfRegister** function when the XLL is activated.</span></span> 
    
<span data-ttu-id="3f77a-p119">A quarta abordagem � autocontida: o c�digo que registra as fun��es e o c�digo da fun��o est�o contidos no mesmo projeto de c�digo. Fazer altera��es no suplemento n�o envolve fazer altera��es em uma planilha XLM ou em um m�dulo de c�digo VBA. Para fazer isso de uma maneira bem gerenciada mantendo-se no limite dos recursos da API do C, voc� dever� transformar sua DLL em um XLL e carregar o suplemento resultante usando o Gerenciador de Suplementos. Isso permite que o Excel chame uma fun��o exposta por sua DLL quando o suplemento � carregado ou ativado, a partir do qual voc� poder� registrar todas as fun��es contidas em seu XLL e realizar a inicializa��o de qualquer outra DLL.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p119">The fourth approach is self-contained: the code that registers the functions and the function code are both contained in the same code project. Making changes to the add-in does not involve making changes to an XLM sheet or to a VBA code module. To do this in a well-managed way while still staying within the capabilities of the C API, you must turn your DLL into an XLL and load the resulting add-in by using the Add-in Manager. This enables Excel to call a function that your DLL exposes when the add-in is loaded or activated, from which you can register all of the functions your XLL contains, and carry out any other DLL initialization.</span></span>
  
## <a name="calling-dll-commands-directly-from-excel"></a><span data-ttu-id="3f77a-237">Chamar comandos DLL diretamente do Excel</span><span class="sxs-lookup"><span data-stu-id="3f77a-237">Calling DLL commands directly from Excel</span></span>

<span data-ttu-id="3f77a-238">Os comandos de DLL Win32 n�o podem ser diretamente acessados de caixas de di�logo e de menus do Excel sem que haja uma interface, como o VBA, ou sem o registro pr�vio dos comandos.</span><span class="sxs-lookup"><span data-stu-id="3f77a-238">Win32 DLL commands are not accessible directly from Excel dialog boxes and menus without there being an interface, such as VBA, or without the commands being registered in advance.</span></span>
  
<span data-ttu-id="3f77a-239">As maneiras nas quais voc� pode acessar os comandos de uma DLL s�o as seguintes:</span><span class="sxs-lookup"><span data-stu-id="3f77a-239">The ways in which you can access the commands of a DLL are as follows:</span></span>
  
- <span data-ttu-id="3f77a-240">Declare o comando no VBA como descrito anteriormente e acesse-o por meio de uma macro do VBA.</span><span class="sxs-lookup"><span data-stu-id="3f77a-240">Declare the command in VBA as described previously and access it via a VBA macro.</span></span>
    
- <span data-ttu-id="3f77a-241">Chame o comando da DLL usando **CALL** em uma folha de macros XLM e acesse-o por meio de uma macro XLM.</span><span class="sxs-lookup"><span data-stu-id="3f77a-241">Call the DLL command using **CALL** on an XLM macro sheet, and access it via an XLM macro.</span></span> 
    
- <span data-ttu-id="3f77a-242">Use um comando XLM ou VBA para chamar a fun��o **REGISTER** XLM, que fornece as informa��es de que o Excel precisa para reconhecer o comando quando ele for inserido em uma caixa de di�logo que espere o nome de um comando de macro.</span><span class="sxs-lookup"><span data-stu-id="3f77a-242">Use an XLM or VBA command to call the XLM **REGISTER** function, which provides the information Excel needs to recognize the command when it is entered into a dialog box that expects the name of a macro command.</span></span> 
    
- <span data-ttu-id="3f77a-243">Transforme a DLL em um XLL e registre o comando usando a fun��o **xlfRegister** da API do C.</span><span class="sxs-lookup"><span data-stu-id="3f77a-243">Turn the DLL into an XLL and register the command using the C API **xlfRegister** function.</span></span> 
    
<span data-ttu-id="3f77a-p120">Como discutido anteriormente no contexto de fun��es de DLL, a quarta abordagem � a mais autocontida, mantendo o c�digo de registro pr�ximo ao c�digo do comando. Para fazer isso, voc� deve transformar sua DLL em um XLL e carregar o suplemento resultante usando o Gerenciador de Suplementos. O registro de comandos dessa maneira tamb�m permite que voc� anexe o comando a um elemento da interface do usu�rio, como um menu personalizado ou configure uma intercepta��o de evento que chame o comando em um determinado pressionamento de tecla ou outro evento.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p120">As discussed earlier in the context of DLL functions, the fourth approach is the most self-contained, keeping the registration code close to the command code. To do this, you must turn your DLL into an XLL and load the resulting add-in using the Add-in Manager. Registering commands in this way also lets you attach the command to an element of the user interface, such as a custom menu, or to set up an event trap that calls the command on a given keystroke or other event.</span></span>
  
<span data-ttu-id="3f77a-247">Todos os comandos de XLL registrados no Excel s�o considerados pelo Excel como do formato a seguir.</span><span class="sxs-lookup"><span data-stu-id="3f77a-247">All XLL commands that are registered with Excel are assumed by Excel to be of the following form.</span></span>
  
```cpp
int WINAPI my_xll_cmd(void)
{
// Function code...
    return 1;
}
```

> [!NOTE]
> <span data-ttu-id="3f77a-p121">O Excel ignorar� o valor de retorno, a menos que ele seja chamado de uma folha de macros XLM; nesse caso, o valor de retorno ser� convertido em **TRUE** ou em **FALSE**. Dessa forma, voc� dever� retornar 1 se o seu comando tiver sido executado com �xito e 0 caso ele tenha falhado ou tenha sido cancelado pelo usu�rio.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p121">Excel ignores the return value unless it is called from an XLM macro sheet, in which case the return value is converted to **TRUE** or **FALSE**. You should therefore return 1 if your command executed successfully, and 0 if it failed or was canceled by the user.</span></span> 
  
## <a name="dll-memory-and-multiple-dll-instances"></a><span data-ttu-id="3f77a-250">DLL de memória e várias instâncias DLL</span><span class="sxs-lookup"><span data-stu-id="3f77a-250">DLL memory and multiple DLL instances</span></span>

<span data-ttu-id="3f77a-p122">Quando um aplicativo carrega uma DLL, o c�digo execut�vel da DLL � carregado na pilha global de forma que possa ser executado, e � alocado um espa�o na pilha global para suas estruturas de dados. O Windows usa o mapeamento de mem�ria para fazer com que essas �reas da mem�ria apare�am como se estivessem no processo do aplicativo, de forma que o aplicativo possa acess�-las.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p122">When an application loads a DLL, the DLL's executable code is loaded into the global heap so that it can be run, and space is allocated on the global heap for its data structures. Windows uses memory mapping to make these areas of memory appear as if they are in the application's process so that the application can access them.</span></span>
  
<span data-ttu-id="3f77a-p123">Se um segundo aplicativo carregar a DLL, o Windows n�o far� outra c�pia do c�digo execut�vel da DLL, j� que a mem�ria � somente leitura. O Windows mapeia a mem�ria do c�digo execut�vel da DLL para os processos de ambos os aplicativos. No entanto, ele aloca um segundo espa�o para uma c�pia privada das estruturas de dados da DLL e mapeia essa c�pia apenas para o segundo processo. Isso garante que os aplicativos n�o interfiram nos dados de DLL um do outro.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p123">If a second application then loads the DLL, Windows does not make another copy of the DLL executable code, as that memory is read-only. Windows maps the DLL executable code memory to the processes of both applications. It does, however, allocate a second space for a private copy of the DLL's data structures and maps this copy to the second process only. This ensures that neither application can interfere with the DLL data of the other.</span></span>
  
<span data-ttu-id="3f77a-p124">Isso significa que os desenvolvedores n�o precisa se preocupar com a possibilidade de as vari�veis est�ticas e globais e as estruturas de dados serem acessados por mais de um aplicativo, ou por mais de uma inst�ncia do mesmo aplicativo. Todas as inst�ncias de todos os aplicativos obt�m sua pr�pria c�pia dos dados da DLL.</span><span class="sxs-lookup"><span data-stu-id="3f77a-p124">This means that DLL developers do not have to be concerned about static and global variables and data structures being accessed by more than one application, or more than one instance of the same application. Every instance of every application gets its own copy of the DLL's data.</span></span>
  
<span data-ttu-id="3f77a-p125">Os desenvolvedores de DLL n�o precisam se preocupar com o fato de a mesma inst�ncia do aplicativo chamar sua DLL v�rias vezes de threads diferentes, porque isso pode resultar em conten��o dos dados da inst�ncia. Para saber mais, consulte [Memory Management in Excel](memory-management-in-excel.md).</span><span class="sxs-lookup"><span data-stu-id="3f77a-p125">DLL developers do need to be concerned about the same instance of an application calling their DLL many times from different threads, because this can result in contention for that instance's data. For more information, see [Memory Management in Excel](memory-management-in-excel.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3f77a-261">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="3f77a-261">See also</span></span>

- [<span data-ttu-id="3f77a-262">Developing DLLs</span><span class="sxs-lookup"><span data-stu-id="3f77a-262">Developing DLLs</span></span>](developing-dlls.md) 
- [<span data-ttu-id="3f77a-263">Calling into Excel from the DLL or XLL</span><span class="sxs-lookup"><span data-stu-id="3f77a-263">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)

