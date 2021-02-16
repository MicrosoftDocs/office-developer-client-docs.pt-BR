---
title: Chamar funções definidas pelo usuário a partir de DLLs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- udfs [excel 2007], chamando de dlls,funções definidas pelo usuário [Excel 2007], chamando de DLLs,DLLs [Excel 2007], chamando UDFs
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
# <a name="calling-user-defined-functions-from-dlls"></a>Chamar funções definidas pelo usuário a partir de DLLs

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Chamar funções definidas pelo usuário (UDFs) a partir de uma planilha é tão simples quanto chamar funções internas: você inserir a função por meio de uma fórmula de célula. No entanto, na API de C, não há códigos de função pré-definidos para usar com os retornos de chamada. Para permitir que você chame UDFs, a API de C exporta uma função somente XLL, a [função xlUDF.](xludf.md) O primeiro argumento da função é o nome da função como uma cadeia de caracteres, e os argumentos subsequentes são aqueles que a UDF normalmente espera. 
  
Você pode obter uma lista das funções e comandos do complemento XLL atualmente registrados usando a função **xlfGetWorkspace** com o argumento 44. Isso retorna uma matriz de três colunas onde as colunas representam o seguinte: 
  
- O caminho completo e o nome do XLL
    
- O nome da UDF ou comando conforme exportado do XLL
    
- A cadeia de caracteres de código de retorno e argumento
    
> [!NOTE]
> O nome exportado do XLL pode não ser igual ao nome registrado pelo qual o Excel conhece o UDF ou comando. 
  
A partir do Excel 2007, as funções de Análise Toolpak (ATP) estão totalmente integradas, e a API de C tem suas próprias enumerações para funções como PREÇO, **xlfPrice**. Em versões anteriores, você precisava usar **xlUDF** para chamar essas funções. Se o seu complemento precisar trabalhar com o Excel 2003 e o Excel 2007 ou versões posteriores, e ele usar essas funções, você deverá detectar a versão atual e chamar a função da maneira apropriada. 
  
## <a name="examples"></a>Exemplos

O exemplo a seguir mostra a **função xlUDF** que está sendo usada para chamar a função ATP **PRICE** quando a versão em execução do Excel é 2003 ou anterior. Para obter informações sobre a configuração de uma variável de versão global, como **gExcelVersion12plus** neste exemplo, consulte [Backward Compatibility](backward-compatibility.md).
  
> [!NOTE]
> Este exemplo usa as funções Framework **TempNum**, **TempStrConst** para configurar os argumentos e o Excel para chamar a API de C. 
  
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

Onde você está chamando uma função XLL que retorna um valor modificando um argumento no local, a função **xlUDF** ainda retorna o valor por meio do endereço do resultado **XLOPER/XLOPER12**. Em outras palavras, o resultado é retornado como se fosse por meio de uma instrução de retorno normal. O **XLOPER/XLOPER12** que corresponde ao argumento usado para o valor de retorno não émodificado. Por exemplo, considere as duas UDFs a seguir. 
  
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

Quando **udf \_ 2** chama **UDF \_ 1**, o valor de **pxArg** é inalterado após a chamada para **Excel12** e o valor retornado por **UDF_1** está contido em **xRetVal**.
  
Ao fazer um grande número de chamadas para uma UDF dessa maneira, você pode avaliar o nome da função primeiro usando a função [xlfEvaluate](xlfevaluate.md). O número resultante, que é igual à ID de registro retornada pela função **xlfRegister,** pode ser passado no lugar do nome da função como o primeiro argumento para a função **xlUDF.** Isso permite que o Excel encontre e chame a função mais rapidamente do que se fosse necessário procurar o nome da função sempre. 
  
## <a name="see-also"></a>Confira também

- [Permitir intervenções de usuário em operações demoradas](permitting-user-breaks-in-lengthy-operations.md)
- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
- [Introdução ao Excel XLL SDK](getting-started-with-the-excel-xll-sdk.md)

