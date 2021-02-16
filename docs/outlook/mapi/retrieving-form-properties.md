---
title: Recuperando propriedades do formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 023d2cf312438b1e4b6a90c57e1ead7d606d7727
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412916"
---
# <a name="retrieving-form-properties"></a>Recuperando propriedades do formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para emitir uma consulta que seja significativa para um tipo de mensagem personalizado, um aplicativo precisa saber as propriedades esperadas nessa mensagem. Para obter uma lista de propriedades que uma classe de mensagem personalizada usa, um aplicativo cliente consulta o gerenciador de formulário MAPI. O gerenciador de formulário obtém essas informações do arquivo de configuração de formulário apropriado para que os aplicativos cliente possam usar essas informações sem a sobrecarga de ativar o próprio servidor de formulário. Para fazer isso, o aplicativo cliente chama o [método IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) da seguinte forma: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Observe que o terceiro argumento para **ResolveMessageClass** é a pasta que contém o índice de conteúdo associado que a consulta procurará por servidores de formulário. NULL indica que o gerenciador de formulário deve pesquisar todos os contêineres de formulário disponíveis. Se a consulta for executar em uma pasta específica, é melhor incluir o ponteiro [IMAPIFolder](imapifolderimapicontainer.md) apropriado. 
  
## <a name="see-also"></a>Confira também



[Interações do Servidor de Formulário](form-server-interactions.md)

