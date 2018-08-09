---
title: Implementar um visualizador de formulários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a567185c-bd72-4307-928c-08cac5494c1a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 645f98342b4b3ec2bebf3f233f719bd5cae69da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767397"
---
# <a name="implementing-a-form-viewer"></a>Implementar um visualizador de formulários

  
  
**Aplica-se a**: Outlook 
  
Um visualizador de formulário inclui três objetos: um site de mensagem, coletor de eventos e um contexto de modo de exibição de aviso de um modo de exibição. Cada um desses objetos permite que você interaja com um servidor de formulário e seus formulários.
  
Um site de mensagem é um objeto que implementa o [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interface e os servidores de formulário com tarefas como mover, salvar, ou excluindo mensagens, criando novas mensagens ou lançar novos servidores de formulário de Ajuda. Para obter mais informações sobre o status do seu cliente com relação a vários provedores de serviços, sites de mensagem são usados por formulários. Por exemplo, um formulário pode usar o seu site de mensagem para obter um ponteiro para o armazenamento de mensagens atual, uma mensagem ou uma pasta. 
  
Existem dois tipos de métodos na interface do **IMAPIMessageSite** : 
  
- Métodos que fornecem informações aos objetos de formulário.
    
- Métodos que manipulam mensagens.
    
Os métodos que fornecem informações aos objetos de formulário são simples de implementar. Em todos os casos, exceto [IMAPIMessageSite::GetSiteStatus](imapimessagesite-getsitestatus.md), você já deve ter disponíveis as informações necessárias para cada método.
  
Os métodos de manipulam mensagens devem agir como se eles tivessem sido disparados por meio da interface de usuário normal. Por exemplo, se um objeto form chama seu método [IMAPIMessageSite::NewMessage](imapimessagesite-newmessage.md) , se comportam como se o usuário teve escolhida redigir uma nova mensagem personalizada com uma interface do usuário regular. Os comandos que geralmente geram esse comportamento são **redação**, **Abrir**, **responder**, **responder a todos os destinatários**e **Encaminhar**. 
  
Um contexto de modo de exibição é um objeto que implementa o [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) interface e fornece os servidores de formulário com um contexto da mensagem atual, permitindo que os servidores alternar facilmente para a mensagem anterior ou seguinte na pasta. Um formulário usa um contexto de modo de exibição para compartilhamento de informações. Com um objeto de contexto do modo de exibição, um formulário pode: 
  
- Registre seu cliente para notificações.
    
- Ative a mensagem anterior ou seguinte na pasta.
    
- Obtenha informações sobre a impressão.
    
- Obter o status do seu cliente.
    
- Obtenha um fluxo que pode ser usado para salvar a versão de texto de uma mensagem.
    
Semelhante aos métodos no [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interface, os métodos do **IMAPIViewContext** correlacionam com ações do usuário e recursos do cliente que se relacionam com o contexto de modo de exibição. Por exemplo, um contexto de modo de exibição está envolvido com ativando a mensagem anterior ou seguinte, o conteúdo da pasta de classificação e filtragem de conteúdo da pasta. 
  
Não é importante que você fornecer para usuários de mecanismo para ativar esses recursos, só é importante que a semântica desses recursos mapa bem para os métodos na interface do **IMAPIViewContext** . 
  
Um modo de exibição de aviso coletor de eventos é um objeto que implementa o [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) notificações de interface e os identificadores dos servidores de formulário que afetam seus formulários visualizador e ajuda e visualizadores de formulário para que trabalhem juntos. Para obter mais informações, consulte [enviando e recebendo notificações de formulário](sending-and-receiving-form-notifications.md). 
  

