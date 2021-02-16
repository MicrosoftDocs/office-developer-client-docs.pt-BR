---
title: Manipular formulários MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c1589d49-2ebe-48ce-85c7-b70fb7c1bb67
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 91347f0c34b8d7b76e4e456397a1faa061f3b2c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423052"
---
# <a name="handling-mapi-forms"></a>Manipular formulários MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um formulário MAPI é um visualizador de uma mensagem de uma classe específica. Os clientes que permitem que seus usuários trabalhem com mensagens pertencentes a uma variedade de classes de mensagens devem ser gravados para lidar com uma variedade de formulários MAPI. Para manipular vários formulários, os clientes implementam um componente conhecido como visualizador de formulários que contém os três objetos a seguir:
  
- Um objeto de site de mensagem, que oferece suporte à interface [IMAPIMessageSite : IUnknown.](imapimessagesiteiunknown.md) 
    
- Um sink de alerta de exibição, que dá suporte à [interface IMAPIViewAdviseSink : IUnknown.](imapiviewadvisesinkiunknown.md) 
    
- Um objeto de contexto de exibição, que oferece suporte à interface [IMAPIViewContext : IUnknown.](imapiviewcontextiunknown.md) 
    
Cada um desses objetos é usado por um componente chamado servidor de formulário que implementa cada formulário, manipulando seu armazenamento e as notificações geradas por clientes que manipulam o visualização. Um outro componente, o provedor de biblioteca de formulário, implementa um gerenciador de formulário. O gerenciador de formulário administra as bibliotecas de formulário, que armazenam arquivos executáveis do servidor de formulário. Essa administração inclui carregar o servidor de formulário apropriado e manipular a comunicação inicial entre o servidor e o cliente.
  
O diagrama a seguir mostra a relação entre um cliente e as outras partes da arquitetura de formulário MAPI.
  
## <a name="mapi-form-architecture"></a>MAPI form architecture
  
![MapI form architecture](media/forms01.gif "MAPI form architecture")
  
Se seu cliente planeja lidar com formulários MAPI, você usará o [IMAPIFormMgr do](imapiformmgriunknown.md) gerenciador de formulários : interface IUnknown para executar cinco tarefas básicas: 
  
- Iniciar o servidor de formulário MAPI apropriado quando uma mensagem for aberta ou composta.
    
- Exibe os ícones dos servidores de formulário nos índices de conteúdo das pastas.
    
- Enviar e receber notificações de formulário. Para obter mais informações, consulte [Enviando e recebendo notificações de formulário.](sending-and-receiving-form-notifications.md)
    
- Permitir que os usuários instalem ou removam servidores de formulário de bibliotecas de formulário. Para obter mais informações, consulte [Mantendo uma biblioteca de formulário.](maintaining-a-form-library.md)
    
- Permitir que os usuários associem servidores de formulário a pastas específicas.
    
Para acessar o gerenciador de formulário, chame a [função MAPIOpenFormMgr](mapiopenformmgr.md) uma vez durante a inicialização. 
  
## <a name="in-this-section"></a>Nesta seção

- [Implementando um Visualizador de](implementing-a-form-viewer.md)Formulário: descreve como implementar um visualizador de formulário usando um evento de alerta de exibição, um site de mensagens e um contexto de exibição.
    
- [Implementando verbos de formulário](implementing-standard-form-verbs.md)padrão: descreve como implementar os verbos para cliques de botão ou menu de usuário em formulários MAPI.
    
- [Envio e recebimento de notificações de](sending-and-receiving-form-notifications.md)formulário: descreve como enviar e receber notificações de formulário.
    
- [Mantendo uma biblioteca de formulário:](maintaining-a-form-library.md)descreve como manter uma biblioteca que contém todas as informações importantes sobre um formulário.
    
- [Carregando uma mensagem em um formulário:](loading-a-message-into-a-form.md)descreve como carregar uma mensagem em um formulário.
    
- [Composição de uma nova mensagem usando um formulário:](composing-a-new-message-by-using-a-form.md)descreve como redigir uma mensagem usando um formulário.
    
- [Exibindo ícones de](displaying-form-icons.md)formulário: descreve as etapas para exibir um ícone com um formulário.
    
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)
- [Desenvolvendo servidores de formulário MAPI](developing-mapi-form-servers.md)

