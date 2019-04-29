---
title: Manipular uma mensagem de entrada
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d45d5ed9-41cd-4aaf-91d2-1e4a27bb16d4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f3fbe34793e3520b26b984f4bd6b14fbcab7a951
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438978"
---
# <a name="handling-an-incoming-message"></a>Manipular uma mensagem de entrada

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma mensagem de entrada é uma mensagem que foi enviada por um ou mais sistemas de mensagens. Ele pode ter sido enviado apenas para você ou para muitos outros destinatários. As mensagens de entrada são colocadas em uma pasta de recebimento designada para armazenar mensagens de uma determinada classe. Você pode configurar uma pasta de recebimento diferente para cada classe de mensagem que você manipula ou usa uma pasta para todas as classes.
  
Se você tiver registrado para novas notificações de email com o repositório de mensagens, será notificado sempre que uma mensagem for colocada em uma pasta de recebimento. Se você não tiver registrado para novas notificações de email, deverá abrir a pasta de recebimento apropriada periodicamente para verificar manualmente a chegada de novas mensagens.
  
Os clientes se registram para novas notificações de email Configurando os parâmetros para [IMsgStore:: Advise](imsgstore-advise.md) da seguinte maneira: 
  
- Defina _cbEntryID_ como 0. 
    
- Defina _lpEntryID_ como nulo. 
    
- Defina _ulEventMask_ como fnevNewMail. 
    
O parâmetro _lpNotifications_ na chamada para o método **IMAPIAdviseSink:: OnNotify** aponta para uma estrutura de **notificação do NEWMAIL\_** que contém informações sobre a mensagem de entrada, como sua classe de mensagens, sua entrada identificador, o identificador de entrada de sua pasta pai e o conteúdo de sua propriedade **PR_MESSAGE_FLAGS** . Para obter mais informações sobre como registrar e lidar com notificações, consulte [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) e [tratamento de notificações](handling-notifications.md). 
  
Antes de exibir uma mensagem de entrada para um usuário, determine se sua classe de mensagem é uma classe que seu cliente suporta. Caso contrário, ignore a mensagem. Se a classe é suportada, você pode abrir e exibir a mensagem com um formulário apropriado para a classe de mensagem da mensagem. A opção de formulários é baseada na classe da mensagem. As mensagens que pertencem à classe IPM usam um formulário padrão implementado por MAPI. As mensagens que pertencem a classes personalizadas definidas por clientes podem usar formulários especializados definidos pelo cliente ou o formulário MAPI padrão.
  
## <a name="open-and-display-an-incoming-message"></a>Abrir e exibir uma mensagem de entrada
  
1. Chame **IMsgStore:: GetReceiveFolder** para recuperar o identificador de entrada da pasta de recebimento para a classe de mensagem da mensagem e passar esse identificador de entrada para **IMsgStore:: OpenEntry** para abrir a pasta. Para obter mais informações, consulte [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore:: OpenEntry](imsgstore-openentry.md)e [abrindo uma pasta do repositório de mensagens](opening-a-message-store-folder.md).
    
2. Chame o método **IMAPIContainer::** getcontenttable da pasta de recebimento para recuperar sua tabela de conteúdo. Para obter mais informações, consulte [IMAPIContainer::](imapicontainer-getcontentstable.md)getcontenttable. Chame o método imApitable **:: QueryRows** da tabela para recuperar todas as linhas da tabela. Para obter mais informações, consulte imApitable [:: QueryRows](imapitable-queryrows.md) e [Content Tables](contents-tables.md). Para obter mais informações sobre como exibir uma tabela de conteúdo, consulte [exibindo uma tabela de conteúdo da pasta](displaying-a-folder-contents-table.md).
    
3. Se o cliente for interativo, permita que o usuário selecione uma mensagem da tabela e determine o formulário a ser usado para exibir a mensagem. Os clientes podem usar o formulário padrão fornecido por MAPI ou um formulário personalizado. Para obter mais informações, consulte [tratamento de formulários MAPI](handling-mapi-forms.md).
    
4. Chame **IMsgStore:: OpenEntry** para abrir a mensagem. Para obter mais informações, consulte [abrir uma mensagem](opening-a-message.md).
    
5. Processe o texto da mensagem. Para obter mais informações, consulte [abrindo mensagem de texto](opening-message-text.md).
    
6. Renderizar cada um dos anexos da mensagem. Para obter mais informações, consulte [renderizar um anexo em texto sem formatação](rendering-an-attachment-in-plain-text.md) ou [renderizar um anexo em texto RTF](rendering-an-attachment-in-rtf-text.md).
    
7. Abra um anexo, se desejado. Para obter mais informações, consulte [abrir um anexo](opening-an-attachment.md).
    
## <a name="in-this-section"></a>Nesta seção

- [Abrindo mensagem texto](opening-message-text.md): descreve como abrir o texto da mensagem.
    
- [Renderizar um anexo em texto sem formatação](rendering-an-attachment-in-plain-text.md): descreve como renderizar um anexo em texto sem formatação.
    
- [Renderizar um anexo em texto RTF](rendering-an-attachment-in-rtf-text.md): descreve como renderizar um anexo em texto formatado.
    
- [Abrir um anexo](opening-an-attachment.md): descreve como abrir um anexo.
    

