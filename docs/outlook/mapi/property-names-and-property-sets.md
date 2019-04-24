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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328543"
---
# <a name="property-names-and-property-sets"></a>Nomes de propriedades e conjuntos de propriedades

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O nome de cada propriedade nomeada tem duas partes:
  
- Um identificador global exclusivo, ou GUID, que especifica um conjunto de propriedades.
    
- Uma cadeia de caracteres Unicode ou um valor numérico de 32 bits. 
    
Os nomes das propriedades nomeadas são descritos usando uma estrutura [MAPINAMEID](mapinameid.md) . Esta estrutura contém um membro de conjunto de propriedades, um membro para especificar o nome em formato numérico ou de cadeia de caracteres e um membro para identificar qual formato é usado. Como o conjunto de propriedades é parte do nome da propriedade, ele não é opcional. O MAPI definiu vários conjuntos de propriedades para uso por clientes e provedores de serviço, mas se um conjunto de propriedades existente for inapropriado, um novo conjunto de propriedades poderá ser definido. Os clientes e provedores de serviços podem definir seus próprios conjuntos de propriedades chamando [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) função. Normalmente, esses conjuntos de propriedades são criados para aplicativos cliente personalizados. 
  
Os conjuntos de propriedades de MAPI são representados pelas seguintes constantes:
  
PS_MAPI
  
PS_PUBLIC_STRINGS
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_SEARCH_KEY
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
O conjunto de propriedades PS_MAPI é reservado; Ele é usado por provedores de serviços para gerar nomes para propriedades com identificadores abaixo do intervalo de propriedades nomeados. O conjunto de propriedades PS_PUBLIC_STRINGS é usado por clientes para propriedades nomeadas de mensagens IPM. Como as propriedades nomeadas no conjunto de propriedades PS_PUBLIC_STRINGS aparecem na interface de usuário de um cliente, as mensagens não visíveis, como as que pertencem à classe de mensagens de IPC, devem evitar a criação de propriedades nomeadas com esse conjunto de propriedades. Em vez disso, eles devem criar propriedades no intervalo específico de classe de mensagem, 0x6800 a 0x7FFF.
  
A outra propriedade define as propriedades nomeadas que descrevem destinatários que normalmente são membros de uma lista de circulação. Contendo o mesmo tipo de informação que as propriedades associadas às propriedades da lista de destinatários, as propriedades nesses conjuntos de propriedades são compreendidas pelos gateways para exigir o mapeamento de um sistema de mensagens de destino. Como há cinco tipos de informações para descrever as propriedades, o MAPI definiu cinco conjuntos de propriedades diferentes. Um cliente que envia uma mensagem que deve incluir um endereço e tipo de endereço para seus membros da lista de circulação atribui uma propriedade nomeada para cada membro nos conjuntos de propriedades PS_ROUTING_EMAIL_ADDRESSES e PS_ROUTING_ADDRTYPE. Isso garante que o endereço e o tipo de endereço permaneçam viáveis quando enviados para um sistema de mensagens externas.
  
## <a name="see-also"></a>Confira também



[MAPI denominada propriedades](mapi-named-properties.md)

