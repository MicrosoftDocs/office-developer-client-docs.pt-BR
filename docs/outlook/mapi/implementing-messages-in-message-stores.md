---
title: Implementar mensagens em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1d68a5258739a8952df97ddceb07ebe6d9c8d2d7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568124"
---
# <a name="implementing-messages-in-message-stores"></a>Implementar mensagens em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O [IMessage: IMAPIProp](imessageimapiprop.md) interface é semelhante do [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interface nessa derivam de ambas as interfaces do [IMAPIProp: IUnknown](imapipropiunknown.md) interface. Clientes usam os métodos **IMAPIProp** para acessar o conteúdo de uma mensagem. A interface **IMessage** fornece métodos adicionais para a manipulação de mensagens (por exemplo, a adição de anexos ou modificar os destinatários de uma mensagem). Os métodos na interface do **IMessage** modificam atributos de mensagens que não são armazenadas diretamente nas propriedades da mensagem. 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

