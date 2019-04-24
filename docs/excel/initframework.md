---
title: InitFramework
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- InitFramework
keywords:
- função initframework [Excel 2007]
localization_priority: Normal
ms.assetid: c472a14a-92a6-46f6-924c-db8d6199d6fb
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 34fe8f4a606956b90a0d005b0bc523cea460153f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310679"
---
# <a name="initframework"></a>InitFramework

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função da biblioteca da estrutura que inicializa a biblioteca do Framework, que simplesmente inicializa as estruturas de dados de memória do**XLOPER12** de **XLOPER**/ temporários, liberando qualquer memória que já tenha sido alocada. 
  
```cs
short WINAPI InitFramework(void);
```

## <a name="parameters"></a>Parâmetros

Essa função não usa argumentos.
  
## <a name="return-value"></a>Valor de retorno

Essa função não retorna um valor.
  
## <a name="example"></a>Exemplo

Este exemplo usa a função **InitFramework** para liberar toda a memória temporária. 
  
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

