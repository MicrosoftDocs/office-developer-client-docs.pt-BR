---
title: Implementando um Visualizador de Formulário
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bbd0792b0e3e3f274797fabd7f5d5eb49cfc73fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435814"
---
# <a name="implementing-a-form-viewer"></a>Implementando um Visualizador de Formulário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um visualizador de formulário inclui três objetos: um site de mensagens, um pia de conselhos de exibição e um contexto de exibição. Cada um desses objetos permite que você interaja com um servidor de formulários e seus formulários.
  
Um site de mensagens é um objeto que implementa a interface [IMAPIMessageSite : interface IUnknown](imapimessagesiteiunknown.md) e auxilia os servidores de formulário com tarefas como mover, salvar ou excluir mensagens, criar novas mensagens ou iniciar novos servidores de formulário. Os sites de mensagens são usados por formulários para obter informações sobre o status do cliente em relação a vários provedores de serviços. Por exemplo, um formulário pode usar seu site de mensagens para obter um ponteiro para seu armazenamento de mensagens atual, uma mensagem ou uma pasta. 
  
Há dois tipos de métodos na interface **IMAPIMessageSite:** 
  
- Métodos que fornecem informações para objetos de formulário.
    
- Métodos que manipulam mensagens.
    
Os métodos que fornecem informações para objetos de formulário são simples de implementar. Em todos os casos, exceto [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), você já deve ter disponível as informações necessárias para cada método.
  
Os métodos que manipulam mensagens devem agir como se tivessem sido disparados por meio da interface do usuário normal. Por exemplo, se um objeto de formulário chamar seu método [IMAPIMessageSite::NewMessage,](imapimessagesite-newmessage.md) comporte-se como se o usuário tivesse optado por redigir uma nova mensagem personalizada com sua interface de usuário normal. Os comandos que normalmente geram esse comportamento são **Compose**, **Open**, **Reply**, Reply to **All Recipients** e **Forward**. 
  
Um contexto de exibição é um objeto que implementa a interface [IMAPIViewContext : IUnknown](imapiviewcontextiunknown.md) e fornece servidores de formulário com um contexto para a mensagem atual, permitindo que os servidores alternem facilmente para a mensagem seguinte ou anterior na pasta. Um formulário usa um contexto de exibição para compartilhar informações. Com um objeto de contexto de exibição, um formulário pode: 
  
- Registre-se com seu cliente para receber notificações.
    
- Ative a próxima mensagem ou a mensagem anterior na pasta.
    
- Obter informações de impressão.
    
- Obter o status do seu cliente.
    
- Obter um fluxo que pode ser usado para salvar a versão de texto de uma mensagem.
    
Semelhante aos métodos na interface [IMAPIMessageSite : IUnknown,](imapimessagesiteiunknown.md) os métodos em **IMAPIViewContext** correlacionam-se com as ações do usuário e os recursos do cliente relacionados ao contexto de exibição. Por exemplo, um contexto de exibição está envolvido na ativação da mensagem seguinte ou anterior, na classificação do conteúdo da pasta e na filtragem do conteúdo da pasta. 
  
Não é importante qual mecanismo você fornece para que os usuários ativem esses recursos, é importante apenas que a semântica desses recursos mapeie bem para os métodos na interface **IMAPIViewContext.** 
  
Um sink de aviso de exibição é um objeto que implementa o [IMAPIViewAdviseSink : interface IUnknown](imapiviewadvisesinkiunknown.md) e lida com notificações de servidores de formulário que afetam seu visualizador e ajudam os formulários e visualizadores de formulário a trabalharem juntos. Para obter mais informações, consulte [Enviando e recebendo notificações de formulário.](sending-and-receiving-form-notifications.md) 
  

