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
description: 'Aplica-se a: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765375"
---
# <a name="fdance"></a>fDance

 **Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio 
  
Comando de exemplo definida pelo usuário que altera as células selecionadas na planilha ativa ao redor até que o usuário pressiona **ESC**. Quando GENERIC.xll é carregado, ele cria um menu definidas pelo usuário, genérico, através do qual esse comando é acessado.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Par�metros

A função não assumir nenhum parâmetro.
  
## <a name="property-valuereturn-value"></a>Propriedade valor/valor de retorno

A função sempre retornará 1.
  
## <a name="remarks"></a>Coment�rios

Este é um exemplo de uma operação demorada. Ele chama a função [xlAbort](xlabort.md) ocasionalmente. Isso produz o processador (ajudando com multitarefa cooperativa) e verifica se o usuário pressiona **ESC** para cancelar a operação. Em caso afirmativo, ele oferece ao usuário uma oportunidade de cancelar a anulação. 
  
### <a name="example"></a>Example

Consulte `\SAMPLES\GENERIC\GENERIC.C` para o código-fonte para essa função. 
  
## <a name="see-also"></a>Confira também



[Funções na DLL genérico](functions-in-the-generic-dll.md)

