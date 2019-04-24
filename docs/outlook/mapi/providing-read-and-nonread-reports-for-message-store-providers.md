---
title: Fornecer relatórios de leitura e não leitura para provedores de repositórios de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9644b8c5-ecc0-4ea3-972a-2169c78b99e5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 96546d3d766af398ff7acb50f4fc3a479b5668b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328508"
---
# <a name="providing-read-and-nonread-reports-for-message-store-providers"></a>Fornecer relatórios de leitura e não leitura para provedores de repositórios de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Se um provedor de repositório de mensagens puder receber mensagens, será necessário suportar relatórios de leitura e relatórios não lidos de mensagens recebidas pelo provedor de armazenamento de mensagens. Se uma mensagem recebida contiver a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) e se o valor dessa propriedade for true, o repositório de mensagens deverá enviar uma mensagem de notificação ao remetente quando o usuário abrir a mensagem, indicando que a mensagem foi lida. Da mesma forma, se o usuário excluir a mensagem antes de abri-la, o repositório de mensagens deverá emitir uma resposta para o remetente, indicando que a mensagem não foi lida.
  
A emissão desses relatórios é uma questão de criação de um objeto [IMessage: IMAPIProp](imessageimapiprop.md) , o preenchimento das propriedades relevantes na mensagem e o envio ao spooler MAPI como se a mensagem tivesse sido originada com o usuário. O método [IMAPISupport:: ReadReceipt](imapisupport-readreceipt.md) pode ser usado para isso. 
  
> [!NOTE]
> Cuidado especial deve ser feito quando um repositório de mensagens faz cópias de uma mensagem não lida com os relatórios de leitura ou não leitura pendentes. Esses relatórios não devem ser gerados quando os usuários lêem qualquer cópia de uma mensagem para a qual os relatórios foram solicitados. Ao fazer uma cópia dessa mensagem, o provedor do repositório de mensagens deve incluir os sinalizadores CLEAR_RN_PENDING e CLEAR_NRN_PENDING em suas chamadas para [IMAPIFolder:: SetReadFlags](imapifolder-setreadflags.md) e [IMessage:: SetReadFlag](imessage-setreadflag.md). 
  
## <a name="see-also"></a>Confira também



[Recursos do repositório de mensagens](message-store-features.md)

