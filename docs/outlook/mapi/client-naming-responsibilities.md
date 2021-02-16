---
title: Responsabilidades de nomeação de cliente
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 808c7abf3d29872a8c5095fdc6dc39b2107a8993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424949"
---
# <a name="client-naming-responsibilities"></a>Responsabilidades de nomeação de cliente

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes devem seguir uma convenção de nomenal para suas propriedades que precisam ser traduzidas por um gateway. Todas as propriedades a serem traduzidas devem ser criadas como propriedades nomeadas em um dos cinco conjuntos de propriedades designados para manter as propriedades que podem ser usadas:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
As propriedades de endereçamento relacionadas ao mesmo usuário devem receber o mesmo nome. Os gateways dependem dessa convenção de nomenal, que permite que eles corresponderem a um endereço com seu tipo de endereço correto. Para análise de endereços, o mapeamento entre o endereço e o tipo de endereço deve ser preciso.
  
MapI named properties are represented with the **MAPINAMEID** data structure, which specifies that the property name can be either a Unicode string or a 32-bit integer. Para obter mais informações, [consulte MAPINAMEID](mapinameid.md). A nomeação de inteiro é recomendada para grupos de endereços porque é uma maneira simples de diferenciar entre conjuntos de propriedades mappable e pode servir facilmente como um índice para o usuário. A alternativa ao uso de inteiros é atribuir uma cadeia de caracteres como o nome de todas as cinco propriedades mappable de um usuário. Se apenas um usuário exigir mapeamento, atribuir uma cadeia de caracteres será aceitável. No entanto, quando há vários usuários, é melhor usar a nomeação de inteiro. O nome, seja numérico ou baseado em cadeia de caracteres, deve ser armazenado em uma propriedade específica da classe de mensagem ou em uma propriedade pertencente a um conjunto de propriedades definido pelo aplicativo cliente. 
  
> [!NOTE]
> Evite traduzir nomes inteiros para cadeias de caracteres, como "route_recipient_1" e "route_recipient_2". Esse esforço é desnecessário. 
  
Para ilustrar como essa convenção de nomenis funciona, considere um aplicativo de roteamento que envia uma mensagem para cada membro de uma equipe de quatro pessoas. Quando um membro recebe a mensagem, ele deve responder a ela antes que ela possa ser enviada junto com as respostas compiladas para o próximo membro. A mensagem original contém uma lista de destinatários com uma entrada: o primeiro membro da equipe. Incorporadas na mensagem estão as propriedades de gateway mappable para os outros três membros da equipe. Cada membro tem cinco propriedades de usuário principais residindo nos conjuntos de propriedades mappable de gateway, que são atribuídos a um número exclusivo como um nome. 
  
A tabela a seguir ilustra as configurações para cada conjunto de propriedades de gateway-mappable armazenadas para os três membros restantes da equipe para os quais a mensagem é roteada quando o primeiro membro da equipe é concluído com ela.
  
|**Property Set**|**Segundo Membro da  <br/> Equipe**|**Terceiro membro da  <br/> equipe**|**Quarto membro da  <br/> equipe**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Endereço = 0  <br/> |Endereço = 1  <br/> |Endereço = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Tipo de endereço = 0  <br/> |Tipo de endereço = 1  <br/> |Tipo de endereço = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nome de exibição = 0  <br/> |Nome de exibição = 1  <br/> |Nome para exibição = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificador de entrada = 0  <br/> |Identificador de entrada = 1  <br/> |Identificador de entrada = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Tecla de pesquisa = 0  <br/> |Tecla de pesquisa = 1  <br/> |Tecla de pesquisa = 2  <br/> |
   
Os clientes que usam chaves de pesquisa que podem ser usadas como referências a outras propriedades da mensagem devem reconhecer que as outras propriedades da mensagem não serão traduzidas, a menos que sejam colocadas em um desses conjuntos de propriedades mappable. Quando uma mensagem com referências não mapeadas a chaves de pesquisa mapeadas é enviada para um destino em outro domínio de mensagens, as referências são inválidas. Para permitir que essas outras propriedades permaneçam sincronizadas com as chaves de pesquisa, você pode atribuí-las nomes de cadeia de caracteres no conjunto de propriedades PS_ROUTING_SEARCH_KEY que não interferem com os nomes dados a nenhuma das propriedades mappable principais. Por exemplo, suponha que um cliente precise transmitir uma propriedade que contenha a chave de pesquisa para a última pessoa em uma longa lista de roteamento. O cliente pode criar uma propriedade nomeada no conjunto PS_ROUTING_SEARCH_KEY propriedade chamada "last_search_key". Como ela é armazenada em um conjunto de propriedades mappable, a propriedade "last_search_key" é traduzida juntamente com o restante das propriedades mappable do gateway.
  

