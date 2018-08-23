---
title: Recuperar propriedades do formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9dec5ad6-af34-4c5e-848b-5c3909d0c0a1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: a6636b6298fcf565a297ed5df8a885c43c279c2c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583845"
---
# <a name="retrieving-form-properties"></a>Recuperar propriedades do formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para emitir uma consulta que é significativa para um tipo de mensagem personalizado, um aplicativo que precisa saber as propriedades esperados sobre a mensagem. Para obter uma lista de propriedades que usa uma classe de mensagem personalizada, um aplicativo cliente consulta o Gerenciador de formulário MAPI. O gerente do formulário obtém essas informações do arquivo de configuração de formulário apropriada para que os aplicativos cliente podem usar essas informações sem a sobrecarga de ativação do servidor de formulário em si. Para fazer isso, o aplicativo cliente chama o método [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) da seguinte maneira: 
  
```cpp
IMAPIFormInfo *pfrminf = NULL;
hr = pfrmmgr->ResolveMessageClass("IPM.Demo", 0L, NULL, &amp;pfrminf);

```

Observe que o terceiro argumento para **ResolveMessageClass** é a pasta que contém a tabela de conteúdo associado que a consulta buscarão para servidores de formulário. NADA indica que o Gerenciador de formulário deve pesquisar todos os contêineres do formulário disponível. Se a consulta deve ser executado em uma pasta particular, é melhor incluir o ponteiro de [IMAPIFolder](imapifolderimapicontainer.md) apropriado em vez disso. 
  
## <a name="see-also"></a>Confira também



[Interações do servidor de formulário](form-server-interactions.md)

