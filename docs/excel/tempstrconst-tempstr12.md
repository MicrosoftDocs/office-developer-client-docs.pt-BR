---
title: TempStrConst/TempStr12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr12
- TempStrConst
keywords:
- Função tempstr12 [excel 2007],função TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d93f9de021c7ba325d9c11af2cede0245ffbbf6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407148"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de biblioteca de estrutura que cria um **XLOPER/XLOPER12** temporário que contém uma cadeia de caracteres **xltypeStr,** tendo uma cadeia de caracteres de origem terminada por nulo como entrada. A função aloca um novo buffer de memória e copia a cadeia de caracteres passada nele. A cadeia de caracteres de entrada não é alterada e, portanto, é declarada como **constante**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Parâmetros

 _str_
  
Um ponteiro para a cadeia de caracteres de origem terminada por caractere nulo. No caso de **XLOPER** s, TempStrConst trunca cadeias de caracteres que têm mais de 255 bytes. No caso de **XLOPER12** s, TempStr12Const trunca cadeias de caracteres que têm mais de 32.767 caracteres Unicode.
  
## <a name="return-value"></a>Valor de retorno

Retorna uma **cadeia de caracteres xltypeStr** que contém uma cópia do buffer de cadeia de caracteres passado. 
  
## <a name="remarks"></a>Comentários

Observe que a função de estrutura de cadeia de caracteres **XLOPER,** **TempStr**, se comporta de maneira diferente e tenta substituir o primeiro caractere da cadeia de caracteres fornecida pelo comprimento da cadeia de caracteres subsequente. Isso nem sempre é uma coisa segura: o Microsoft Excel pode falhar se passar uma cadeia de caracteres somente leitura. Essa maneira de criar cadeias de caracteres temporárias agora foi preterida em favor da maneira como **TempStrConst** e **TempStr12** funcionam. Portanto, o primeiro caractere da cadeia de caracteres de entrada é tratado como o início da cadeia de caracteres, ou seja, não como um caractere de comprimento ou como um espaço para um caractere de comprimento. Você não deve passar cadeias de caracteres que tenham um caractere de comprimento codificado no início, pois as consequências podem ser imprevisíveis. 
  
## <a name="example"></a>Exemplo

Este exemplo usa a **função TempStr12** para criar uma cadeia de caracteres para uma caixa de mensagem. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempStrExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempStr12Const(L"Made it!"));
   return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

