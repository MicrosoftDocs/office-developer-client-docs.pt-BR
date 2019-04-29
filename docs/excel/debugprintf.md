---
title: debugPrintf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- debugPrintf
keywords:
- função debugprintf [Excel 2007]
localization_priority: Normal
ms.assetid: 9ad541f6-0b35-4f50-926a-8940e3f8033a
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 08bde61573874c137b18856fd24d23b324a35328
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424795"
---
# <a name="debugprintf"></a>debugPrintf

**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A função da biblioteca de estrutura que grava uma cadeia de caracteres byte terminada em nulo no depurador ativo por meio da função SDK do Windows **OutputDebugStringa**. Se o aplicativo não tiver nenhum depurador, o depurador do sistema exibe a cadeia de caracteres. Se o aplicativo não tiver nenhum depurador e o depurador do sistema não estiver ativo, o **debugPrintf** não fará nada. 
  
Essa função não retorna um valor.
  
```cs
void WINAPI debugPrintf(LPSTR lpFormat, arguments);
```

## <a name="parameters"></a>Parâmetros

 _lpFormat (LPSTR)_
  
A cadeia de caracteres de formato, que segue a sintaxe e as regras usadas com a função **sprintf** . 
  
 _argumento_
  
Zero ou mais argumentos para corresponder à cadeia de caracteres de formato.
  
## <a name="example"></a>Exemplo

Essa função imprime uma cadeia de caracteres para mostrar que o controle foi passado para ela. O sinalizador _DEBUG deve ser definido antes da compilação ou esta função não faz nada.
  
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



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

