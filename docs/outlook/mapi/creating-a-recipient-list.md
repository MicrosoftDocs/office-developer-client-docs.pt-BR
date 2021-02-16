---
title: Criando uma lista de destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428211"
---
# <a name="creating-a-recipient-list"></a>Criando uma lista de destinatários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma lista de destinatários é [uma estrutura ADRLIST](adrlist.md) que contém uma matriz de estruturas de valores de propriedade para cada destinatário da mensagem — destino da mensagem. Um destinatário pode representar um usuário humano, um computador ou uma pasta. Todas as mensagens a serem enviadas exigem pelo menos um destinatário que passou pelo processo de resolução de nomes — um processo para garantir que a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) seja incluída na matriz de valores de propriedade do destinatário. 
  
As propriedades de um destinatário são uma combinação de propriedades do livro de endereços e propriedades da mensagem. As propriedades de destinatário podem ser aplicadas a todas as mensagens de um destinatário específico ou somente à mensagem atual. Tanto o armazenamento de mensagens quanto os provedores de transporte podem definir as propriedades do destinatário. 
  
Cada destinatário deve ter um conjunto principal de propriedades em sua matriz de valores de propriedade quando a mensagem estiver pronta para ser enviada. O conjunto obrigatório de propriedades de destinatários inclui:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Essas propriedades são usadas para acessar o destinatário, enviar mensagens a ele e compará-lo com outras pessoas. Nem todas essas propriedades precisam estar disponíveis imediatamente. Você pode adicionar um destinatário inicialmente sem conhecer seu identificador de entrada, confiando no processo de resolução de nomes para atribuir essa propriedade. Em algum momento antes de enviar uma mensagem, chame [IAddrBook::ResolveName](iaddrbook-resolvename.md) para garantir que todos os destinatários em sua lista de destinatários sejam resolvidos. Para obter mais informações, consulte [Resolvendo um nome de destinatário.](resolving-a-recipient-name.md)
  
Listas de destinatários podem ser criadas a partir de usuários de mensagens ou entradas de listas de distribuição em um contêiner de um livro de endereços ou de um único usuário. One-offs são destinatários criados como entradas temporárias a serem usadas apenas para endereçamento de uma única mensagem ou como entradas a serem adicionadas a um livro de endereços pessoal. O formato para um identificador de entrada único e endereço é definido por MAPI. Para obter mais informações sobre esses formatos, consulte [One-Off Addresses](one-off-addresses.md) and [One-Off Entry Identifiers](one-off-entry-identifiers.md).
  
Você pode permitir que os usuários criem suas listas de destinatários:
  
- Somente com entradas do livro de endereços.
    
- Somente com entradas únicas.
    
- Com uma combinação de destinatários do livro de endereços e one-offs.
    
 **Para criar uma lista de destinatários usando a caixa de diálogo de endereço comum**
  
1. Aloce uma [estrutura ADRPARM](adrparm.md) e um ponteiro para uma [estrutura ADRLIST.](adrlist.md) 
    
2. Anula a memória na estrutura **ADRPARM** e defina o ponteiro **ADRLIST** como NULL. 
    
3. Chame [IAddrBook::Address](iaddrbook-address.md) para exibir a caixa de diálogo de endereço e preencher a estrutura **ADRPARM.** 
    
4. Chame [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passando o ponteiro **ADRLIST.** Essa estrutura conterá as propriedades de cada um dos destinatários selecionados pelo usuário. 
    
 **Para criar uma lista de destinatários programaticamente**
  
1. Aloce **uma estrutura ADRLIST** que contenha uma estrutura [ADRENTRY](adrentry.md) para cada um dos destinatários a serem incluídos na lista. Tornar cada **estrutura ADRENTRY** grande o suficiente para manter cada uma das propriedades necessárias **e PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).
    
2. Para cada destinatário, defina a matriz de valores de propriedade para seu **membro aEntries** na **estrutura ADRLIST.** 
    
3. Chame [IMessage::ModifyRecipients com](imessage-modifyrecipients.md) o sinalizador MODRECIP_ADD definido. 
    

