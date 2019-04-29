---
title: Chamar funções definidas pelo usuário a partir de DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- UDFs [Excel 2007], chamadas de DLLs, funções definidas pelo usuário [Excel 2007], chamadas de DLLs, DLLs [Excel 2007], chamadas UDFs
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9e2ca3f4485fb41c5ab6a48f323b4c0093e747e4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417942"
---
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="52f21-104">Chamar funções definidas pelo usuário a partir de DLLs</span><span class="sxs-lookup"><span data-stu-id="52f21-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="52f21-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52f21-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52f21-106">Chamar funções definidas pelo usuário (UDFs) de uma planilha é tão simples quanto chamar funções internas: você insere a função por meio de uma fórmula de célula.</span><span class="sxs-lookup"><span data-stu-id="52f21-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="52f21-107">No enTanto, a partir da API de C, não há códigos de função pré-definidos para usar com os retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="52f21-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="52f21-108">Para permitir que você chame UDFs, a API C exporta uma função somente XLL, a função [xlUDF](xludf.md) .</span><span class="sxs-lookup"><span data-stu-id="52f21-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="52f21-109">O primeiro argumento da função é o nome da função como uma cadeia de caracteres e os argumentos subsequentes são aqueles que o UDF normalmente esperaria.</span><span class="sxs-lookup"><span data-stu-id="52f21-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="52f21-110">Você pode obter uma lista de funções e comandos de suplemento XLL registrados atualmente usando a função **xlfGetWorkspace** com o argumento 44.</span><span class="sxs-lookup"><span data-stu-id="52f21-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="52f21-111">Isso retorna uma matriz de três colunas onde as colunas representam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="52f21-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="52f21-112">O caminho completo e o nome do XLL</span><span class="sxs-lookup"><span data-stu-id="52f21-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="52f21-113">O nome do UDF ou comando exportado do XLL</span><span class="sxs-lookup"><span data-stu-id="52f21-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="52f21-114">A cadeia de caracteres de código de retorno e argumento</span><span class="sxs-lookup"><span data-stu-id="52f21-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="52f21-115">O nome a ser exportado do XLL pode não ser igual ao nome registrado pelo qual o Excel conhece o UDF ou comando.</span><span class="sxs-lookup"><span data-stu-id="52f21-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="52f21-116">A partir do Excel 2007, as funções de ferramentas de análise (ATP) são totalmente integradas e a API C tem suas próprias enumerações para funções como PRICE, **xlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="52f21-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="52f21-117">Em versões anteriores, você precisava usar o **xlUDF** para chamar essas funções.</span><span class="sxs-lookup"><span data-stu-id="52f21-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="52f21-118">Se o suplemento precisar funcionar com o Excel 2003 e o Excel 2007 ou versões posteriores e usar essas funções, você deverá detectar a versão atual e chamar a função da maneira apropriada.</span><span class="sxs-lookup"><span data-stu-id="52f21-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="52f21-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52f21-119">Examples</span></span>

<span data-ttu-id="52f21-120">O exemplo a seguir mostra a função **xlUDF** que está sendo usada para chamar o **preço** da função ATP quando a versão em execução do Excel for 2003 ou anterior.</span><span class="sxs-lookup"><span data-stu-id="52f21-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="52f21-121">Para obter informações sobre a configuração de uma variável de versão global, como **gExcelVersion12plus** neste exemplo, consulte [compatibilidade com versões anteriores](backward-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="52f21-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="52f21-122">Este exemplo usa as funções de estrutura **TempNum**, **TempStrConst** para configurar os argumentos e o Excel para chamar a API de C.</span><span class="sxs-lookup"><span data-stu-id="52f21-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
```C
LPXLOPER TempNum(double d);
LPXLOPER TempStrConst(const LPSTR lpstr);
int cdecl Excel(int xlfn, LPXLOPER pxResult, int count, ...);
double call_ATP_example(void)
{
  XLOPER xPrice;
  int xl_ret_val;
  if(gExcelVersion12plus) // Starting in Excel 2007
  {
    xl_ret_val = Excel(xlfPrice, &xPrice, 7,
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redemption value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  else // Excel 2003-
  {
    xl_ret_val = Excel(xlUDF, &xPrice, 8,
      TempStrConst("PRICE"),
      TempNum(39084.0), // settlement date 2-Jan-2007
      TempNum(46706.0), // maturity date 15-Nov-2027
      TempNum(0.04), // Coupon
      TempNum(0.05), // Yield
      TempNum(1.0), // redepmtion value: 100% of face
      TempNum(1.0), // Annual coupons
      TempNum(1.0)); // Rate basis Act/Act
  }
  if(xl_ret_val != xlretSuccess || xPrice.xltype != xltypeNum)
  {
// Even though PRICE is not expected to return a string, there
// is no harm in freeing the XLOPER to be safe
    Excel(xlFree, 0, 1, &xPrice);
    return -1.0; // an error value
  }
  return xPrice.val.num;
}
```

<br/>

<span data-ttu-id="52f21-123">Onde você está chamando uma função XLL que retorna um valor modificando um argumento no local, a função **xlUDF** ainda retorna o valor pelo endereço do resultado **XLOPER/XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="52f21-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="52f21-124">Em outras palavras, o resultado é retornado como se por meio de uma instrução de retorno normal.</span><span class="sxs-lookup"><span data-stu-id="52f21-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="52f21-125">O **XLOPER/XLOPER12** que corresponde ao argumento que é usado para o valor de retorno não é modificado.</span><span class="sxs-lookup"><span data-stu-id="52f21-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="52f21-126">Por exemplo, considere os dois UDFs a seguir.</span><span class="sxs-lookup"><span data-stu-id="52f21-126">For example, consider the following two UDFs.</span></span> 
  
```C
// Registered as "1E". Returns its argument incremented by 1.
void WINAPI UDF_1(double *pArg)
{
  *pArg += 1.0;
}
// Registered as "QQ". Returns its argument unmodified
// unless it is a number, in which case it increments it
// by calling UDF_1.
LPXLOPER12 WINAPI UDF_2(LPXLOPER12 pxArg)
{
  static XLOPER12 xRetVal; // Not thread-safe
  XLOPER12 xFn;
  xFn.xltype = xltypeStr;
  xFn.val.str = L"\005UDF_1";
  Excel12(xlUDF, &xRetVal, 2, &xFn, pxArg);
  xRetVal.xltype |= xlbitXLFree;
  return &xRetVal;
}
```

<span data-ttu-id="52f21-127">Quando **o\_UDF 2** chama o **UDF\_1**, o valor de **pxArg** é inalterado após a chamada para **Excel12**, e o valor retornado por **UDF_1** está contido em **xRetVal**.</span><span class="sxs-lookup"><span data-stu-id="52f21-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="52f21-128">Ao fazer um grande número de chamadas para um UDF dessa forma, você pode avaliar o nome da função primeiro usando a [função xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="52f21-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="52f21-129">O número resultante, que é o mesmo que a ID de registro retornada pela função **xlfRegister** , pode ser passado no lugar do nome da função como o primeiro argumento para a função **xlUDF** .</span><span class="sxs-lookup"><span data-stu-id="52f21-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="52f21-130">Isso permite que o Excel encontre e chame a função mais rapidamente do que se tiver que procurar o nome da função todas as vezes.</span><span class="sxs-lookup"><span data-stu-id="52f21-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52f21-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="52f21-131">See also</span></span>

- [<span data-ttu-id="52f21-132">Permitir intervenções de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="52f21-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="52f21-133">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="52f21-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="52f21-134">Introdução ao Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="52f21-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

