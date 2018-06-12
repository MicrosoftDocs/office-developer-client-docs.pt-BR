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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4e893cf1e54489610315dd5c5d57bd78c3c936d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765268"
---
# <a name="calling-user-defined-functions-from-dlls"></a>Chamando de funções definidas pelo usuário a partir de DLLs

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamando funções definidas pelo usuário (UDFs) a partir de uma planilha é tão simple quanto chamar funções internas: insira a função por meio de uma fórmula de célula. No entanto, da API do C, não há nenhuma códigos de funções predefinidas para uso com retornos de chamada. Para permitir que você chamar UDFs, a API C exporta uma função somente XLL, a função [xlUDF](xludf.md) . Argumento primeiro da função é o nome da função como uma cadeia de caracteres e argumentos subsequentes são aquelas que normalmente esperaria UDF. 
  
Você pode obter uma lista dos comandos e atualmente XLL suplemento funções registradas, usando a função **xlfGetWorkspace** com o argumento 44. Isso retorna uma matriz de três colunas onde as colunas representam o seguinte: 
  
- O caminho completo e o nome da XLL
    
- O nome do comando conforme exportá-los de XLL ou UDF
    
- A cadeia de caracteres de retorno e o argumento de código
    
> [!NOTE]
> O nome como exportá-los de XLL não pode ser o mesmo que o nome registrado pelo qual o Excel sabe o UDF ou o comando. 
  
Começando no Excel 2007, as funções de ferramentas de análise (ATP) são totalmente integradas e a API C tem seus próprio enumerações para funções como o preço, **xlfPrice**. Nas versões anteriores, era necessário usar **xlUDF** para chamar essas funções. Se seu suplemento precisa trabalhar com o Excel 2003 e Excel 2007 ou versões posteriores, e ele usa essas funções, você deve detectar a versão atual e chamar a função da maneira apropriada. 
  
## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a função **xlUDF** sendo usada para chamar a função de ATP **preço** quando a versão em execução do Excel 2003 ou anterior. Para obter informações sobre a configuração de uma variável de versão global, como **gExcelVersion12plus** neste exemplo, consulte [Compatibilidade com versões anteriores](backward-compatibility.md).
  
> [!NOTE]
> Este exemplo usa as funções de Framework **TempNum**, **TempStrConst** para configurar os argumentos e o Excel para chamar a API C. 
  
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

Ainda é onde você está chamando uma função XLL que retorna um valor modificando um argumento no local, a função **xlUDF** retornará o valor através do endereço do resultado **XLOPER/XLOPER12**. Em outras palavras, o resultado é retornado como se por meio de uma instrução return normal. **XLOPER/XLOPER12** que corresponde ao argumento que é usado para o valor de retorno é não modificados. Por exemplo, considere os seguintes dois UDFs. 
  
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

Quando **UDF\_2** chamadas **UDF\_1**, o valor de **pxArg** é inalterado após a chamada para **Excel12**e o valor retornado pela **UDF_1** está contido no **xRetVal**.
  
Quando você está fazendo um grande número de chamadas para um UDF dessa maneira, você pode avaliar o nome da função pela primeira vez usando a [função xlfEvaluate](xlfevaluate.md). O número resultante, que é o mesmo que a ID de registro que é retornada pela função **xlfRegister** , pode ser passado no lugar do nome da função como o primeiro argumento para a função **xlUDF** . Isso permite que o Excel localizar e chamar a função mais rapidamente do que se ele deve procurar o nome da função a cada vez. 
  
## <a name="see-also"></a>Confira também

- [Quebras de autorizações de usuário em operações demoradas](permitting-user-breaks-in-lengthy-operations.md)
- [Funções da API C que podem ser chamadas apenas por um DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Getting Started with the Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

