---
title: Enviar tarefas do provedor de transporte de mensagens
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
# <a name="sending-messages-transport-provider-tasks"></a>Enviar Mensagens: Tarefas do Provedor de Transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para transmitir uma mensagem, os provedores de transporte**
  
- Definir a propriedade **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) da mensagem como VERDADEIRO depois que o provedor de transporte tiver enviado a mensagem ou tentado enviar a mensagem. Se uma tentativa de enviar uma mensagem falhar, os provedores de transporte deverão chamar [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para gerar um relatório de não entrega. Se a mensagem for enviada com êxito e a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) estiver definida como TRUE, crie uma estrutura [ADRLIST](adrlist.md) contendo os destinatários bem-sucedidos, definindo a propriedade **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) para cada um e chame **StatusRecips** para gerar um relatório de entrega. Para obter mais informações sobre como criar relatórios de entrega e não entrega, consulte os seguintes tópicos: [MAPI Report Messages](mapi-report-messages.md), [Required Report Message Properties](required-report-message-properties.md), Optional Report Message [Properties](optional-report-message-properties.md), and Sending Message [Delivery Reports](sending-message-delivery-reports.md).
    
- De definir o grupo **PR_SENDER** de propriedades da mensagem como a identidade do usuário que fez logor. Esse grupo inclui: **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) e **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- De definir as  propriedades PR_SENT_REPRESENTING mensagem, se possível, para a identidade do usuário que fez logor ou para uma identidade de representante válida. As **PR_SENT_REPRESENTING** propriedades são usadas para implementar o envio de mensagens por um usuário em nome de outro usuário. Os provedores de transporte que não suportam essas propriedades devem ignorá-las em mensagens de saída. 
    
- Definir a propriedade **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) da mensagem para indicar quando o cliente chamou [IMessage::SubmitMessage](imessage-submitmessage.md).
    
- Definir a propriedade PR_PROVIDER_SUBMIT_TIME ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) da mensagem para indicar a data e a hora em que o provedor de armazenamento de mensagens marcou **a** mensagem como tendo sido enviada. 
    
Quando uma mensagem é enviada para vários destinatários com vários sistemas de mensagens, cada cópia transmitida terá uma identidade de remetente diferente. 
  
O provedor de transporte ou o armazenamento e o transporte de mensagens fortemente próximos também são responsáveis por configurar informações de origem e resposta. As informações de origem são armazenadas **nas PR_ORIGINATOR** propriedades e as informações de resposta são armazenadas nas PR_REPLY propriedades. O cliente pode definir essas propriedades; no entanto, o provedor de transporte tem permissão para ignorar e substituir as configurações do cliente. 
  

