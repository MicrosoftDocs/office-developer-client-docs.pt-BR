---
title: Enviar mensagens usando MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3edfbfff-ea15-4926-bf0f-47137251d921
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: bf6324b89f06ef7f0553d3de1eaa24ae31a329ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438719"
---
# <a name="sending-messages-by-using-mapi"></a>Enviar mensagens usando MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente chamam [o método IMessage::SubmitMessage](imessage-submitmessage.md) para enviar uma mensagem. **SubmitMessage** chama [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvar a mensagem antes de transferir o controle para o spooler MAPI ou diretamente para um provedor de transporte. 
  
O spooler MAPI receberá a mensagem se qualquer uma das seguintes condições ocorrer:
  
- O provedor de armazenamento de mensagens e o provedor de transporte não estão fortemente unidos.
    
- A mensagem requer pré-processamento.
    
- O armazenamento e o transporte de mensagens fortemente a par não podem lidar com todos os destinatários aos quais a mensagem é endereçada.
    
Um armazenamento de mensagens fortemente a par deve levar em conta o status de uma mensagem antes de apresenta-la ao spooler MAPI a ser baixado para um provedor de transporte. Há situações em que uma mensagem pode parecer exigir o spooler MAPI, mas o spooler MAPI realmente não deve estar envolvido.
  
Por exemplo, considere a situação em que um usuário envia uma mensagem da Caixa de Entrada. O cliente está usando um armazenamento e transporte fortemente próximos. Se o armazenamento de mensagens fortemente a par usa a localização da mensagem como o único critério para decidir se o spooler MAPI deve ou não manipular a mensagem, o spooler MAPI sempre receberá a mensagem. Para evitar esse tipo de problema, um armazenamento de mensagens fortemente a par deve verificar o status da mensagem, além do local da mensagem. Especificamente, o provedor de transporte não deve solicitar que o spooler MAPI baixe qualquer mensagem que seja enviada ativamente.
  
O processo de transmissão de mensagens envolve o provedor de armazenamento de mensagens, um ou mais provedores de transporte e MAPI. Os tópicos desta seção fornecem informações detalhadas sobre funções específicas no processo de transmissão de mensagens.
  
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

