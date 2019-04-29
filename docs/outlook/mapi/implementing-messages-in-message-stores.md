---
title: Implementar mensagens em repositórios de mensagens
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
# <a name="implementing-messages-in-message-stores"></a>Implementar mensagens em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A interface [IMessage: IMAPIProp](imessageimapiprop.md) é semelhante à interface [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) em que ambas as interfaces derivam da interface [IMAPIProp: IUnknown](imapipropiunknown.md) . Os clientes usam os métodos **IMAPIProp** para acessar o conteúdo de uma mensagem. A interface **IMessage** fornece métodos adicionais para a manipulação de mensagens (por exemplo, adição de anexos ou modificação dos destinatários de uma mensagem). Os métodos na interface **IMessage** modificam atributos de mensagens que não são armazenadas diretamente nas propriedades da mensagem. 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

