---
title: fShowDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fShowDialog
keywords:
- função fshowdialog [excel 2007]
localization_priority: Normal
ms.assetid: 6cc01075-7221-488e-870f-433da62930e6
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6122e4b99c69cd1bd878c9267ff85f59d0f61998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433588"
---
# <a name="fshowdialog"></a>fShowDialog

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemplo de comando definido pelo usuário que carrega e exibe um exemplo de caixa de diálogo nativa do Windows. Quando GENERIC.xll é carregado, ele cria um menu definido pelo usuário, Genérico, por meio do qual esse comando é acessado.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parâmetros

A função não aceita parâmetros.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função retorna o número inteiro zero para indicar a conclusão bem-sucedida
  
## <a name="remarks"></a>Comentários

As etapas para exibir a caixa de diálogo nativa do Windows são as seguintes:
  
1. Obtenha o alça principal do Windows do Microsoft Excel usando **GetHwnd**.
    
2. Conectar a janela principal do Excel **usando HookExcelWindow**.
    
3. Exibir a caixa de diálogo usando **DialogBox**.
    
4. Desaconsinchar a janela principal do Excel **usando UnhookExcelWindow**.
    
### <a name="example"></a>Exemplo

Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

