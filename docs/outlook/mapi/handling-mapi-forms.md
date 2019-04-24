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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299445"
---
# <a name="handling-mapi-forms"></a>Manipular formulários MAPI

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um formulário MAPI é um visualizador para uma mensagem de uma determinada classe. Os clientes que permitem que os usuários trabalhem com mensagens pertencentes a uma variedade de classes de mensagens devem ser escritos para lidar com uma variedade de formulários MAPI. Para lidar com vários formulários, os clientes implementam um componente conhecido como visualizador de formulários que contém os três objetos a seguir:
  
- Um objeto de site de mensagem, que oferece suporte à interface [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md) . 
    
- Um coletor de aviso de exibição, que oferece suporte à interface [IMAPIViewAdviseSink: IUnknown](imapiviewadvisesinkiunknown.md) . 
    
- Um objeto de contexto View, que oferece suporte à interface [IMAPIViewContext: IUnknown](imapiviewcontextiunknown.md) . 
    
Cada um desses objetos é usado por um componente chamado servidor de formulário que implementa cada formulário, tratando seu armazenamento e as notificações geradas por clientes que lidam com o modo de exibição. Um outro componente, o provedor de biblioteca de formulários, implementa um gerente de formulários. O Gerenciador de formulários administra as bibliotecas de formulários, que armazenam arquivos executáveis do servidor de formulários. Essa administração inclui o carregamento do servidor de formulário apropriado e a manipulação da comunicação inicial entre o servidor e o cliente.
  
O diagrama a seguir mostra a relação entre um cliente e as outras partes da arquitetura de formulários MAPI.
  
## <a name="mapi-form-architecture"></a>MAPI form architecture
  
![Arquitetura de formulários MAPI] (media/forms01.gif "Arquitetura de formulários MAPI")
  
Se o cliente planeja lidar com formulários MAPI, você usará a interface [IMAPIFormMgr: IUnknown](imapiformmgriunknown.md) do gerente de formulários para executar cinco tarefas básicas: 
  
- Inicie o servidor de formulário MAPI apropriado quando uma mensagem for aberta ou redigida.
    
- Exibir ícones de servidores de formulário nas tabelas de conteúdo das pastas.
    
- Enviar e receber notificações de formulário. Para obter mais informações, consulte [envio e recebimento de notificações de formulário](sending-and-receiving-form-notifications.md).
    
- Permitir que os usuários instalem ou removam servidores de formulários de bibliotecas de formulários. Para obter mais informações, consulte [manutenção de uma biblioteca de formulários](maintaining-a-form-library.md).
    
- Permitir que os usuários associem servidores de formulário a pastas particulares.
    
Para acessar o Gerenciador de formulários, chame a função [MAPIOpenFormMgr](mapiopenformmgr.md) uma vez durante a inicialização. 
  
## <a name="in-this-section"></a>Nesta seção

- [Implementar um visualizador de formulários](implementing-a-form-viewer.md): descreve como implementar um visualizador de formulários usando um coletor de aviso de exibição, um site de mensagens e um contexto de exibição.
    
- [Implementar verbos de formulário padrão](implementing-standard-form-verbs.md): descreve como implementar os verbos para o menu do usuário ou cliques de botão em formulários MAPI.
    
- [Enviar e receber notificações de formulário](sending-and-receiving-form-notifications.md): descreve como enviar e receber notificações de formulário.
    
- [Manutenção de uma biblioteca de formulários](maintaining-a-form-library.md): descreve como manter uma biblioteca que contém todas as informações importantes sobre um formulário.
    
- [Carregar uma mensagem em um formulário](loading-a-message-into-a-form.md): descreve como carregar uma mensagem em um formulário.
    
- [Redigir uma nova mensagem usando um formulário](composing-a-new-message-by-using-a-form.md): descreve como redigir uma mensagem usando um formulário.
    
- [Exibir ícones de formulário](displaying-form-icons.md): descreve as etapas para exibir um ícone com um formulário.
    
## <a name="see-also"></a>Confira também

- [Formulários MAPI](mapi-forms.md)
- [Desenvolver servidores de formulário MAPI](developing-mapi-form-servers.md)

