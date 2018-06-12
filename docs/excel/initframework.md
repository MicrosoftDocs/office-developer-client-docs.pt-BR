---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- função initframework [excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2d7e3286d794d6f21da9ef83ca44d18ec242c063
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765371"
---
# <a name="initframework"></a>InitFramework

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca de Framework que inicializa a biblioteca de Framework, que simplesmente inicializa temporário **XLOPER**/ **XLOPER12** estruturas de dados de memória, dispensando qualquer memória que já foi alocada. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Par�metros

Essa função não assume nenhum argumento.
  
## <a name="return-value"></a>Valor retornado

Essa função não retorna um valor.
  
## <a name="example"></a>Example

Este exemplo usa a função **InitFramework** para liberar memória temporária todos. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI InitFrameworkExample(void)
{
    InitFramework();
    return 1;
}
```

## <a name="see-also"></a>Confira também



[Funções na biblioteca do Framework](functions-in-the-framework-library.md)

