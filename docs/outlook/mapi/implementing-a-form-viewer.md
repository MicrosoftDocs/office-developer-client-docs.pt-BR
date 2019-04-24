---
title: Implementar um visualizador de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332890"
---
# <a name="implementing-a-form-viewer"></a>Implementar um visualizador de formulários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um visualizador de formulários inclui três objetos: um site de mensagens, um coletor de aviso de exibição e um contexto de exibição. Cada um desses objetos permite interagir com um servidor de formulários e seus formulários.
  
Um site de mensagens é um objeto que implementa a interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) e ajuda os servidores de formulário com tarefas como mover, salvar ou excluir mensagens, criar novas mensagens ou iniciar novos servidores de formulários. Os sites de mensagens são usados por formulários para obter informações sobre o status do seu cliente em relação a vários provedores de serviços. Por exemplo, um formulário pode usar seu site de mensagens para obter um ponteiro para o repositório de mensagens atual, uma mensagem ou uma pasta. 
  
Há dois tipos de métodos na interface **IMAPIMessageSite** : 
  
- Métodos que fornecem informações para objetos de formulário.
    
- Métodos que manipulam mensagens.
    
Os métodos que fornecem informações a objetos de formulário são simples de implementar. Em todos os casos, exceto [IMAPIMessageSite:: GetSiteStatus](imapimessagesite-getsitestatus.md), você já deve ter disponível as informações exigidas por cada método.
  
Os métodos que manipulam mensagens devem atuar como se tivessem sido acionados por meio da interface do usuário normal. Por exemplo, se um objeto Form chamar o método [IMAPIMessageSite:: NewMessage](imapimessagesite-newmessage.md) , se comportará como se o usuário tivesse optado por compor uma nova mensagem personalizada com sua interface do usuário normal. Comandos que normalmente geram esse comportamento **** são compor, **abrir**, **responder**, **responder a todos os destinatários**e encaminhar. **** 
  
Um contexto de exibição é um objeto que implementa a interface [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) e fornece servidores de formulário com um contexto para a mensagem atual, permitindo que os servidores alternem facilmente para a mensagem seguinte ou anterior na pasta. Um formulário usa um contexto de exibição para compartilhar informações. Com um objeto de contexto de exibição, um formulário pode: 
  
- Registre-se em seu cliente para notificações.
    
- Ativar a mensagem seguinte ou anterior na pasta.
    
- Obter informações de impressão.
    
- Obter o status do cliente.
    
- Obtenha um Stream que pode ser usado para salvar a versão de texto de uma mensagem.
    
Semelhante aos métodos da interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) , os métodos no **IMAPIViewContext** se correlacionam com ações do usuário e recursos do cliente relacionados ao contexto do modo de exibição. Por exemplo, um contexto de exibição está envolvido na ativação da mensagem seguinte ou anterior, classificando o conteúdo da pasta e filtrando o conteúdo da pasta. 
  
Não é importante qual mecanismo você fornece para que os usuários ativem esses recursos, é importante que a semântica desses recursos seja mapeada bem para os métodos na interface **IMAPIViewContext** . 
  
Um coletor de aviso de exibição é um objeto que implementa a interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) e manipula notificações de servidores de formulário que afetam o visualizador e formulários de ajuda e visualizadores de formulários para trabalhar juntos. Para obter mais informações, consulte [envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md). 
  

