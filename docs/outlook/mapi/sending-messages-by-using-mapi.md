---
title: Envio de mensagens usando MAPI
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
# <a name="sending-messages-by-using-mapi"></a>Envio de mensagens usando MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os aplicativos cliente chamam o método [IMessage:: SubmitMessage](imessage-submitmessage.md) para enviar uma mensagem. **SubmitMessage** chama [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) para salvar a mensagem antes de transferir o controle para o spooler MAPI ou diretamente para um provedor de transporte. 
  
O spooler MAPI receberá a mensagem se ocorrer qualquer uma das seguintes ações:
  
- O provedor de repositório de mensagens e o provedor de transporte não estão rigidamente acoplados.
    
- A mensagem requer pré-processamento.
    
- O armazenamento de mensagens rigidamente acoplado e o transporte não podem lidar com todos os destinatários para os quais a mensagem é endereçada.
    
Um repositório de mensagens rigidamente acoplado deve levar em conta o status de uma mensagem antes de apresentá-la ao spooler MAPI a ser baixado para um provedor de transporte. Há situações em que uma mensagem pode parecer exigir o spooler MAPI, mas o spooler MAPI deve realmente não estar envolvido.
  
Por exemplo, considere a situação em que um usuário envia uma mensagem da caixa de entrada. O cliente está usando um armazenamento e transporte rigidamente acoplado. Se o repositório de mensagens rigidamente acoplado usar o local da mensagem como o único critério para decidir se permitirá ou não o spooler MAPI para lidar com a mensagem, o spooler MAPI sempre receberá a mensagem. Para evitar esse tipo de problema, um repositório de mensagens rigidamente acoplado deve verificar o status da mensagem além do local da mensagem. Especificamente, o provedor de transporte não deve solicitar que o spooler MAPI Baixe qualquer mensagem que esteja ativamente enviada.
  
O processo de transmissão de mensagens envolve o provedor de armazenamento de mensagens, um ou mais provedores de transporte e MAPI. Os tópicos desta seção fornecem informações detalhadas sobre funções específicas no processo de transmissão de mensagens.
  
## <a name="see-also"></a>Confira também



[IMessage::SubmitMessage](imessage-submitmessage.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)

