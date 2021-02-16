---
title: Fornecendo relatórios lidos e não lidos para provedores de armazenamento de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432335"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Fornecendo relatórios lidos e não lidos para provedores de armazenamento de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se um provedor de armazenamento de mensagens puder receber mensagens, será necessário dar suporte a relatórios de leitura e relatórios não lidos de mensagens recebidas pelo provedor do armazenamento de mensagens. Se uma mensagem recebida contiver a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) e o valor dessa propriedade for VERDADEIRO, o armazenamento de mensagens deverá enviar uma mensagem de notificação ao remetente quando o usuário abrir a mensagem, indicando que a mensagem foi lida. Da mesma forma, se o usuário excluir a mensagem antes de abri-la, o armazenamento de mensagens deverá emitir uma resposta para o remetente indicando que a mensagem não foi lida.
  
A emissão desses relatórios é uma questão de criar um [objeto IMessage : IMAPIProp,](imessageimapiprop.md) preencher as propriedades relevantes na mensagem e enviar para o spooler MAPI como se a mensagem tivesse se originado com o usuário. O [método IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) pode ser usado para isso. 
  
> [!NOTE]
> É necessário ter cuidado especial quando um armazenamento de mensagens faz cópias de uma mensagem não lida com relatórios de leitura ou não lidos pendentes. Esses relatórios não devem ser gerados quando os usuários leem quaisquer cópias de uma mensagem para a qual os relatórios foram solicitados. Ao fazer uma cópia dessa mensagem, o provedor de armazenamento de mensagens deve incluir os sinalizadores CLEAR_RN_PENDING e CLEAR_NRN_PENDING em suas chamadas para [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) e [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Confira também



[Recursos do Armazenamento de Mensagens](message-store-features.md)

