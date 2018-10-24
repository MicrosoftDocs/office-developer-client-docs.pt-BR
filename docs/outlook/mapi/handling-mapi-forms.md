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
ms.openlocfilehash: c6cdb07e1cbe68d90c6dcd9d5418f700ea5abc3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589648"
---
# <a name="handling-mapi-forms"></a>Manipular formulários MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um formulário MAPI é um visualizador de uma mensagem de uma determinada classe. Clientes que permitem que seus usuários trabalhar com mensagens que pertencem a uma variedade de classes de mensagem devem ser escritos para lidar com uma variedade de formulários MAPI. Para lidar com vários formulários, os clientes implementam um componente conhecido como um visualizador de formulário que contém os três objetos a seguintes:
  
- Um objeto de site de mensagem, que oferece suporte a [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) interface. 
    
- Um modo de exibição de aviso coletor de eventos, que suporta o [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) interface. 
    
- Um objeto de contexto do modo de exibição, que oferece suporte a [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) interface. 
    
Cada um desses objetos é usado por um componente chamado o servidor de formulário que implementa a cada formulário, como manipular seu armazenamento e as notificações geradas pelos clientes para manipular o modo de exibição. Um outro componente, o provedor de biblioteca de formulário, implementa um gerente de formulário. O gerente do formulário administra as bibliotecas de formulários, qual armazenam arquivos executáveis do servidor de formulário. Este administração inclui carregar o servidor de formulário apropriada e manipular a comunicação inicial entre o servidor e o cliente.
  
O diagrama a seguir mostra a relação entre um cliente e as outras partes da arquitetura de formulário de MAPI.
  
## <a name="mapi-form-architecture"></a>MAPI form architecture
  
![Arquitetura de formulário MAPI] (media/forms01.gif "Arquitetura de formulário MAPI")
  
Se estiver planejando lidar com formulários MAPI seu cliente, você usará o Gerenciador de formulário [IMAPIFormMgr: IUnknown](imapiformmgriunknown.md) interface para executar as cinco tarefas básicas: 
  
- Inicie o servidor de formulário MAPI apropriado quando uma mensagem é aberta ou composta.
    
- Exiba ícones dos servidores do formulário nas tabelas de conteúdo de pastas.
    
- Enviar e receber notificações de formulário. Para obter mais informações, consulte [enviando e recebendo notificações de formulário](sending-and-receiving-form-notifications.md).
    
- Permitir que usuários instalar ou remover servidores de formulário de bibliotecas de formulários. Para obter mais informações, consulte a [manutenção de uma biblioteca de formulários](maintaining-a-form-library.md).
    
- Permitir que usuários associar os servidores de formulário específicas pastas.
    
Para acessar o Gerenciador de formulário, chame a função de [MAPIOpenFormMgr](mapiopenformmgr.md) uma vez durante a inicialização. 
  
## <a name="in-this-section"></a>Nesta seção

- [Implementando uma tela de formulário](implementing-a-form-viewer.md): descreve como implementar um visualizador de formulário usando um modo de exibição de aviso de coletor de eventos, um site de mensagem e um contexto de modo de exibição.
    
- [Implementando verbos padrão do formulário](implementing-standard-form-verbs.md): descreve como implementar os verbos para os cliques de menu ou botão do usuário em formulários MAPI.
    
- [Enviando e recebendo notificações de formulário](sending-and-receiving-form-notifications.md): descreve como enviar e receber notificações de formulário.
    
- [Mantendo uma biblioteca de formulários](maintaining-a-form-library.md): descreve como manter uma biblioteca que contém todas as informações importantes sobre um formulário.
    
- [Carregando uma mensagem em um formulário](loading-a-message-into-a-form.md): descreve como carregar uma mensagem em um formulário.
    
- [Redigir uma nova mensagem usando um formulário](composing-a-new-message-by-using-a-form.md): descreve como redigir uma mensagem usando um formulário.
    
- [Exibir ícones de formulário](displaying-form-icons.md): descreve as etapas para a exibição de um ícone com um formulário.
    
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)
- [Desenvolvimento de servidores de formulário MAPI](developing-mapi-form-servers.md)

