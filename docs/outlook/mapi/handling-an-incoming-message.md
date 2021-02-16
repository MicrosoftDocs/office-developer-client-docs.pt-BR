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
  
Uma mensagem de entrada é uma mensagem que foi enviada por um ou mais sistemas de mensagens. Ele pode ter sido enviado apenas para você ou para muitos outros destinatários. As mensagens de entrada são colocadas em uma pasta de recebimento designada para manter mensagens de uma classe específica. Você pode configurar uma pasta de recebimento diferente para cada classe de mensagem que manipular ou usar uma pasta para todas as classes.
  
Se você tiver se registrado para novas notificações de email com o armazenamento de mensagens, você será notificado sempre que uma mensagem for colocada em uma pasta de recebimento. Se você não tiver se registrado para novas notificações de email, deverá abrir a pasta de recebimento apropriada periodicamente para verificar manualmente a chegada de novas mensagens.
  
Os clientes se registram para novas notificações de email definindo os parâmetros como [IMsgStore::Advise](imsgstore-advise.md) da seguinte forma: 
  
- De  _definida cbEntryID_ como 0. 
    
- De  _definida lpEntryID_ como NULL. 
    
- De  _definir ulEventMask_ como fnevNewMail. 
    
O parâmetro _lpNotifications_ na chamada para seu método **IMAPIAdviseSink::OnNotify** aponta para uma estrutura NOTIFICAÇÃO **DE NEWMAIL \_** que contém informações sobre a mensagem de entrada, como sua classe de mensagem, seu identificador de entrada, o identificador de entrada de sua pasta pai e o conteúdo de sua propriedade **PR_MESSAGE_FLAGS.** Para obter mais informações sobre como registrar e manipular notificações, consulte [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) e Manipulando notificações [.](handling-notifications.md) 
  
Antes de exibir uma mensagem de entrada para um usuário, determine se sua classe de mensagem é uma classe compatível com seu cliente. Caso não seja, ignore a mensagem. Se a classe for aquela à qual você dá suporte, você poderá abrir e exibir a mensagem com um formulário apropriado para a classe de mensagem da mensagem. A escolha de formulários baseia-se na classe da mensagem. Mensagens que pertencem à classe IPM usam um formulário padrão implementado por MAPI. Mensagens que pertencem a classes personalizadas definidas por clientes podem usar formulários especializados definidos pelo cliente ou o formulário padrão MAPI.
  
## <a name="open-and-display-an-incoming-message"></a>Abrir e exibir uma mensagem de entrada
  
1. Chame **IMsgStore::GetReceiveFolder** para recuperar o identificador de entrada da pasta de recebimento da classe de mensagem da mensagem e passe esse identificador de entrada para **IMsgStore::OpenEntry** para abrir a pasta. For more information, see [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md), and [Opening a Message Store Folder](opening-a-message-store-folder.md).
    
2. Chame o método **IMAPIContainer::GetContentsTable** da pasta de recebimento para recuperar sua tabela de conteúdo. Para obter mais informações, consulte [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Chame o método **IMAPITable::QueryRows** da tabela para recuperar todas as linhas da tabela. Para obter mais informações, [consulte IMAPITable::QueryRows](imapitable-queryrows.md) and [Contents Tables](contents-tables.md). Para obter mais informações sobre a exibição de uma tabela de conteúdos, consulte [Exibindo uma tabela de conteúdo de pasta.](displaying-a-folder-contents-table.md)
    
3. Se o cliente for interativo, permita que o usuário selecione uma mensagem da tabela e determine o formulário a ser usado para exibir essa mensagem. Os clientes podem usar o formulário padrão fornecido por MAPI ou um formulário personalizado. Para obter mais informações, consulte [Manipulando formulários MAPI.](handling-mapi-forms.md)
    
4. Chame **IMsgStore::OpenEntry** para abrir a mensagem. Para obter mais informações, consulte [Abrindo uma mensagem.](opening-a-message.md)
    
5. Processe o texto da mensagem. Para obter mais informações, consulte [Opening Message Text](opening-message-text.md).
    
6. Renderizar cada um dos anexos da mensagem. Para obter mais informações, consulte [Renderização de](rendering-an-attachment-in-plain-text.md) um anexo em texto sem texto ou [renderização de um anexo em texto RTF.](rendering-an-attachment-in-rtf-text.md)
    
7. Abra um anexo, se desejado. Para obter mais informações, [consulte Abrindo um anexo.](opening-an-attachment.md)
    
## <a name="in-this-section"></a>Nesta seção

- [Abrir Texto da](opening-message-text.md)Mensagem: Descreve como abrir o texto da mensagem.
    
- [Renderização de um anexo em texto sem](rendering-an-attachment-in-plain-text.md)texto: descreve como renderizar um anexo em texto sem forma.
    
- [Renderização de um anexo em texto RTF:](rendering-an-attachment-in-rtf-text.md)descreve como renderizar um anexo em texto formatado.
    
- [Abrir um anexo:](opening-an-attachment.md)descreve como abrir um anexo.
    

