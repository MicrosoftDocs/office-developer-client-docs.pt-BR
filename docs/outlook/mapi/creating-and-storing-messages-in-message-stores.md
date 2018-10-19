---
title: Criar e armazenar mensagens em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: be718ea3ef4da91d2f85a0229f5a506198a2527f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589172"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Criar e armazenar mensagens em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Como o seu provedor de repositório de mensagens cria e armazena mensagens no mecanismo de armazenamento subjacente depende fortemente do próprio mecanismo de armazenamento. Em geral, você precisa apenas escrever o código para preservar as propriedades de uma mensagem e seus valores.
  
Quando o provedor de repositório de mensagens cria uma nova mensagem, ele precisa criar a mensagem com as propriedades requeridas para mensagens. Você pode encontrar uma lista dessas propriedades na documentação da interface [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md). Depois disso, os aplicativos clientes acrescentam quaisquer propriedades adicionais com os métodos [IMAPIProp](imapipropiunknown.md). 
  
Quando o provedor de repositório de mensagens salva uma mensagem no mecanismo de armazenamento subjacente, o provedor precisa iterar sobre as propriedades das mensagens e salvá-las no mecanismo de armazenamento subjacente para que possam ser totalmente recuperadas se a mensagem for aberta mais tarde.
  
A MAPI requer que as propriedades nas interfaces [IMessage](imessageimapiprop.md) sejam negociadas, o que significa que as alterações feitas nessas propriedades não se tornem permanentes até que o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado no objeto da mensagem. O provedor de repositório de mensagem é responsável pela implementação desse comportamento. Geralmente, isso não é difícil; significa simplesmente manter as propriedades na memória enquanto elas estão sendo modificadas e confirmá-las para o mecanismo de armazenamento subjacente quando **SaveChanges** for chamado. 
  
Algumas propriedades em objetos de mensagem tem semântica especial para aplicativos clientes em relação ao método **SaveChanges** método, como descrito a seguir: 
  
- Algumas propriedades devem ser de leitura/gravação antes de **SaveChanges** ser chamado, mas do tipo somente leitura depois disso. Por exemplo, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) é definida inicialmente pelo aplicativo cliente que cria a mensagem (sendo assim de leitura/gravação), mas não pode ser alterada depois da primeira chamada para **SaveChanges**.
    
- Algumas propriedades têm relações especiais com propriedades das pastas em que estão ou com métodos **IMAPIFolder**. Por exemplo, a propriedade **PR_MESSAGE_FLAGS** está relacionada com os sinalizadores usados na chamada [IMAPIFolder::CreateMessage](imapifolder-createmessage.md). 
    
- Algumas propriedades podem não estar disponíveis até que **SaveChanges** seja chamado pela primeira vez. Por exemplo, a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) pode não estar disponível até que **SaveChanges** seja chamado. 
    
- Algumas propriedades podem ter relações especiais com outras propriedades do objeto de mensagem. Por exemplo, a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) geralmente deriva da propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) nos provedores de repositório de mensagens que suportam mensagens no Formato Rich Text.
    
- Algumas propriedades são usadas por mais de um tipo de objeto relacionado aos repositórios de mensagens. Por exemplo, a propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) é necessária na pasta e nos objetos de mensagem, bem como nos objetos de repositórios de mensagens.
    
É responsabilidade do provedor de repositórios de mensagem implementar a semântica correta para essas propriedades.
  
## <a name="see-also"></a>Confira também



[Implementar mensagens em repositórios de mensagens](implementing-messages-in-message-stores.md)

