---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- função fdance [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409045"
---
# <a name="fdance"></a>fDance

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Exemplo de comando definido pelo usuário que altera as células selecionadas na planilha ativa até que o usuário pressione **ESC**. Quando GENERIC.xll é carregado, ele cria um menu definido pelo usuário, Genérico, por meio do qual esse comando é acessado.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parâmetros

A função não aceita parâmetros.
  
## <a name="property-valuereturn-value"></a>Valor de propriedade/Valor de retorno

A função sempre retorna 1.
  
## <a name="remarks"></a>Comentários

Este é um exemplo de uma operação demorada. Ele chama a função [xlAbort ocasionalmente.](xlabort.md) Isso gera o processador (ajudando com multitarefa cooperativo) e verifica se o usuário pressionou **o ESC** para cancelar a operação. Se sim, oferece ao usuário a chance de cancelar a anulação. 
  
### <a name="example"></a>Exemplo

Consulte  `\SAMPLES\GENERIC\GENERIC.C` o código-fonte para esta função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérica](functions-in-the-generic-dll.md)

