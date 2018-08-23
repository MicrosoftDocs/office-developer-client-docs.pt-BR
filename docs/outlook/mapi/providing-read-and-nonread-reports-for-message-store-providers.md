---
title: Fornecer relatórios de leitura e não leitura para provedores do repositório de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8e2552cbeaf528de634c39a5ebd175a2615782b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594436"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Fornecer relatórios de leitura e não leitura para provedores do repositório de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se um provedor de armazenamento de mensagem pode receber mensagens, ela é necessária para oferecer suporte a relatórios de leitura e nonread relatórios de mensagens recebidas pelo provedor de armazenamento de mensagem. Se uma mensagem recebida contém a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) e o valor da propriedade é TRUE, o armazenamento de mensagens deve enviar uma mensagem de notificação para o remetente quando o usuário abre a mensagem, indicando que a mensagem foi lido. Da mesma forma, se o usuário excluir a mensagem antes de abri-lo, o armazenamento de mensagens deve emitir uma resposta ao remetente, indicando que a mensagem não foi lido.
  
Emitir esses relatórios é uma questão de criação de um [IMessage: IMAPIProp](imessageimapiprop.md) objeto, preenchendo as propriedades relevantes na mensagem e enviá-lo para o spooler MAPI como se a mensagem tinha originada com o usuário. O método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) pode ser usado para que isso. 
  
> [!NOTE]
> Especial deve ter cuidado quando um armazenamento de mensagens faz cópias de uma mensagem não lida com pendentes lidas ou nonread relatórios. Esses relatórios não deverão ser gerados quando os usuários ler alguma cópia de uma mensagem para o qual os relatórios tiverem sido solicitados. Quando você faz uma cópia de uma mensagem, o provedor de armazenamento de mensagem deve incluir os sinalizadores CLEAR_RN_PENDING e CLEAR_NRN_PENDING em suas chamadas para [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) e [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

