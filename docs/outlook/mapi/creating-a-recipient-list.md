---
title: Criar lista de destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6de805da2aadd8ac40ca984c5f336d5ca7906248
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590124"
---
# <a name="creating-a-recipient-list"></a>Criar lista de destinatários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma lista de destinatários é uma estrutura [ADRLIST](adrlist.md) que contém uma matriz de estruturas de valor de propriedade de cada destinatário da mensagem — destino da mensagem. Um destinatário pode representar um usuário humano, uma máquina ou uma pasta. Todas as mensagens sejam enviadas exigem pelo menos um destinatário que tiver ficado durante o processo de resolução de nome — um processo para garantir que a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) é incluída na matriz de valores de propriedade do destinatário. 
  
As propriedades de um destinatário são uma combinação de propriedades do catálogo de endereços e propriedades da mensagem. Propriedades de destinatário podem aplicar a todas as mensagens para um destinatário específico ou apenas à mensagem atual. Ambos repositório de mensagens e provedores de transporte podem definir propriedades de destinatário. 
  
Cada destinatário deve ter um conjunto básico de propriedades em sua matriz de valores de propriedade no momento em que a mensagem está pronta para ser enviada. O conjunto necessário de propriedades de destinatário incluem:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Essas propriedades são usadas para acessar o destinatário, enviar mensagens a ela e compará-lo com outras pessoas. Nem todas essas propriedades precisam estar disponíveis imediatamente. Você pode adicionar um destinatário inicialmente sem saber seu identificador de entrada, contar com o processo de resolução de nomes para atribuir essa propriedade. Em algum momento antes de enviar uma mensagem, chame [IAddrBook::ResolveName](iaddrbook-resolvename.md) para certificar-se de que todos os destinatários na sua lista de destinatários forem resolvidos. Para obter mais informações, consulte a [resolução de um nome de destinatário](resolving-a-recipient-name.md).
  
Destinatários listas podem ser criadas a partir de mensagens a usuários ou entradas da lista de distribuição em um contêiner de catálogo de endereços ou algo isolado. Algo isolado é destinatários que são criados como entradas temporárias a ser usado apenas para uma única mensagem:/ / Tools.ietf.org ou como entradas a ser adicionado a um catálogo de endereços pessoal. O formato de um identificador de entrada únicos e endereço é definido por MAPI. Para obter mais informações sobre esses formatos, consulte [Endereços únicos](one-off-addresses.md) e [Únicos identificadores de entrada](one-off-entry-identifiers.md).
  
Você pode permitir que os usuários criem suas listas de destinatário:
  
- Somente com entradas do catálogo de endereços.
    
- Somente com entradas únicas.
    
- Com uma combinação de destinatários do catálogo de endereços e algo isolado.
    
 **Para criar uma lista de destinatários usando a caixa de diálogo endereço comuns**
  
1. Aloca uma estrutura [ADRPARM](adrparm.md) e um ponteiro para uma estrutura [ADRLIST](adrlist.md) . 
    
2. Zero a memória na estrutura de **ADRPARM** e defina o ponteiro **ADRLIST** como NULL. 
    
3. Chame [IAddrBook::Address](iaddrbook-address.md) para exibir a caixa de diálogo de endereço e popular a estrutura **ADRPARM** . 
    
4. Chame [IMessage::ModifyRecipients](imessage-modifyrecipients.md), passando o ponteiro **ADRLIST** . Essa estrutura irá conter as propriedades de cada um dos destinatários selecionados pelo usuário. 
    
 **Para criar uma lista de destinatários programaticamente**
  
1. Aloca uma estrutura **ADRLIST** que contém uma estrutura [ADRENTRY](adrentry.md) para cada um dos destinatários a serem incluídos na lista. Verifique cada estrutura **ADRENTRY** grande o suficiente para armazenar cada uma das propriedades exigidas e **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).
    
2. Para cada destinatário, defina a matriz de valores de propriedade para seu membro **aEntries** na estrutura **ADRLIST** . 
    
3. Chame [IMessage::ModifyRecipients](imessage-modifyrecipients.md) com o sinalizador MODRECIP_ADD definido. 
    

