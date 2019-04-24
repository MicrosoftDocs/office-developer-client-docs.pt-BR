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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342802"
---
# <a name="handling-an-outgoing-message"></a>Manipular uma mensagem de saída

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma mensagem de saída é uma mensagem que pode ser enviada a um ou mais destinatários em um ou mais sistemas de mensagens ou ser publicada em uma pasta em um repositório de mensagens.
  
## <a name="create-and-send-an-outgoing-message"></a>Criar e enviar uma mensagem de saída
  
1. Abra o repositório de mensagens padrão. Para obter mais informações, consulte [abrir um repositório de mensagens](opening-a-message-store.md) e [abrir o repositório de mensagens padrão](opening-the-default-message-store.md).
    
2. Abra a pasta de saída. Para obter mais informações, consulte [abrir uma pasta de armazenamento de mensagens](opening-a-message-store-folder.md).
    
3. Chame o método **IMAPIFolder:: CreateMessage** da pasta de saída para criar a nova mensagem. Para obter mais informações, consulte [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md),
    
4. Criar uma lista de destinatários com um ou mais destinatários resolvidos. Para obter mais informações, consulte [Creating a Recipient List](creating-a-recipient-list.md).
    
5. Opcionalmente, adicione um assunto. Para obter mais informações, consulte [Creating a Message Subject](creating-a-message-subject.md).
    
6. Adicione o texto da mensagem. Para obter mais informações, consulte [Creating Message Text](creating-message-text.md).
    
7. Se o texto da mensagem estiver formatado, adicione informações de renderização. Para obter mais informações, consulte [adicionando informações de renderização ao texto formatado](adding-rendering-information-to-formatted-text.md).
    
8. Opcionalmente, adicione um ou mais anexos. Para obter mais informações, consulte [Creating a Message Attachment](creating-a-message-attachment.md).
    
9. Defina outras propriedades de mensagem conforme desejado e, em seguida, salve e envie a mensagem chamando **IMessage:: SubmitMessage**. Para obter mais informações, consulte [IMessage:: SubmitMessage](imessage-submitmessage.md).
    
10. Exclua a mensagem enviada se **a\_Propriedade PR DELETE_AFTER_SUBMIT** ([PIDTAGDELETEAFTERSUBMIT](pidtagdeleteaftersubmit-canonical-property.md)) estiver definida como true ou mova-a para a pasta identificada pela propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)). Para obter mais informações, consulte [processamento de uma mensagem enviada](processing-a-sent-message.md).
    
Se você quiser que o intermittantly salve a mensagem antes de enviá-la, chame o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) da mensagem. Para obter mais informações, consulte [salvando uma mensagem](saving-a-message.md) ou [enviando uma mensagem](sending-a-message.md). 
  
## <a name="in-this-section"></a>Nesta seção

- [Criar uma lista de destinatários](creating-a-recipient-list.md): descreve como criar uma lista de destinatários.
    
- [Criar um assunto da mensagem](creating-a-message-subject.md): descreve como criar um assunto opcional para uma mensagem.
    
- [Criando texto da mensagem](creating-message-text.md): descreve como criar o texto da mensagem.
    
- [Adicionar informações de renderização ao texto formatado](adding-rendering-information-to-formatted-text.md): descreve onde no texto formatado um anexo deve ser renderizado.
    
- [Criar um anexo de mensagem](creating-a-message-attachment.md): descreve como criar anexos.
    
- [Salvar uma mensagem](saving-a-message.md): descreve como os clientes salvam mensagens.
    
- [Enviando uma mensagem](sending-a-message.md): descreve como enviar uma mensagem.
    
- [Processamento de uma mensagem enviada](processing-a-sent-message.md): descreve como enviar mensagens que podem ser processadas.
    

