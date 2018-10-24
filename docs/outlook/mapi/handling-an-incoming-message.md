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
ms.openlocfilehash: d6ec40005683cc67c51a63d6b186c042c8e170d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568172"
---
# <a name="handling-an-incoming-message"></a>Manipular uma mensagem de entrada

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma mensagem de entrada é uma mensagem que foi enviada entre um ou mais sistemas de mensagens. Ele pode ter sido enviado apenas para você ou para muitos outros destinatários. Mensagens de entrada são colocadas em uma pasta de recebimento designada para manter as mensagens de uma determinada classe. Você pode configurar a pasta para cada classe de mensagem que você deseja tratar ou usa uma pasta para todas as classes de receber uma diferente.
  
Se você registrou para novas notificações de email com o armazenamento de mensagens, você será notificado sempre que uma mensagem é colocada em uma pasta de recebimento. Se você não tiver registrado para novas notificações de email, é necessário abrir o apropriado receber pasta periodicamente para verificar manualmente a chegada de novas mensagens.
  
Registrar clientes para novas notificações de email, definindo os parâmetros para [IMsgStore::Advise](imsgstore-advise.md) da seguinte maneira: 
  
- Defina _cbEntryID_ como 0. 
    
- Defina _lpEntryID_ como NULL. 
    
- Defina _ulEventMask_ como fnevNewMail. 
    
O parâmetro _lpNotifications_ na chamada para seu método **IMAPIAdviseSink::OnNotify** aponta para um **NEWMAIL\_notificação** estrutura que contém informações sobre a mensagem de entrada, como sua classe de mensagem, sua entrada identificador, o identificador de entrada da sua pasta pai e o conteúdo de sua propriedade **PR_MESSAGE_FLAGS** . Para obter mais informações sobre como registrar para e manipular notificações, consulte [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md), [NEWMAIL_NOTIFICATION](newmail_notification.md), **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) e [Tratamento de notificações](handling-notifications.md). 
  
Antes de exibir uma mensagem de entrada para um usuário, determine se sua classe de mensagem é uma classe que ofereça suporte a seu cliente. Caso contrário, ignore a mensagem. Se a classe é um suportado, você pode abrir e exibir a mensagem com um formulário que é apropriado para a classe de mensagem da mensagem. A opção de formulários baseia-se na classe da mensagem. As mensagens que pertencem à classe IPM usam um formulário padrão implementado pelo MAPI. Mensagens que pertencem a classes personalizadas definidas por clientes podem usar formulários especializados definida pelo cliente ou o formulário padrão MAPI.
  
## <a name="open-and-display-an-incoming-message"></a>Abre e exibe uma mensagem de entrada
  
1. Chame **IMsgStore::GetReceiveFolder** para recuperar o identificador de entrada da pasta de recebimento para a classe de mensagem da mensagem e passar esse identificador de entrada para **IMsgStore::OpenEntry** para abrir a pasta. Para obter mais informações, consulte [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md), [IMsgStore::OpenEntry](imsgstore-openentry.md)e [Abrir uma pasta de repositório de mensagem](opening-a-message-store-folder.md).
    
2. Chame o método de **IMAPIContainer::GetContentsTable** de recebimento da pasta para recuperar sua tabela de conteúdo. Para obter mais informações, consulte [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md). Chame o método da tabela **IMAPITable:: QueryRows** para recuperar todas as linhas na tabela. Para obter mais informações, consulte [IMAPITable:: QueryRows](imapitable-queryrows.md) e [Tabelas de conteúdo](contents-tables.md). Para obter mais informações sobre a exibição de uma tabela de conteúdo, consulte [exibindo uma tabela de conteúdo de pasta](displaying-a-folder-contents-table.md).
    
3. Se seu cliente for interativo, permitir que o usuário selecione uma mensagem da tabela e determinar o formato a ser usado para exibir a mensagem. Os clientes podem usar o formulário padrão fornecido pelo MAPI ou um formulário personalizado. Para obter mais informações, consulte [Manipulação de formulários de MAPI](handling-mapi-forms.md).
    
4. Chame **IMsgStore::OpenEntry** para abrir a mensagem. Para obter mais informações, consulte [abrindo uma mensagem](opening-a-message.md).
    
5. Processe o texto da mensagem. Para obter mais informações, consulte o [Texto da mensagem de abertura](opening-message-text.md).
    
6. Renderize cada anexos da mensagem. Para obter mais informações, consulte a [renderização de um anexo em texto sem formatação](rendering-an-attachment-in-plain-text.md) ou [renderização de um anexo em texto RTF](rendering-an-attachment-in-rtf-text.md).
    
7. Abra um anexo, se desejado. Para obter mais informações, consulte [abertura de um anexo](opening-an-attachment.md).
    
## <a name="in-this-section"></a>Nesta seção

- [Texto da mensagem de abertura](opening-message-text.md): descreve como abrir o texto da mensagem.
    
- [Renderização de um anexo em texto não criptografado](rendering-an-attachment-in-plain-text.md): descreve como a renderização de um anexo em texto sem formatação.
    
- [Renderização de um anexo em texto RTF](rendering-an-attachment-in-rtf-text.md): descreve como um anexo de renderização em texto não formatado.
    
- [Abertura de um anexo](opening-an-attachment.md): descreve como abrir um anexo.
    

