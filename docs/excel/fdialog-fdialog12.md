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
- função fdialog [excel 2007],função fDialog12 [Excel 2007]
localization_priority: Normal
ms.assetid: a9a47408-07d1-4a00-9596-abc48b12392f
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58d0df500c38534ec1315d2dab1517c1f5272ad5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431523"
---
# <a name="fdialogfdialog12"></a>fDialog/fDialog12

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemplo de comando definido pelo usuário que demonstra como criar uma UDD do Microsoft Excel (caixa de diálogo definida pelo usuário) em uma DLL usando os recursos da caixa de diálogo na API de C. Quando GENERIC.xll é carregado, ele cria um menu definido pelo usuário, Genérico, por meio do qual esse comando é acessado.
  
```cs
int WINAPI fDialog(void);
```

## <a name="parameters"></a>Parâmetros

A função não aceita parâmetros.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função sempre retorna 1.
  
### <a name="example"></a>Exemplo

Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

