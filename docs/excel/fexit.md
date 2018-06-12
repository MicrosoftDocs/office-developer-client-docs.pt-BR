---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- função fexit [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765362"
---
# <a name="fexit"></a>fExit

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Definido pelo usuário comando de exemplo que descarrega GENERIC.xll. Quando GENERIC.xll é carregado, ele cria um menu definidas pelo usuário, genérico, através do qual esse comando é acessado. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Par�metros

A função não assumir nenhum parâmetro.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

A função sempre retornará 1.
  
## <a name="remarks"></a>Coment�rios

Isso é uma rotina iniciadas pelo usuário para sair GENERIC.xll Evite simplesmente chamar `UNREGISTER("GENERIC.XLL")` nessa função. Isso seria forçada cancelar o registro de todas as funções nessa DLL, mesmo se eles são registrados em algum lugar else. Cancelar o registro em vez disso, as funções de um por vez. 
  
### <a name="example"></a>Example

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérico](functions-in-the-generic-dll.md)

