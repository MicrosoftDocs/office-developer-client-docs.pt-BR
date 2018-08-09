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
ms.openlocfilehash: ae6d8b2f0b95641678947e9bd75daa2237b080b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765381"
---
# <a name="fshowdialog"></a>fShowDialog

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Definido pelo usuário comando de exemplo que carrega e exibe uma caixa de diálogo de Windows nativa do exemplo. Quando GENERIC.xll é carregado, ele cria um menu definidas pelo usuário, genérico, através do qual esse comando é acessado.
  
```cs
int WINAPI fShowDialog(void);
```

## <a name="parameters"></a>Parâmetros

A função não assumir nenhum parâmetro.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

O inteiro de retorno de função zero para indicar a conclusão bem-sucedida
  
## <a name="remarks"></a>Comentários

As etapas para exibir a caixa de diálogo nativa do Windows são da seguinte maneira:
  
1. Obter o identificador de Windows principal do Microsoft Excel usando **GetHwnd**.
    
2. Capturar a janela principal do Excel usando **HookExcelWindow**.
    
3. Exibe a caixa de diálogo usando **DialogBox**.
    
4. Solte a janela principal do Excel usando **UnhookExcelWindow**.
    
### <a name="example"></a>Exemplo

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

