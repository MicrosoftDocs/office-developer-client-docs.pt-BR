---
title: Enviar uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6845c3d86fb3d34119a296ebbae76a7322d7d8c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590908"
---
# <a name="sending-a-message"></a>Enviar uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando você estiver pronto para enviar uma mensagem, chame seu método de [IMessage::SubmitMessage](imessage-submitmessage.md) . **SubmitMessage** coloca a mensagem na fila de saída e define o sinalizador MSGFLAG_SUBMIT na propriedade de **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.
  
O provedor de armazenamento de mensagem, se fortemente acoplada a um provedor de transporte, dará a mensagem diretamente para o transporte que entrega para o sistema de mensagens. Se não estreitamente acoplado, o provedor de armazenamento de mensagem informa o spooler MAPI que a fila de saída foi alterada e o MAPI spooler transfere a mensagem para um provedor de transporte adequado.
  
Se você permitir aos usuários cancelar uma operação de envio, chame [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para implementar esse recurso. **AbortSubmit** remove a mensagem da fila de saída. Os usuários podem ter permissão para interromper um envio aconteça até que a mensagem é fornecida para o sistema de mensagens subjacente. 
  
Se **SubmitMessage** retornar MAPI_E_CORRUPT_DATA, suponha que os dados que estão sendo enviados são agora perdido. Antes de tentar enviar uma segunda vez, gravar novamente a mensagem chamando [IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Exiba um erro ao usuário se essas chamadas **IMAPIProp** falharem ou se **SubmitMessage** falhar uma segunda vez. 
  
Depois de uma chamada bem sucedida a **SubmitMessage**, liberar qualquer memória que foi alocada para a lista de destinatários e liberar a mensagem e seus respectivos anexos. Depois que uma mensagem foi enviada, MAPI não permite que quaisquer operações mais sobre os ponteiros para esses objetos. A única exceção é chamando **IUnknown:: Release**. Nenhuma outra chamada é permitida porque muitos provedores de armazenamento de mensagem invalidar identificadores de entrada para mensagens que foram enviados.
  

