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
ms.openlocfilehash: 6a3172dcd962c04d72aacd14d2e42990fb0f78c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593449"
---
# <a name="sending-messages-by-using-mapi"></a>Enviar mensagens usando MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aplicativos cliente chamam o método [IMessage::SubmitMessage](imessage-submitmessage.md) para enviar uma mensagem. **SubmitMessage** chama [IMAPIProp::SaveChanges](imapiprop-savechanges.md) para salvar a mensagem antes de transferir o controle para o spooler MAPI ou diretamente a um provedor de transporte. 
  
O MAPI spooler recebe a mensagem se qualquer um destes procedimentos ocorrer:
  
- O provedor de armazenamento de mensagem e o provedor de transporte não estão intimamente ligadas.
    
- A mensagem requer pré-processamento.
    
- O repositório de ligação estreita de mensagem e transporte não podem lidar com todos os destinatários para quem a mensagem é endereçada.
    
Um armazenamento de mensagens de ligação estreita deve levar em conta o status de uma mensagem antes que ele apresenta-as para o MAPI spooler sejam baixados para um provedor de transporte. Existem situações em que uma mensagem é exibida exigir que o spooler MAPI, mas o MAPI spooler realmente não deveriam estar envolvido.
  
Por exemplo, considere a situação em que um usuário envia uma mensagem da caixa de entrada. O cliente está usando um repositório de ligação estreita e o transporte. Se o armazenamento de mensagens de ligação estreita usa do local da mensagem como o único critério para decidir sobre se devem ou não permitir que o spooler MAPI lidar com a mensagem, o MAPI spooler sempre receberá a mensagem. Para evitar esse tipo de problema, um armazenamento de mensagens de ligação estreita deve verificar o status de mensagem além do local da mensagem. Especificamente, o provedor de transporte não deve solicitar que o MAPI spooler baixar qualquer mensagem que será enviada ativamente.
  
O processo de transmissão de mensagem envolve o provedor de armazenamento de mensagem, um ou mais provedores de transporte e MAPI. Os tópicos desta seção fornecem informações detalhadas sobre funções específicas no processo de transmissão de mensagem.
  
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

