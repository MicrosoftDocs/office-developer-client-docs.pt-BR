---
title: fDialog/fDialog12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDialog
- fDialog12
keywords:
- função fdialog [excel 2007], função fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 554b76d2d316110286e83158acfff33aa68e19c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765367"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Definido pelo usuário comando de exemplo que demonstra como criar um UDD de Excel da Microsoft (caixa de diálogo definidas pelo usuário) dentro de uma DLL usando os recursos de caixa de diálogo do C API. Quando GENERIC.xll é carregado, ele cria um menu definidas pelo usuário, genérico, através do qual esse comando é acessado.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Par�metros

A função não assumir nenhum parâmetro.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

A função sempre retornará 1.
  
### <a name="example"></a>Example

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérico](functions-in-the-generic-dll.md)

