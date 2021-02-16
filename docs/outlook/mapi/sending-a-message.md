---
title: Enviar uma mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4fa47824-b4ef-41e1-9096-c1b1cdacd7ac
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 01fd66033da0f24948913f47a752d555eca655fe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423619"
---
# <a name="sending-a-message"></a>Enviar uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando você estiver pronto para enviar uma mensagem, chame seu [método IMessage::SubmitMessage.](imessage-submitmessage.md) **SubmitMessage** coloca a mensagem na fila de saída e define o sinalizador MSGFLAG_SUBMIT na propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) da mensagem.
  
O provedor de armazenamento de mensagens, se estiver fortemente ligado a um provedor de transporte, fornece a mensagem diretamente para o transporte que a entrega ao sistema de mensagens. Se não estiver fortemente afiliado, o provedor de armazenamento de mensagens informa ao spooler MAPI que a fila de saída foi alterada e o spooler MAPI transfere a mensagem para um provedor de transporte apropriado.
  
Se você permitir que os usuários cancelem uma operação de envio, chame [IMsgStore::AbortSubmit](imsgstore-abortsubmit.md) para implementar esse recurso. **AbortSubmit** remove a mensagem da fila de saída. Os usuários podem impedir que um envio aconteça até que a mensagem seja entregue ao sistema de mensagens subjacente. 
  
Se **SubmitMessage** retornar MAPI_E_CORRUPT_DATA, suponha que os dados que estão sendo enviados agora foram perdidos. Antes de tentar enviar uma segunda vez, re-escreva a mensagem chamando [IMAPIProp::SetProps](imapiprop-setprops.md) e [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Exibir um erro para o usuário se essas chamadas **IMAPIProp** falharem ou **se SubmitMessage** falhar uma segunda vez. 
  
Após uma chamada bem-sucedida para **SubmitMessage**, libere qualquer memória alocada para a lista de destinatários e libere a mensagem e seus anexos. Depois que uma mensagem for enviada, o MAPI não permitirá mais operações nos ponteiros desses objetos. A única exceção é chamar **IUnknown::Release**. Nenhuma outra chamada é permitida porque muitos provedores de armazenamento de mensagens invalidam identificadores de entrada para mensagens que foram enviadas.
  

