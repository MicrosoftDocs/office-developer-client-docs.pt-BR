---
title: Enviando tarefas do provedor de transporte de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 431e3d2f66616db2c586b76387a8521832ed985f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426545"
---
# <a name="sending-messages-transport-provider-tasks"></a>Enviar mensagens: tarefas do provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para transmitir uma mensagem, provedores de transporte**
  
- Defina a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) da mensagem como true Depois que o provedor de transporte tenha enviado a mensagem ou tentado enviar a mensagem. Se uma tentativa de enviar uma mensagem falhar, os provedores de transporte devem chamar [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) para gerar um relatório de não entrega. Se a mensagem for enviada com êxito e a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) estiver definida como true, crie uma estrutura [das ADRLIST](adrlist.md) que contenha os destinatários com êxito, definir a propriedade **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) para cada, e chamar **StatusRecips** para gerar um relatório de entrega. Para obter mais informações sobre como criar notificações de entrega e de falha na entrega, consulte os seguintes tópicos: [mensagens de relatório MAPI](mapi-report-messages.md), [Propriedades de mensagens](required-report-message-properties.md)de relatórios requeridas, propriedades de [mensagens de relatórios opcionais](optional-report-message-properties.md)e envio de [mensagens Relatórios](sending-message-delivery-reports.md).
    
- Definir o grupo de propriedades **PR_SENDER** da mensagem para a identidade do usuário que fez logon. Este grupo inclui: **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([ PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) e **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- Defina as propriedades de **PR_SENT_REPRESENTING** da mensagem, se possível, para a identidade do usuário que fez logon ou para uma identidade de representante válida. As propriedades **PR_SENT_REPRESENTING** são usadas para implementar o envio de mensagens por um usuário em nome de outro usuário. Provedores de transporte que não dão suporte a essas propriedades devem ser ignorados em mensagens de saída. 
    
- Defina a propriedade **PR_CLIENT_SUBMIT_TIME** da mensagem ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) para indicar quando o cliente chamou [IMessage:: SubmitMessage](imessage-submitmessage.md).
    
- Defina a propriedade **PR_PROVIDER_SUBMIT_TIME** da mensagem ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) para indicar a data e a hora em que o provedor do repositório de mensagens marcou a mensagem como tendo sido enviada. 
    
Quando uma mensagem é enviada para vários destinatários com vários sistemas de mensagens, cada cópia transmitida terá uma identidade de remetente diferente. 
  
O provedor de transporte ou o armazenamento e transporte de mensagens rigidamente acoplados também são responsáveis por definir as informações de originador e de resposta. As informações de originador são armazenadas nas propriedades do **PR_ORIGINATOR** e as informações de resposta são armazenadas nas propriedades PR_REPLY. O cliente pode definir essas propriedades; no entanto, o provedor de transporte tem permissão para ignorar e substituir as configurações do cliente. 
  

