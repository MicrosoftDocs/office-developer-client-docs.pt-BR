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
- função tempstr12 [excel 2007], função TempStrConst [Excel 2007]
localization_priority: Normal
ms.assetid: faf4ee4e-8d33-4cb3-ae16-5648a837ee4f
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 321c41aa87a3bfa0edc1d77ecc8fbe4b6a6a4730
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765450"
---
# <a name="tempstrconsttempstr12"></a>TempStrConst/TempStr12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de biblioteca Framework que cria um temporário **XLOPER/XLOPER12** que contém uma cadeia de caracteres **xltypeStr** , levando a uma cadeia de caracteres terminada em nulo fonte como entrada. A função aloca um novo buffer de memória e copia a cadeia de caracteres passada para ele. A cadeia de caracteres de entrada não seja alterada e portanto é declarada como **constante**.
  
```cs
LPXLOPER TempStrConst(const LPSTR str);
LPXLOPER12 TempStr12(const XCHAR* lpstr);
```

## <a name="parameters"></a>Par�metros

 _STR_
  
Um ponteiro para a cadeia de caracteres fonte terminada em nulo. No caso de s **XLOPER**, TempStrConst trunca strings que são maiores do que 255 bytes. No caso de **XLOPER12**s, TempStr12Const trunca cadeias de caracteres que são mais de 32.767 caracteres Unicode.
  
## <a name="return-value"></a>Valor retornado

Retorna uma cadeia de caracteres **xltypeStr** contendo uma cópia do buffer passado na cadeia de caracteres. 
  
## <a name="remarks"></a>Coment�rios

Observe que a cadeia de caracteres **XLOPER** função Framework, **TempStr**, se comporta de maneira diferente e tenta sobrescrever o primeiro caractere da cadeia de caracteres fornecida com o comprimento da cadeia de caracteres subsequentes. Isso não é sempre uma segura coisa a fazer: Microsoft Excel pode falhar se passadas uma cadeia de caracteres somente leitura. A maneira que o trabalho **TempStrConst** e o **TempStr12** agora é substituída dessa maneira de criação de cadeias de caracteres temporárias. Portanto, o primeiro caractere da cadeia de caracteres de entrada é tratado como o início da cadeia de caracteres, ou seja, não como um caractere de comprimento ou como um espaço para um caractere de comprimento. Você não deve passar cadeias de caracteres que possuem um caractere de comprimento codificado no início, conforme as consequências poderia ser imprevisíveis. 
  
## <a name="example"></a>Example

Este exemplo usa a função **TempStr12** para criar uma cadeia de caracteres para uma caixa de mensagem. 
  
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

