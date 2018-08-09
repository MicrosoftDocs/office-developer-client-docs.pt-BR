---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- função debugprintf [excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 25669cfc705e797b80be0fab590d809e8f1e3b5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765261"
---
# <a name="debugprintf"></a>debugPrintf

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca Framework que grava uma sequência de byte terminada em nulo ao depurador ativo por meio da função **OutputDebugStringA**do SDK do Windows. Se o aplicativo não possui nenhum depurador, o depurador do sistema exibe a cadeia de caracteres. Se o aplicativo não tem nenhum depurador e o depurador do sistema não está ativo, **debugPrintf** não fará nada. 
  
Essa função não retorna um valor.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Parâmetros

 _lpFormat (LPSTR)_
  
A sequência de formato, que segue a sintaxe e as regras para que usados com a função **sprintf** . 
  
 _argumentos_
  
Zero ou mais argumentos para coincidir com a cadeia de caracteres de formato.
  
## <a name="example"></a>Exemplo

Essa função imprime uma cadeia de caracteres para mostrar que o controle foi passado para ele. O sinalizador _DEBUG deve ser definido antes de compilar senão essa função não faz nada.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI debugPrintfExample(void)
{
#ifdef _DEBUG
   debugPrintf("Made it!\r");
#endif
   return 1;
}

```

## <a name="see-also"></a>Confira também



[Funções na biblioteca de estrutura](functions-in-the-framework-library.md)

