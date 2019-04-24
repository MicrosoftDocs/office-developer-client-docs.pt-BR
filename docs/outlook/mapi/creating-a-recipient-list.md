---
title: Criar uma lista de destinatários
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 270f86dd-2c1f-47eb-80f7-9d0d63936d61
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e3aa1f2b2e1e7c6d8a9be3fff451002952930ffb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332904"
---
# <a name="creating-a-recipient-list"></a>Criar uma lista de destinatários

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma lista de destinatários é uma estrutura [das ADRLIST](adrlist.md) que contém uma matriz de estruturas de valor de propriedade para cada destinatário de mensagem — destino para a mensagem. Um destinatário pode representar um usuário humano, uma máquina ou uma pasta. Todas as mensagens a serem enviadas exigem pelo menos um destinatário com o processo de resolução de nome — um processo para garantir que a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) seja incluída na matriz de valor de Propriedade do destinatário. 
  
As propriedades de um destinatário são uma combinação de propriedades de catálogo de endereços e propriedades de mensagem. As propriedades de destinatário podem ser aplicadas a todas as mensagens de um determinado destinatário ou apenas à mensagem atual. O armazenamento de mensagens e os provedores de transporte podem definir as propriedades do destinatário. 
  
Cada destinatário deve ter um conjunto principal de propriedades em sua matriz de valor de propriedade, quando a mensagem estiver pronta para ser enviada. O conjunto necessário de propriedades de destinatários inclui:
  
- **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) 
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) 
    
- **PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md)) 
    
- **PR_ENTRYID**
    
- **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) 
    
- **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) 
    
Essas propriedades são usadas para acessar o destinatário, enviar mensagens a ele e compará-las a outras pessoas. Nem todas essas propriedades precisam estar disponíveis imediatamente. Você pode adicionar um destinatário inicialmente sem saber seu identificador de entrada, contando com o processo de resolução de nomes para atribuir essa propriedade. Em algum momento antes de enviar uma mensagem, chame [IAddrBook:: ResolveName](iaddrbook-resolvename.md) para garantir que todos os destinatários na lista de destinatários sejam resolvidos. Para obter mais informações, consulte [resolvendo o nome de um destinatário](resolving-a-recipient-name.md).
  
As listas de destinatários podem ser criadas a partir de usuários de mensagens ou entradas de lista de distribuição em um contêiner de catálogo de endereços ou em um. Uma delas são destinatários criados como entradas temporárias para serem usados apenas para endereçar uma única mensagem ou como entradas a serem adicionadas a um catálogo de endereços pessoal. O formato para um identificador de entrada one-off e um endereço é definido por MAPI. Para obter mais informações sobre esses formatos, confira [endereços únicos](one-off-addresses.md) e [identificadores de entrada one-off](one-off-entry-identifiers.md).
  
Você pode permitir que os usuários criem suas listas de destinatários:
  
- Somente com entradas do catálogo de endereços.
    
- Somente com entradas one-off.
    
- Com uma combinação de destinatários do catálogo de endereços e uma única.
    
 **Para criar uma lista de destinatários usando a caixa de diálogo endereço comum**
  
1. Alocar uma estrutura [ADRPARM](adrparm.md) e um ponteiro para uma estrutura [das ADRLIST](adrlist.md) . 
    
2. Zero a memória na estrutura **ADRPARM** e definir o ponteiro **das ADRLIST** como nulo. 
    
3. Chamar [IAddrBook:: endereço](iaddrbook-address.md) para exibir a caixa de diálogo de endereço e preencher a estrutura **ADRPARM** . 
    
4. Chamar [IMessage:: ModifyRecipients](imessage-modifyrecipients.md), passando o ponteiro do **das ADRLIST** . Essa estrutura conterá as propriedades de cada um dos destinatários selecionados pelo usuário. 
    
 **Para criar uma lista de destinatários por programação**
  
1. Aloque uma estrutura **das ADRLIST** que contenha uma estrutura [ADRENTRY](adrentry.md) para cada um dos destinatários a serem incluídos na lista. Torne cada estrutura **ADRENTRY** grande o suficiente para reter cada uma das propriedades obrigatórias e **PR_RECIPIENT_TYPE** ([PidTagRecipientType](pidtagrecipienttype-canonical-property.md)).
    
2. Para cada destinatário, defina a matriz de valor da propriedade para seu membro **aEntries** na estrutura **das ADRLIST** . 
    
3. Chamar [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) com o sinalizador MODRECIP_ADD definido. 
    

