---
title: Pastas de caixa de entrada e caixa de saída em repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2bd71ee4fca53fbf3d309cbaf9d33835b84c0c2d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767553"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a>Pastas de caixa de entrada e caixa de saída em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 
  
Para ser o armazenamento de mensagens padrão, um provedor de armazenamento de mensagem deve implementar a caixa de entrada e pastas da caixa de saída. Normalmente, elas são armazenadas em subárvore IPM um armazenamento de mensagens. Essas pastas são especiais em que eles são designados como as pastas que as mensagens são entregues e enviadas de, mas nenhuma funcionalidade especial é exigida deles. Enviando e recebendo mensagens acontece por meio de sequências de chamada definidas entre aplicativos de cliente, o spooler MAPI e o provedor de armazenamento de mensagem. As pastas de caixa de entrada e caixa de saída são simplesmente as pastas que são usadas para armazenar mensagens durante as sequências de chamadas. Não, o importante é que as pastas são especiais ou até mesmo que eles são chamados de entrada e saída; o importante é que o provedor de armazenamento de mensagem usa-los como parte de seu suporte para envio e recebimento de mensagens.
  
Para suportar o recebimento de mensagens, o provedor de armazenamento de mensagem deve implementar os métodos [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) e [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) . Para obter mais informações, consulte o [Recebimento de mensagens por provedores de repositório de mensagem usando](receiving-messages-by-using-message-store-providers.md).
  
Para suportar o envio de mensagens, o provedor de armazenamento de mensagem deve oferecer suporte ao método [IMsgStore::GetOutgoingQueue](imsgstore-getoutgoingqueue.md) , além de outros métodos usados pelo spooler MAPI durante a mensagem enviando o processo. Fila de saída de um repositório mensagem não tem para que corresponda a uma pasta real em qualquer lugar na árvore de pastas do armazenamento de mensagens. No entanto, é comum para um provedor de armazenamento de mensagem mostrar o conteúdo da fila de mensagens de saída na pasta caixa de saída, se houver uma. Isso oferece aplicativos cliente uma maneira conveniente para indicar o status de mensagens que o usuário tiver enviado, porque uma pasta caixa de saída pode ser exibida junto com todas as outras pastas em um armazenamento de mensagens. Para obter mais informações, consulte [Enviando mensagens por provedores de repositório de mensagem usando](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Confira também



[Implementar pastas em repositórios de mensagens](implementing-folders-in-message-stores.md)

