---
title: Nomes de propriedades e conjuntos de propriedades
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391651"
---
# <a name="property-names-and-property-sets"></a>Nomes de propriedades e conjuntos de propriedades

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O nome de cada propriedade nomeada tem duas partes:
  
- Um identificador global exclusivo ou GUID, que especifica um conjunto de propriedades.
    
- Uma cadeia de caracteres Unicode ou o valor numérico de 32 bits. 
    
Nomes de propriedades nomeadas são descritos usando uma estrutura [MAPINAMEID](mapinameid.md) . Essa estrutura contém um membro do conjunto de propriedade, um membro para especificar o nome no formato numérico ou cadeia de caracteres e para identificar qual formato é usado. Como o conjunto de propriedades é parte do nome da propriedade, não é opcional. MAPI definiu vários conjuntos de propriedade para uso por clientes e provedores de serviço, mas se um conjunto existente de propriedade for inadequado, um novo conjunto de propriedades pode ser definido. Clientes e provedores de serviços podem definir seus próprios conjuntos de propriedade chamando [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) função. Normalmente, esses conjuntos de propriedade são criados para os aplicativos cliente personalizados. 
  
Conjuntos de propriedades do MAPI são representados por constantes a seguir:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
O conjunto de propriedades PS_MAPI está reservado; ele é usado pelos provedores de serviços para gerar nomes de propriedades com identificadores abaixo do intervalo de propriedade nomeada. O conjunto de propriedades PS_PUBLIC_STRINGS é usado pelos clientes para propriedades nomeadas das mensagens IPM. Como propriedades nomeadas no conjunto de propriedades PS_PUBLIC_STRINGS aparecem na interface de usuário do cliente, mensagens arquvo, tais como aqueles que pertencem à classe de mensagem CPI devem evitar a criação de chamada propriedades com este conjunto de propriedades. Em vez disso, eles devem criar propriedades no intervalo de específicas de classe de mensagem, 0x6800 por meio de 0x7FFF.
  
Os outros conjuntos de propriedade espera propriedades nomeadas descrevendo os destinatários que geralmente são membros de uma lista de roteamento. Propriedades nesses conjuntos de propriedade que contém o mesmo tipo de informações como as propriedades que estão associadas com propriedades da lista de destinatários, são compreendidas por gateways para exigir o mapeamento para um sistema de mensagens de destino. Como há cinco tipos de informações para descrição das propriedades, MAPI definiu cinco conjuntos de propriedade diferentes. Um cliente enviando uma mensagem que deve incluir um endereço e o tipo de endereço para seus membros da lista roteamento atribui uma propriedade nomeada para cada membro na PS_ROUTING_EMAIL_ADDRESSES e a propriedade PS_ROUTING_ADDRTYPE define. Isso garante que o endereço e o tipo de endereço permaneçam viáveis quando enviado para um sistema de mensagens externo.
  
## <a name="see-also"></a>Confira também



[MAPI denominada propriedades](mapi-named-properties.md)

