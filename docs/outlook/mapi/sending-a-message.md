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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339743"
---
# <a name="sending-a-message"></a>Enviar uma mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando estiver pronto para enviar uma mensagem, chame o método [IMessage:: SubmitMessage](imessage-submitmessage.md) . **SubmitMessage** coloca a mensagem na fila de saída e define o sinalizador MSGFLAG_SUBMIT na propriedade **PR_MESSAGE_FLAGS** da mensagem ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)).
  
O provedor de repositório de mensagens, se rigidamente acoplado a um provedor de transporte, fornece a mensagem diretamente ao transporte que a entrega ao sistema de mensagens. Se não estiver rigidamente acoplado, o provedor de armazenamento de mensagens informa ao spooler MAPI que a fila de saída foi alterada e o spooler MAPI transfere a mensagem para um provedor de transporte apropriado.
  
Se você permitir que os usuários cancelem uma operação de envio, chame [IMsgStore:: AbortSubmit](imsgstore-abortsubmit.md) para implementar esse recurso. **AbortSubmit** remove a mensagem da fila de saída. Os usuários podem ter permissão para interromper um envio de acontecer até que a mensagem seja dada ao sistema de mensagens subjacente. 
  
Se **SubmitMessage** retornar MAPI_E_CORRUPT_DATA, presuma que os dados que estão sendo enviados serão perdidos. Antes de tentar enviar uma segunda vez, reescreva a mensagem chamando [IMAPIProp::](imapiprop-setprops.md) SetProps e [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). Exibe um erro para o usuário se essas **IMAPIProp** chamadas falharem ou se o **SubmitMessage** falhar uma segunda vez. 
  
Após uma chamada bem-sucedida para o **SubmitMessage**, libere qualquer memória que tenha sido alocada para a lista de destinatários e libere a mensagem e seus anexos. Depois que uma mensagem for enviada, o MAPI não permitirá nenhuma operação adicional nos ponteiros desses objetos. A única exceção é chamar **IUnknown:: Release**. Nenhuma outra chamada é permitida porque muitos provedores de repositórios de mensagens invalidam identificadores de entrada para mensagens enviadas.
  

