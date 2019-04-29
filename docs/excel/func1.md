---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- função func1 [Excel 2007]
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
  
Exemplo de função de planilha definida pelo usuário demonstra o retorno de um valor de cadeia de caracteres estática. Quando GENERIC. XLL é carregado, ele registra essa função para que ela possa ser chamada da planilha.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Parâmetros

 _PX_ (**LPXLOPER**)
  
Esse argumento é ignorado e serve apenas para disparar o Microsoft Excel para chamar a função.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

 **LPXLOPER12**: sempre a cadeia de caracteres "func1"
  
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

