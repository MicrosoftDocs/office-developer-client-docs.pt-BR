---
title: Enviando mensagens tarefas do provedor de transporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bd722f48-b166-4670-8dba-897ac50caf37
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 2c1f73ab263e5851c78b33b6157d6d44c9e5e404
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586225"
---
# <a name="sending-messages-transport-provider-tasks"></a>Enviar mensagens: tarefas do provedor de transporte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para transmitir uma mensagem, provedores de transporte**
  
- Defina a propriedade de **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) da mensagem como TRUE depois que o provedor de transporte tem o enviou a mensagem ou tentou enviar a mensagem. Se uma tentativa de enviar uma mensagem falhar, provedores de transporte devem chamar [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) para gerar um relatório de não entrega. Se a mensagem é enviada com êxito e a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) for definida como TRUE, crie uma estrutura [ADRLIST](adrlist.md) contendo os destinatários bem-sucedida, a configuração da propriedade de **PR_DELIVER_TIME** ([PidTagDeliverTime](pidtagdelivertime-canonical-property.md)) para cada e chamadas **StatusRecips** para gerar um relatório de entrega. Para obter mais informações sobre a criação de relatórios de entrega e de entrega, consulte os seguintes tópicos: [Mensagens de relatório de MAPI](mapi-report-messages.md), [Necessárias propriedades da mensagem de relatório](required-report-message-properties.md), [Optional relatar propriedades da mensagem](optional-report-message-properties.md)e [Sending entrega de mensagens Relatórios](sending-message-delivery-reports.md).
    
- Defina o grupo **PR_SENDER** da mensagem das propriedades para a identidade do usuário que fez logon. Esse grupo inclui: **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)), **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)), **PR_SENDER_SEARCH_KEY** ([PidTagSenderSearchKey](pidtagsendersearchkey-canonical-property.md)), **PR_SENDER_ADDRTYPE** ([ PidTagSenderAddressType](pidtagsenderaddresstype-canonical-property.md)) e **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).
    
- Defina as propriedades da mensagem **PR_SENT_REPRESENTING** , se possível, para qualquer um da identidade do usuário que fez logon ou para uma identidade válida de representante. As propriedades **PR_SENT_REPRESENTING** são usadas para implementar o envio de mensagens por um usuário em nome de outro usuário. Provedores de transporte que não oferecem suporte a essas propriedades devem ignorá-las em mensagens de saída. 
    
- Defina a propriedade de **PR_CLIENT_SUBMIT_TIME** ([PidTagClientSubmitTime](pidtagclientsubmittime-canonical-property.md)) da mensagem para indicar quando o cliente chamado [IMessage::SubmitMessage](imessage-submitmessage.md).
    
- Defina a propriedade de **PR_PROVIDER_SUBMIT_TIME** ([PidTagProviderSubmitTime](pidtagprovidersubmittime-canonical-property.md)) da mensagem para indicar a data e hora em que o provedor de armazenamento de mensagem tiver marcado a mensagem como tendo sido enviado. 
    
Quando uma mensagem é enviada a uma variedade de destinatários com vários sistemas de mensagens, cada cópia transmitida terá uma identidade do remetente diferentes. 
  
O provedor de transporte ou o armazenamento de mensagens de ligação estreita e o transporte também é responsável por informações de originador e responder para configuração. As informações do originador são armazenadas nas propriedades do **PR_ORIGINATOR** e responder para informações são armazenadas nas propriedades do PR_REPLY. O cliente pode definir essas propriedades; No entanto, o provedor de transporte é permitido para ignorar e substituir as configurações do cliente. 
  

