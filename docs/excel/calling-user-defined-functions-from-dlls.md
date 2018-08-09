---
title: Chamando de funções definidas pelo usuário a partir de DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- UDFs [excel 2007], chamada a partir de dlls,-funções definidas pelo usuário [Excel 2007], chamada a partir de DLLs, DLLs [Excel 2007], chamar UDFs
localization_priority: Normal
ms.assetid: 99a37108-0083-4240-9c6a-3afa8d7a04f6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4e893cf1e54489610315dd5c5d57bd78c3c936d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765268"
---
# <a name="calling-user-defined-functions-from-dlls"></a><span data-ttu-id="52549-104">Chamando de funções definidas pelo usuário a partir de DLLs</span><span class="sxs-lookup"><span data-stu-id="52549-104">Calling user-defined functions from DLLs</span></span>

<span data-ttu-id="52549-105">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="52549-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="52549-106">Chamando funções definidas pelo usuário (UDFs) a partir de uma planilha é tão simple quanto chamar funções internas: insira a função por meio de uma fórmula de célula.</span><span class="sxs-lookup"><span data-stu-id="52549-106">Calling user-defined functions (UDFs) from a worksheet is as simple as calling built-in functions: You enter the function via a cell formula.</span></span> <span data-ttu-id="52549-107">No entanto, da API do C, não há nenhuma códigos de funções predefinidas para uso com retornos de chamada.</span><span class="sxs-lookup"><span data-stu-id="52549-107">However, from the C API, there are no pre-defined function codes to use with the call-backs.</span></span> <span data-ttu-id="52549-108">Para permitir que você chamar UDFs, a API C exporta uma função somente XLL, a função [xlUDF](xludf.md) .</span><span class="sxs-lookup"><span data-stu-id="52549-108">To enable you to call UDFs, the C API exports an XLL-only function, the [xlUDF ](xludf.md) function.</span></span> <span data-ttu-id="52549-109">Argumento primeiro da função é o nome da função como uma cadeia de caracteres e argumentos subsequentes são aquelas que normalmente esperaria UDF.</span><span class="sxs-lookup"><span data-stu-id="52549-109">The function's first argument is the function name as a string, and subsequent arguments are those that the UDF would normally expect.</span></span> 
  
<span data-ttu-id="52549-110">Você pode obter uma lista dos comandos e atualmente XLL suplemento funções registradas, usando a função **xlfGetWorkspace** com o argumento 44.</span><span class="sxs-lookup"><span data-stu-id="52549-110">You can obtain a list of the currently registered XLL add-in functions and commands by using the **xlfGetWorkspace** function with the argument 44.</span></span> <span data-ttu-id="52549-111">Isso retorna uma matriz de três colunas onde as colunas representam o seguinte:</span><span class="sxs-lookup"><span data-stu-id="52549-111">This returns a three-column array where the columns represent the following:</span></span> 
  
- <span data-ttu-id="52549-112">O caminho completo e o nome da XLL</span><span class="sxs-lookup"><span data-stu-id="52549-112">The full path and name of the XLL</span></span>
    
- <span data-ttu-id="52549-113">O nome do comando conforme exportá-los de XLL ou UDF</span><span class="sxs-lookup"><span data-stu-id="52549-113">The name of the UDF or command as exported from the XLL</span></span>
    
- <span data-ttu-id="52549-114">A cadeia de caracteres de retorno e o argumento de código</span><span class="sxs-lookup"><span data-stu-id="52549-114">The return and argument code string</span></span>
    
> [!NOTE]
> <span data-ttu-id="52549-115">O nome como exportá-los de XLL não pode ser o mesmo que o nome registrado pelo qual o Excel sabe o UDF ou o comando.</span><span class="sxs-lookup"><span data-stu-id="52549-115">The name as exported from the XLL might not be the same as the registered name by which Excel knows the UDF or command.</span></span> 
  
<span data-ttu-id="52549-116">Começando no Excel 2007, as funções de ferramentas de análise (ATP) são totalmente integradas e a API C tem seus próprio enumerações para funções como o preço, **xlfPrice**.</span><span class="sxs-lookup"><span data-stu-id="52549-116">Starting in Excel 2007, the Analysis Toolpak (ATP) functions are fully integrated, and the C API has its own enumerations for functions such as PRICE, **xlfPrice**.</span></span> <span data-ttu-id="52549-117">Nas versões anteriores, era necessário usar **xlUDF** para chamar essas funções.</span><span class="sxs-lookup"><span data-stu-id="52549-117">In earlier versions, you had to use **xlUDF** to call these functions.</span></span> <span data-ttu-id="52549-118">Se seu suplemento precisa trabalhar com o Excel 2003 e Excel 2007 ou versões posteriores, e ele usa essas funções, você deve detectar a versão atual e chamar a função da maneira apropriada.</span><span class="sxs-lookup"><span data-stu-id="52549-118">If your add-in needs to work with Excel 2003 and Excel 2007 or later versions, and it uses these functions, you should detect the current version and call the function in the appropriate way.</span></span> 
  
