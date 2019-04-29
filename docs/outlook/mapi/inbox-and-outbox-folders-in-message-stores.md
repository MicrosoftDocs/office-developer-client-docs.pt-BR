---
title: Pastas de caixa de correio e caixa de saída em repositórios de mensagens
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
# <a name="inbox-and-outbox-folders-in-message-stores"></a>Pastas de caixa de correio e caixa de saída em repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para ser o repositório de mensagens padrão, um provedor de repositório de mensagens deve implementar as pastas caixa de correio e caixa de saída. Normalmente, eles são armazenados na subárvore IPM de um repositório de mensagens. Essas pastas são especiais, pois são designadas como as pastas nas quais as mensagens são entregues e enviadas, mas nenhuma funcionalidade especial é necessária. Enviar e receber mensagens ocorre por meio de sequências de chamadas definidas entre aplicativos clientes, o spooler MAPI e o provedor de repositório de mensagens. As pastas caixa de entrada e caixa de saída são apenas pastas que são usadas para armazenar mensagens durante essas sequências de chamadas. O ponto importante não é que as pastas sejam especiais ou até que sejam nomeadas como caixa de entrada e caixa de saída; o ponto importante é que o provedor de armazenamento de mensagens o utiliza como parte de seu suporte para enviar e receber mensagens.
  
Para dar suporte ao recebimento de mensagens, o provedor de repositório de mensagens deve implementar os métodos [IMsgStore:: GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) e [IMsgStore:: GetReceiveFolder](imsgstore-getreceivefolder.md) . Para obter mais informações, consulte [recebendo mensagens usando provedores de repositório de mensagens](receiving-messages-by-using-message-store-providers.md).
  
Para dar suporte ao envio de mensagens, o provedor de repositório de mensagens deve suportar o método [IMsgStore:: GetOutgoingQueue](imsgstore-getoutgoingqueue.md) , além dos outros métodos usados pelo spooler MAPI durante o processo de envio de mensagens. Uma fila de saída do repositório de mensagens não precisa corresponder a uma pasta real em qualquer lugar na árvore de pastas do repositório de mensagens. No enTanto, é personalizado que um provedor de repositório de mensagens mostre o conteúdo da fila de mensagens de saída na pasta de saída, se houver uma. Isso fornece aos aplicativos cliente uma maneira conveniente de indicar o status das mensagens que o usuário enviou, pois uma pasta de saída pode ser exibida junto com todas as outras pastas em um repositório de mensagens. Para obter mais informações, consulte [enviando mensagens usando provedores de repositório de mensagens](sending-messages-by-using-message-store-providers.md).
  
## <a name="see-also"></a>Confira também



[Implementar pastas em repositórios de mensagens](implementing-folders-in-message-stores.md)

