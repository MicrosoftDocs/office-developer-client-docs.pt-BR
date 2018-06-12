---
title: Implementando mensagens em repositórios de mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: df5003d5-cbfe-40b2-a481-e2e11dce4b3e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c21fea9b0c8de96f427c4bcdfabfde3a0032f0c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767434"
---
# <a name="implementing-messages-in-message-stores"></a>Implementando mensagens em repositórios de mensagem

  
  
**Aplica-se a**: Outlook 
  
O [IMessage: IMAPIProp](imessageimapiprop.md) interface é semelhante do [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) interface nessa derivam de ambas as interfaces do [IMAPIProp: IUnknown](imapipropiunknown.md) interface. Clientes usam os métodos **IMAPIProp** para acessar o conteúdo de uma mensagem. A interface **IMessage** fornece métodos adicionais para a manipulação de mensagens (por exemplo, a adição de anexos ou modificar os destinatários de uma mensagem). Os métodos na interface do **IMessage** modificam atributos de mensagens que não são armazenadas diretamente nas propriedades da mensagem. 
  
## <a name="see-also"></a>Confira também



[Recursos de armazenamento de mensagens](message-store-features.md)

