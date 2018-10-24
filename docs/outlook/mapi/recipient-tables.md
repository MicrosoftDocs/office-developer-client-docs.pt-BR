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
ms.openlocfilehash: fdca2f65c73c0db0fa0b7d59b8d49b218aeb2330
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565085"
---
# <a name="recipient-tables"></a>Tabelas de destinatários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Tabela de destinatário contém informações sobre todos os destinatários de uma mensagem. Tabelas de destinatários de implementar provedores de armazenamento de mensagens e aplicativos cliente usá-los. Clientes acessar uma tabela de destinatário fazendo uma chamada ao método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) ou se o provedor de armazenamento de mensagem lhe fornecer apoio, para o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) . Os clientes acessar tabelas de destinatários com **OpenProperty** especificando **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) para a marca de propriedade e IID_IMAPITable para o identificador de interface. Podem ser feitas alterações em uma tabela de destinatário, chamando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) . 
  
Tabelas de destinatários têm outra coluna definir dependendo se a mensagem foi enviada. As seguintes propriedades compõem a coluna necessária definida nas tabelas de destinatário:
  
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md))
    
- **PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))
    
As propriedades opcionais são:
  
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
- **PR_SPOOLER_STATUS** ([PidTagSpoolerStatus](pidtagspoolerstatus-canonical-property.md))
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
Mensagens enviadas devem incluir essas propriedades adicionais em seu conjunto de coluna necessária:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))
    
- **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))
    
Dependendo da implementação de um provedor, colunas adicionais, como **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) e [ENTRYID](entryid.md), podem ser na tabela.
  
Provedor de armazenamento de qualquer mensagem que ofereça suporte a transmissão de mensagens — conforme indicado pelo sendo definido na propriedade de **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) do provedor definido o bit STORE_SUBMIT_OK — deve oferecer suporte a um determinado conjunto de restrições na implementação de um destinatário de tabela. **E**, **ou**, existir e restrições de propriedade estão entre os tipos de restrições que deveriam estar disponíveis para os usuários da tabela de destinatário. Somente os operadores iguais e não iguais precisam oferecer suporte a restrição de propriedade. Essas restrições devem trabalhar com as seguintes propriedades:
  
- **PR_ADDRTYPE**
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_RECIPIENT_TYPE**
    
- **PR_RESPONSIBILITY**
    
- **PR_SPOOLER_STATUS**
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

