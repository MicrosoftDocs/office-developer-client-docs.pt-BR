---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- função fexit [Excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429912"
---
# <a name="fexit"></a>fExit

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemplo de comando definido pelo usuário que descarrega GENERIC. XLL. Quando GENERIC. XLL é carregado, ele cria um menu definido pelo usuário, genérico, através do qual este comando é acessado. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parâmetros

A função não utiliza parâmetros.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função sempre retorna 1.
  
## <a name="remarks"></a>Comentários

Esta é uma rotina iniciada pelo usuário para sair genérica. XLL você deve evitar simplesmente `UNREGISTER("GENERIC.XLL")` chamar essa função. Isso forçaria a cancelar o registro de todas as funções nessa DLL, mesmo que elas estejam registradas em outro lugar. Em vez disso, cancele o registro de funções, uma de cada vez. 
  
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