## <a name="examples"></a><span data-ttu-id="52549-119">Exemplos</span><span class="sxs-lookup"><span data-stu-id="52549-119">Examples</span></span>

<span data-ttu-id="52549-120">O exemplo a seguir mostra a função **xlUDF** sendo usada para chamar a função de ATP **preço** quando a versão em execução do Excel 2003 ou anterior.</span><span class="sxs-lookup"><span data-stu-id="52549-120">The following example shows the **xlUDF** function being used to call the ATP function **PRICE** when the running version of Excel is 2003 or earlier.</span></span> <span data-ttu-id="52549-121">Para obter informações sobre a configuração de uma variável de versão global, como **gExcelVersion12plus** neste exemplo, consulte [Compatibilidade com versões anteriores](backward-compatibility.md).</span><span class="sxs-lookup"><span data-stu-id="52549-121">For information about the setting of a global version variable, such as **gExcelVersion12plus** in this example, see [Backward Compatibility](backward-compatibility.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="52549-122">Este exemplo usa as funções de Framework **TempNum**, **TempStrConst** para configurar os argumentos e o Excel para chamar a API C.</span><span class="sxs-lookup"><span data-stu-id="52549-122">This example uses the Framework functions **TempNum**, **TempStrConst** to set up the arguments and Excel to call the C API.</span></span> 
  
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

<span data-ttu-id="52549-123">Ainda é onde você está chamando uma função XLL que retorna um valor modificando um argumento no local, a função **xlUDF** retornará o valor através do endereço do resultado **XLOPER/XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="52549-123">Where you are calling an XLL function that returns a value by modifying an argument in place, the **xlUDF** function still returns the value via the address of the result **XLOPER/XLOPER12**.</span></span> <span data-ttu-id="52549-124">Em outras palavras, o resultado é retornado como se por meio de uma instrução return normal.</span><span class="sxs-lookup"><span data-stu-id="52549-124">In other words, the result is returned as if through a normal return statement.</span></span> <span data-ttu-id="52549-125">**XLOPER/XLOPER12** que corresponde ao argumento que é usado para o valor de retorno é não modificados.</span><span class="sxs-lookup"><span data-stu-id="52549-125">The **XLOPER/XLOPER12** that corresponds to the argument that is used for the return value is unmodified.</span></span> <span data-ttu-id="52549-126">Por exemplo, considere os seguintes dois UDFs.</span><span class="sxs-lookup"><span data-stu-id="52549-126">For example, consider the following two UDFs.</span></span> 
  
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

<span data-ttu-id="52549-127">Quando **UDF\_2** chamadas **UDF\_1**, o valor de **pxArg** é inalterado após a chamada para **Excel12**e o valor retornado pela **UDF_1** está contido no **xRetVal**.</span><span class="sxs-lookup"><span data-stu-id="52549-127">When **UDF\_2** calls **UDF\_1**, the value of **pxArg** is unchanged after the call to **Excel12**, and the value returned by **UDF_1** is contained in **xRetVal**.</span></span>
  
<span data-ttu-id="52549-128">Quando você está fazendo um grande número de chamadas para um UDF dessa maneira, você pode avaliar o nome da função pela primeira vez usando a [função xlfEvaluate](xlfevaluate.md).</span><span class="sxs-lookup"><span data-stu-id="52549-128">When you are making a large number of calls to a UDF in this way, you can evaluate the function name first by using the [xlfEvaluate function](xlfevaluate.md).</span></span> <span data-ttu-id="52549-129">O número resultante, que é o mesmo que a ID de registro que é retornada pela função **xlfRegister** , pode ser passado no lugar do nome da função como o primeiro argumento para a função **xlUDF** .</span><span class="sxs-lookup"><span data-stu-id="52549-129">The resulting number, which is the same as the registration ID that is returned by the **xlfRegister** function, can be passed in place of the function name as the first argument to the **xlUDF** function.</span></span> <span data-ttu-id="52549-130">Isso permite que o Excel localizar e chamar a função mais rapidamente do que se ele deve procurar o nome da função a cada vez.</span><span class="sxs-lookup"><span data-stu-id="52549-130">This enables Excel to find and call the function more quickly than if it has to look up the function name every time.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52549-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="52549-131">See also</span></span>

- [<span data-ttu-id="52549-132">Permitir intervenções de usuário em operações demoradas</span><span class="sxs-lookup"><span data-stu-id="52549-132">Permitting User Breaks in Lengthy Operations</span></span>](permitting-user-breaks-in-lengthy-operations.md)
- [<span data-ttu-id="52549-133">Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL</span><span class="sxs-lookup"><span data-stu-id="52549-133">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [<span data-ttu-id="52549-134">Getting Started with the Excel XLL SDK</span><span class="sxs-lookup"><span data-stu-id="52549-134">Getting Started with the Excel XLL SDK</span></span>](getting-started-with-the-excel-xll-sdk.md)

