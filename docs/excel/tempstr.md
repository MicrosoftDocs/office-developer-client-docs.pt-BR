---
title: TempStr
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempStr
keywords:
- Função tempstr [excel 2007]
localization_priority: Normal
ms.assetid: b21b4868-babe-4255-9093-503172efa045
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4ccb6f3c764371c35bac12c8c78fede54234a7d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418040"
---
# <a name="tempstr"></a>TempStr

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de biblioteca de Estrutura preterida que cria um **XLOPER temporário** contendo uma cadeia de caracteres de byte **xltypeStr.** É necessário uma cadeia de caracteres de origem terminada por caractere nulo como entrada. Ele tenta substituir o primeiro caractere da cadeia de caracteres fornecida pelo comprimento da cadeia de caracteres subsequente. Isso nem sempre é uma coisa segura: o Microsoft Excel pode falhar se passar uma cadeia de caracteres somente leitura. 
  
```cs
LPXLOPER TempStr(LPSTR str);
```

## <a name="parameters"></a>Parâmetros

 _str_
  
Um ponteiro para a cadeia de caracteres de origem terminada por caractere nulo. **TempStr** trunca cadeias de caracteres que têm mais de 255 bytes. 
  
## <a name="return-value"></a>Valor de retorno

Retorna uma **cadeia de caracteres xltypeStr** que contém um ponteiro para o buffer de cadeia de caracteres passado. 
  
## <a name="remarks"></a>Comentários

This way of creating temporary strings is now deprecated in favor of the way in which both [TempStrConst and TempStr12](tempstrconst-tempstr12.md) work. Essas funções alocam um novo buffer de memória e copiam a cadeia de caracteres passada nele. As cadeias de caracteres de entrada **para TempStrConst** e **TempStr12** não são alteradas e, portanto, são declaradas como **constante**. Por outro lado, a cadeia de caracteres de entrada **para TempStr** é alterada e, portanto, não pode ser declarada como **constante**. O primeiro caractere da cadeia de caracteres de entrada é tratado como espaço para um caractere de comprimento e é substituído por essa função.
  
## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

