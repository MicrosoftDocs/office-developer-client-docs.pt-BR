---
title: Tabelas de Destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e77317-54c4-4fca-9ab4-835998ce07ce
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8950623308e85de1d239deb322f65ee867a33ca0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437284"
---
# <a name="recipient-tables"></a>Tabelas de Destinatários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela de destinatários contém informações sobre todos os destinatários de uma mensagem. Os provedores de armazenamento de mensagens implementam tabelas de destinatários e os aplicativos cliente as usam. Os clientes acessam uma tabela de destinatários fazendo uma chamada para o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) ou, se o provedor de armazenamento de mensagens a suportar, para o método [IMAPIProp::OpenProperty.](imapiprop-openproperty.md) Os clientes acessam tabelas de destinatários com **OpenProperty** especificando PR_MESSAGE_RECIPIENTS ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para **a** marca de propriedade e IID_IMAPITable para o identificador da interface. As alterações em uma tabela de destinatários podem ser feitas chamando-se o [método IMessage::ModifyRecipients.](imessage-modifyrecipients.md) 
  
As tabelas de destinatários têm um conjunto de colunas diferente, dependendo se a mensagem foi enviada. As propriedades a seguir compom o conjunto de colunas necessário nas tabelas de destinatários:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
As propriedades opcionais são:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
As mensagens enviadas devem incluir essas propriedades adicionais no conjunto de colunas necessário:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Dependendo da implementação de um provedor, colunas adicionais, como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) e [ENTRYID](entryid.md), podem estar na tabela.
  
Qualquer provedor de repositório de mensagens que ofereça suporte à transmissão de mensagens — conforme indicado pelo bit STORE_SUBMIT_OK sendo definido na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do provedor — deve oferecer suporte para um conjunto específico de restrições em uma implementação de tabela de destinatários. The **AND**, **OR**, exist, and property restrictions are among the types of restrictions that should be available to recipient table users. Somente os operadores iguais e não iguais precisam ter suporte na restrição de propriedade. Essas restrições devem funcionar com as seguintes propriedades:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

