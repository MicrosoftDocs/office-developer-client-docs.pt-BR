---
title: Manipular uma mensagem de saída
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f40c2e0b-1a35-4901-868f-af6c191c921e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 07785ac82c41108b4333b3c370e3d2f5bfd1426a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407624"
---
# <a name="handling-an-outgoing-message"></a>Manipular uma mensagem de saída

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma mensagem de saída é uma mensagem que pode ser enviada para um ou mais destinatários em um ou mais sistemas de mensagens ou ser postada em uma pasta em um armazenamento de mensagens.
  
## <a name="create-and-send-an-outgoing-message"></a>Criar e enviar uma mensagem de saída
  
1. Abra o armazenamento de mensagens padrão. Para obter mais informações, consulte [Abrindo um armazenamento de mensagens](opening-a-message-store.md) e abrindo o armazenamento de mensagens [padrão.](opening-the-default-message-store.md)
    
2. Abra a pasta Caixa de Saída. Para obter mais informações, consulte [Abrindo uma pasta do armazenamento de mensagens.](opening-a-message-store-folder.md)
    
3. Chame o método **IMAPIFolder::CreateMessage** da pasta outbox para criar a nova mensagem. Para obter mais informações, [consulte IMAPIFolder::CreateMessage](imapifolder-createmessage.md),
    
4. Crie uma lista de destinatários com um ou mais destinatários resolvidos. Para obter mais informações, consulte [Criando uma lista de destinatários.](creating-a-recipient-list.md)
    
5. Opcionalmente, adicione um assunto. Para obter mais informações, consulte [Criando um assunto de mensagem.](creating-a-message-subject.md)
    
6. Adicione o texto da mensagem. Para obter mais informações, consulte [Criando texto da mensagem.](creating-message-text.md)
    
7. Se o texto da mensagem estiver formatado, adicione informações de renderização. Para obter mais informações, consulte [Adicionando informações de renderização ao texto formatado.](adding-rendering-information-to-formatted-text.md)
    
8. Opcionalmente, adicione um ou mais anexos. Para obter mais informações, consulte [Criando um anexo de mensagem.](creating-a-message-attachment.md)
    
9. Definir outras propriedades de mensagem conforme desejado e salvar e enviar a mensagem chamando **IMessage::SubmitMessage**. Para obter mais informações, consulte [IMessage::SubmitMessage](imessage-submitmessage.md).
    
10. Exclua a mensagem enviada se a propriedade **PR \_ DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) estiver definida como TRUE ou movê-la para a pasta identificada pela propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Para obter mais informações, [consulte Processing a Sent Message](processing-a-sent-message.md).
    
Se você quiser salvar intermitentemente a mensagem antes de enviá-la, chame o método [IMAPIProp::SaveChanges da](imapiprop-savechanges.md) mensagem. Para obter mais informações, consulte, [Salvar uma mensagem](saving-a-message.md) ou enviar uma [mensagem.](sending-a-message.md) 
  
## <a name="in-this-section"></a>Nesta seção

- [Criando uma lista de](creating-a-recipient-list.md)destinatários: descreve como criar uma lista de destinatários.
    
- [Criando um assunto de](creating-a-message-subject.md)mensagem: descreve como criar um assunto opcional para uma mensagem.
    
- [Criando texto da](creating-message-text.md)mensagem: descreve como criar o texto da mensagem.
    
- [Adicionando informações de renderização ao texto formatado:](adding-rendering-information-to-formatted-text.md)descreve onde em texto formatado um anexo deve ser renderizado.
    
- [Criando um anexo de](creating-a-message-attachment.md)mensagem: descreve como criar anexos.
    
- [Salvar uma mensagem:](saving-a-message.md)descreve como os clientes salvam mensagens.
    
- [Enviar uma mensagem:](sending-a-message.md)descreve como enviar uma mensagem.
    
- [Processing a Sent Message](processing-a-sent-message.md): Describes how to sent messages can be processed.
    

