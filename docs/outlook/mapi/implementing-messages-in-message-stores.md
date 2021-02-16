---
title: Implementando mensagens em armazenamentos de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 223dfa2ac990875e98e876ab491bf09caf63e874
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416640"
---
# <a name="implementing-messages-in-message-stores"></a>Implementando mensagens em armazenamentos de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
The [IMessage : IMAPIProp](imessageimapiprop.md) interface is similar to the [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) interface in that both interfaces derive from the [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Os clientes usam **os métodos IMAPIProp** para acessar o conteúdo de uma mensagem. A interface **IMessage** fornece métodos adicionais para manipular mensagens (por exemplo, adicionar anexos ou modificar os destinatários de uma mensagem). Os métodos na interface **IMessage** modificam atributos de mensagens que não são armazenados diretamente nas propriedades da mensagem. 
  
## <a name="see-also"></a>Confira também



[Recursos do Armazenamento de Mensagens](message-store-features.md)

