---
title: Tabelas de destinatários
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
# <a name="recipient-tables"></a>Tabelas de destinatários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela de destinatários contém informações sobre todos os destinatários de uma mensagem. Os provedores de repositórios de mensagens implementam tabelas de destinatários e aplicativos cliente os usam. Os clientes acessam uma tabela de destinatários fazendo uma chamada para o método [IMessage::](imessage-getrecipienttable.md) GetRecipientTable ou, se o provedor de repositório de mensagens oferecer suporte, para o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) . Os clientes acessam **** tabelas de destinatários com OpenProperty especificando **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para a marca de propriedade e IID_IMAPITable para o identificador de interface. As alterações em uma tabela de destinatários podem ser feitas chamando o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) . 
  
As tabelas de destinatários têm um conjunto de colunas diferente, dependendo se a mensagem foi enviada. As propriedades a seguir compõem o conjunto de colunas necessárias nas tabelas de destinatários:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
As propriedades opcionais são:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
As mensagens enviadas devem incluir essas propriedades adicionais no conjunto de colunas exigido:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Dependendo da implementação de um provedor, colunas adicionais, como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) e EntryID [](entryid.md), podem estar na tabela.
  
Qualquer provedor de repositório de mensagens que ofereça suporte à transmissão de mensagens, conforme indicado pelo bit de STORE_SUBMIT_OK que está sendo definido na propriedade **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do provedor, deve oferecer suporte a um determinado conjunto de restrições em uma implementação de tabela de destinatários. As restrições de **e**, **ou**, existem e propriedades estão entre os tipos de restrições que devem estar disponíveis para os usuários da tabela de destinatários. Apenas operadores iguais e não iguais precisam ter suporte na restrição de propriedade. Essas restrições devem funcionar com as seguintes propriedades:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

