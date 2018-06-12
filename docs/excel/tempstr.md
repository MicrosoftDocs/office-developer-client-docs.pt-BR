---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- função tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ce9399168d5b94d10481d2d0b5b69dd2e1d1d2e9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765447"
---
# <a name="tempstr"></a>TempStr

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função preterida da biblioteca Framework que cria um temporário que contém uma cadeia de caracteres de byte **xltypeStr** **XLOPER** . Ele aceita uma cadeia de caracteres terminada em nulo fonte como entrada. Ele tentará substituir o primeiro caractere da cadeia de caracteres fornecida com o comprimento da cadeia de caracteres subsequentes. Isso não é sempre uma segura coisa a fazer: Microsoft Excel pode falhar se passadas uma cadeia de caracteres somente leitura. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Par�metros

 _STR_
  
Um ponteiro para a cadeia de caracteres fonte terminada em nulo. **TempStr** trunca strings que são maiores do que 255 bytes. 
  
## <a name="return-value"></a>Valor retornado

Retorna uma cadeia de caracteres **xltypeStr** contendo um ponteiro para o buffer passado na cadeia de caracteres. 
  
## <a name="remarks"></a>Coment�rios

A maneira em que ambos os trabalhos de [TempStrConst e TempStr12](tempstrconst-tempstr12.md) agora é substituída dessa maneira de criação de cadeias de caracteres temporárias. Essas funções alocar um novo buffer de memória e copiem a cadeia de caracteres passada para ele. As cadeias de caracteres de entrada para **TempStrConst** e **TempStr12** não forem alteradas e portanto são declaradas como **constante**. Por outro lado, a sequência de entrada para **TempStr** for alterada e não pode ser declarada como **constante**. O primeiro caractere da cadeia de caracteres de entrada é tratado como espaço para um caractere de comprimento e será substituído por essa função.
  
## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

