---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- função xlFree [Excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424711"
---
# <a name="xlfree"></a>xlFree

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para liberar recursos de memória alocados pelo Microsoft Excel ao criar o valor de retorno **XLOPER**/ **XLOPER12** em uma chamada para [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)ou [Excel12v](excel4v-excel12v.md). A função **xlFree** libera a memória auxiliar e redefine o ponteiro como **NULL** , mas não destrói outras partes do **XLOPER**/ **XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Parâmetros

 _px_1,..., px_n_
  
Um ou mais **XLOPER**/ **XLOPER12**s a serem liberados. Em versões do Excel até 2003, o número máximo de ponteiros que podem ser passados é 30. A partir do Excel 2007, isso é aumentado para 255.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Essa função não retorna um valor.
  
## <a name="remarks"></a>Comentários

Você deve liberar todos os **XLOPER** que você obtém como um valor de retorno de **Excel4** ou **Excel4v** e todos os **XLOPER12** que você obtém como um valor de retorno de **Excel12** ou **Excel12v** se eles forem um dos seguintes tipos: **xltypeStr **, **XltypeMulti**ou **xltypeRef**. É sempre seguro liberar outros tipos, mesmo se eles não usarem memória auxiliar, desde que você os tenha obtido do **Excel4** ou do **Excel12**.
  
Onde você está retornando ao Excel um ponteiro para um **XLOPER**/ **XLOPER12** que ainda contém memória alocada no Excel para ser liberado, você deve definir o **xlbitXLFree** para garantir que o Excel libere a memória. 
  
## <a name="example"></a>Exemplo

Este exemplo chama **Get. WORKSPACE (1)** para retornar a plataforma na qual o Excel está atualmente em execução como uma cadeia de caracteres. O código copia essa cadeia de caracteres retornada para um buffer para uso posterior. O código coloca o buffer de volta no **XLOPER12** para uso posterior com a função do Excel. Por fim, o código exibe a cadeia de caracteres em uma caixa de alerta. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Confira também

- [Funções da API de C que podem ser chamadas apenas de uma DLL ou XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

