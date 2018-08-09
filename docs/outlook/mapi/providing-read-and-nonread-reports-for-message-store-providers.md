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
ms.openlocfilehash: b082d063cc77be46fcd3d4e07ec6753f78f8f335
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770230"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Fornecer relatórios de leitura e não leitura para provedores do repositório de mensagens

  
  
**Aplica-se a**: Outlook 
  
Se um provedor de armazenamento de mensagem pode receber mensagens, ela é necessária para oferecer suporte a relatórios de leitura e nonread relatórios de mensagens recebidas pelo provedor de armazenamento de mensagem. Se uma mensagem recebida contém a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) e o valor da propriedade é TRUE, o armazenamento de mensagens deve enviar uma mensagem de notificação para o remetente quando o usuário abre a mensagem, indicando que a mensagem foi lido. Da mesma forma, se o usuário excluir a mensagem antes de abri-lo, o armazenamento de mensagens deve emitir uma resposta ao remetente, indicando que a mensagem não foi lido.
  
Emitir esses relatórios é uma questão de criação de um [IMessage: IMAPIProp](imessageimapiprop.md) objeto, preenchendo as propriedades relevantes na mensagem e enviá-lo para o spooler MAPI como se a mensagem tinha originada com o usuário. O método [IMAPISupport::ReadReceipt](imapisupport-readreceipt.md) pode ser usado para que isso. 
  
> [!NOTE]
> Especial deve ter cuidado quando um armazenamento de mensagens faz cópias de uma mensagem não lida com pendentes lidas ou nonread relatórios. Esses relatórios não deverão ser gerados quando os usuários ler alguma cópia de uma mensagem para o qual os relatórios tiverem sido solicitados. Quando você faz uma cópia de uma mensagem, o provedor de armazenamento de mensagem deve incluir os sinalizadores CLEAR_RN_PENDING e CLEAR_NRN_PENDING em suas chamadas para [IMAPIFolder::SetReadFlags](imapifolder-setreadflags.md) e [IMessage::SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

