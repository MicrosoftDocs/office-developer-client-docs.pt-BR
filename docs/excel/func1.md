---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- função func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408912"
---
# <a name="func1"></a>Func1

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
A função de planilha definida pelo usuário de exemplo demonstra o retorno de um valor estático de cadeia de caracteres. Quando GENERIC.xll é carregado, ele registra essa função para que possa ser chamada a partir da planilha.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Parâmetros

 _px_ (**LPXLOPER**)
  
Esse argumento é ignorado e serve apenas para disparar o Microsoft Excel para chamar a função.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

 **LPXLOPER12**: Sempre a cadeia de caracteres "Func1"
  
### <a name="example"></a>Exemplo

Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

