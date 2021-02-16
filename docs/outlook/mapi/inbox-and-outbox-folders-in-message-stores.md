---
title: Pastas de Caixa de Entrada e Caixa de Saída em Armazenamentos de Mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8e4ce129-137d-4618-80a6-88781a578d01
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 95a2b7b9bac11404817fb6848d58c45251c141f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414239"
---
# <a name="inbox-and-outbox-folders-in-message-stores"></a>Pastas de Caixa de Entrada e Caixa de Saída em Armazenamentos de Mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para ser o armazenamento de mensagens padrão, um provedor de armazenamento de mensagens deve implementar as pastas Caixa de Entrada e Caixa de Saída. Eles geralmente são armazenados na subárvore do IPM de um armazenamento de mensagens. Essas pastas são especiais porque são designadas como as pastas de onde as mensagens são entregues e enviadas, mas nenhuma funcionalidade especial é necessária delas. O envio e o recebimento de mensagens ocorrem por meio de sequências de chamada definidas entre aplicativos cliente, o spooler MAPI e o provedor de armazenamento de mensagens. As pastas Caixa de Entrada e Caixa de Saída são simplesmente pastas usadas para manter mensagens durante essas sequências de chamada. O ponto importante não é que as pastas sejam especiais ou até mesmo nomeadas Caixa de Entrada e Caixa de Saída; o ponto importante é que o provedor de armazenamento de mensagens os usa como parte de seu suporte para envio e recebimento de mensagens.
  
Para dar suporte ao recebimento de mensagens, o provedor de repositório de mensagens deve implementar os métodos [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) e [IMsgStore::GetReceiveFolder.](imsgstore-getreceivefolder.md) Para obter mais informações, consulte [Recebimento de mensagens usando provedores de armazenamento de mensagens.](receiving-messages-by-using-message-store-providers.md)
  
Para dar suporte ao envio de mensagens, o provedor de repositório de mensagens deve suportar o método [IMsgStore::GetOutgoingQueue,](imsgstore-getoutgoingqueue.md) além dos outros métodos usados pelo spooler MAPI durante o processo de envio de mensagens. A fila de saída de um armazenamento de mensagens não precisa corresponder a uma pasta real em qualquer lugar na árvore de pastas do armazenamento de mensagens. No entanto, é personalizado para um provedor de armazenamento de mensagens mostrar o conteúdo da fila de mensagens de saída na pasta Caixa de Saída, se houver um. Isso oferece aos aplicativos cliente uma maneira conveniente de indicar o status das mensagens que o usuário enviou, porque uma pasta de Caixa de Saída pode ser exibida junto com todas as outras pastas em um armazenamento de mensagens. Para obter mais informações, consulte [Enviando Mensagens Usando Provedores de Armazenamento de Mensagens.](sending-messages-by-using-message-store-providers.md)
  
## <a name="see-also"></a>Confira também



[Implementar pastas em repositórios de mensagens](implementing-folders-in-message-stores.md)

