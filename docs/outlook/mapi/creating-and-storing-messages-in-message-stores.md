---
title: Criar e armazenar mensagens em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cc74b31c-d7ed-4fcf-9535-a2f9222901b7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 32cfae36fb519654c1fb92d2f3b688c966f9288f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766354"
---
# <a name="creating-and-storing-messages-in-message-stores"></a>Criar e armazenar mensagens em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 
  
Como o seu provedor de armazenamento de mensagem cria e armazena mensagens em que o mecanismo de armazenamento subjacente dependem muito o mecanismo de armazenamento subjacente em si. Em geral, você precisa apenas gravar código para preservar as propriedades de uma mensagem e seus valores.
  
Quando a mensagem armazenar provedor cria uma nova mensagem, o provedor precisa criar a mensagem com as propriedades necessárias para mensagens. Uma lista dessas propriedades pode ser encontrada na documentação para o [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interface. Depois disso, os aplicativos cliente adicionam as propriedades adicionais com os métodos [IMAPIProp](imapipropiunknown.md) . 
  
Quando a mensagem armazena provedor salva uma mensagem para o mecanismo de armazenamento subjacente, o provedor precisa iterar sobre as propriedades da mensagem e salvá-los para o mecanismo de armazenamento subjacente, de forma que eles podem ser totalmente recuperados se a mensagem é aberta mais tarde.
  
MAPI exige que as propriedades nas interfaces [IMessage](imessageimapiprop.md) serão transacionadas, o que significa que as alterações feitas a eles não fiquem permanentes até que o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado no objeto de mensagem. O provedor de armazenamento de mensagens é responsável por implementar esse comportamento. Geralmente isso não é difícil; Isso simplesmente significa pressionada propriedades na memória, enquanto eles estão sendo modificados e confirmá-los para o mecanismo de armazenamento subjacente quando **SaveChanges** é chamado. 
  
Algumas propriedades em objetos de mensagem tem semântica especial para aplicativos de cliente com relação ao método **SaveChanges** , da seguinte maneira: 
  
- Algumas propriedades devem ser de leitura/gravação antes **SaveChanges** é chamado, mas somente leitura posteriormente. Por exemplo, **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) é definida inicialmente pelo aplicativo cliente que cria a mensagem (e, portanto, é leitura/gravação), mas não pode ser alterada após a primeira chamada para **SaveChanges**.
    
- Algumas propriedades têm relações especiais às propriedades na pasta que estejam em ou para os métodos **IMAPIFolder** . Por exemplo, a propriedade **PR_MESSAGE_FLAGS** está relacionada aos sinalizadores usados na chamada [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) . 
    
- Algumas propriedades podem não estar disponíveis até que **SaveChanges** é chamado pela primeira vez. Por exemplo, a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) não estejam disponível até que **SaveChanges** seja chamado. 
    
- Algumas propriedades podem ter relacionamentos especiais a outras propriedades no objeto de mensagem. Por exemplo, a propriedade **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) geralmente é derivada da propriedade **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) em provedores de armazenamento de mensagem que oferecem suporte a mensagens de formato Rich Text.
    
- Algumas propriedades são usadas por mais de um tipo de objeto relacionado à mensagem repositórios. Por exemplo, a propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) é necessário em pasta e a mensagem de objetos, bem como a mensagem armazena objetos.
    
É responsabilidade do provedor de repositório de mensagem para implementar a semântica correta para tais propriedades.
  
## <a name="see-also"></a>Confira também



[Implementar mensagens em repositórios de mensagens](implementing-messages-in-message-stores.md)

