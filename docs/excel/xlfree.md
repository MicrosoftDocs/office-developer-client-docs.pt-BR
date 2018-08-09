---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- função xlFree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765476"
---
# <a name="xlfree"></a>xlFree

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Usado para liberar memória recursos alocados pelo Microsoft Excel ao criar o retorno do valor **XLOPER**/ **XLOPER12** em uma chamada para [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)ou [Excel12v](excel4v-excel12v.md). A função **xlFree** libera a memória auxiliar e redefine o ponteiro para **Nulo** , mas não destruir outras partes da **XLOPER**/ **XLOPER12**.
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a>Parâmetros

 _px_1,..., px_n_
  
Um ou mais **XLOPER**/ **XLOPER12**s serem liberados. Nas versões do Excel até 2003, o número máximo de ponteiros que podem ser passados é 30. Iniciando no Excel 2007, isso é aumentado para 255.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

Essa função não retorna um valor.
  
## <a name="remarks"></a>Comentários

Você deve liberar cada **XLOPER** que você obtenha um valor de retorno do **Excel4** ou **Excel4v** e cada **XLOPER12** que você obteve como um valor de retorno de **Excel12** ou **Excel12v** se eles são um dos seguintes tipos: xltypeStr ** **, **xltypeMulti**ou **xltypeRef**. É sempre seguro liberar outros tipos, mesmo se eles não usar memória auxiliar, desde que você obteve-los do **Excel4** ou **Excel12**.
  
Onde você está retornando ao Excel um ponteiro para um **XLOPER**/ **XLOPER12** que ainda contém memória alocada para Excel serem liberados, você deve definir o **xlbitXLFree** para garantir a memória de versões do Excel. 
  
## <a name="example"></a>Exemplo

Este exemplo chama **Obtenha. WORKSPACE(1)** para retornar a plataforma na qual Excel está sendo executado como uma cadeia de caracteres. O código copia isso retornou a cadeia de caracteres em um buffer para uso posterior. O código coloca o buffer de volta à **XLOPER12** para uso posterior com a função do Excel. Finalmente, o código exibirá a cadeia de caracteres em uma caixa de alerta. 
  
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

