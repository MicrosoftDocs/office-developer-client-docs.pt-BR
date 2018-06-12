---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- função Func1 [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765372"
---
# <a name="func1"></a>Func1

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Função de planilha definida pelo usuário de exemplo demonstra o retorno de um valor de cadeia de caracteres estática. Quando GENERIC.xll é carregado, ele registra esta função para que ele possa ser chamado da planilha.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Par�metros

 _px_ (**LPXLOPER**)
  
Este argumento será ignorado e serve apenas para o Microsoft Excel para chamar a função de gatilho.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

 **LPXLOPER12**: sempre é a cadeia de caracteres "Func1"
  
### <a name="example"></a>Example

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérico](functions-in-the-generic-dll.md)

