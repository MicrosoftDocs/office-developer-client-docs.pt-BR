---
title: Manipulação de uma mensagem de saída
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ab293ee3813d77c3a954e8364736a89bc2330feb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766663"
---
# <a name="handling-an-outgoing-message"></a>Manipulação de uma mensagem de saída

**Aplica-se a**: Outlook 
  
Uma mensagem de saída é uma mensagem que pode ser enviada para um ou mais destinatários através de um ou mais sistemas de mensagens ou ser remetida para uma pasta em um repositório de mensagem.
  
## <a name="create-and-send-an-outgoing-message"></a>Criar e enviar uma mensagem de saída
  
1. Abra o armazenamento de mensagens padrão. Para obter mais informações, consulte [Abrindo um armazenamento de mensagens](opening-a-message-store.md) e [abrindo o armazenamento de mensagens padrão](opening-the-default-message-store.md).
    
2. Abra a pasta caixa de saída. Para obter mais informações, consulte [Abrir uma pasta de repositório de mensagem](opening-a-message-store-folder.md).
    
3. Chame o método de **IMAPIFolder::CreateMessage** da pasta caixa de saída para criar a nova mensagem. Para obter mais informações, consulte [IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Crie uma lista de destinatários com um ou mais destinatários resolvidos. Para obter mais informações, consulte [criar uma lista do destinatário](creating-a-recipient-list.md).
    
5. Opcionalmente, adicione um assunto. Para obter mais informações, consulte o [tópico Criando um assunto da mensagem](creating-a-message-subject.md).
    
6. Adicione o texto da mensagem. Para obter mais informações, consulte [Criando o texto da mensagem](creating-message-text.md).
    
7. Se o texto da mensagem estiver formatado, adicione as informações de renderização. Para obter mais informações, consulte [Adicionando informações de renderização em texto formatado](adding-rendering-information-to-formatted-text.md).
    
8. Opcionalmente, adicione um ou mais anexos. Para obter mais informações, consulte [Criando um anexo da mensagem](creating-a-message-attachment.md).
    
9. Definir outras propriedades de mensagem conforme desejado e, em seguida, salvar e enviar a mensagem chamando **IMessage::SubmitMessage**. Para obter mais informações, consulte [IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Excluir a mensagem enviada, se o **PR\_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) propriedade é definida como TRUE, ou mover para a pasta identificada pela propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Para obter mais informações, consulte o [processamento de uma mensagem enviada](processing-a-sent-message.md).
    
Se você quiser intermittantly salve a mensagem antes de enviá-lo, chame o método de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) da mensagem. Para obter mais informações, consulte, [Salvando uma mensagem](saving-a-message.md) ou [Enviar uma mensagem](sending-a-message.md). 
  
## <a name="in-this-section"></a>Nesta seção

- [Criar uma lista de destinatário](creating-a-recipient-list.md): descreve como criar uma lista de destinatários.
    
- [Criando um assunto da mensagem](creating-a-message-subject.md): descreve como criar um assunto opcional para uma mensagem.
    
- [Criando o texto da mensagem](creating-message-text.md): descreve como criar o texto da mensagem.
    
- [Adicionando informações de renderização em texto formatado](adding-rendering-information-to-formatted-text.md): descreve onde um anexo em texto não formatado é a ser renderizado.
    
- [Criando um anexo de mensagem](creating-a-message-attachment.md): descreve como criar anexos.
    
- [Salvando uma mensagem](saving-a-message.md): descreve como os clientes salvar mensagens.
    
- [Enviar uma mensagem](sending-a-message.md): descreve como enviar uma mensagem.
    
- [Processamento de uma mensagem enviada](processing-a-sent-message.md): descreve como enviadas as mensagens podem ser processadas.
    

