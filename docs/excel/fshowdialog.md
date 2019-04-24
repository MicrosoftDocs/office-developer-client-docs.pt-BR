---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- função fshowdialog [Excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310847"
---
# <a name="fshowdialog"></a>fShowDialog

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemplo de comando definido pelo usuário que carrega e exibe uma caixa de diálogo nativa de exemplo do Windows. Quando GENERIC. XLL é carregado, ele cria um menu definido pelo usuário, genérico, através do qual este comando é acessado.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parâmetros

A função não utiliza parâmetros.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função retorna o inteiro zero para indicar a conclusão bem-sucedida
  
## <a name="remarks"></a>Comentários

As etapas para exibir a caixa de diálogo nativa do Windows são as seguintes:
  
1. Obter o identificador principal do Windows do Microsoft **** Excel usando GetHwnd.
    
2. Enganchar a janela principal do Excel usando o **HookExcelWindow**.
    
3. Exibe a caixa de diálogo usando o **DialogBox**.
    
4. Desenganchar a janela principal do Excel usando o **UnhookExcelWindow**.
    
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

