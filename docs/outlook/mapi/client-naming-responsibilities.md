---
title: Responsabilidades de nomenclatura do cliente
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
# <a name="client-naming-responsibilities"></a>Responsabilidades de nomenclatura do cliente

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os clientes devem seguir uma Convenção de nomenclatura para suas propriedades que precisam ser traduzidas por um gateway. Todas as propriedades a serem traduzidas devem ser criadas como propriedades nomeadas em um dos cinco conjuntos de propriedades designados para armazenar as propriedades mapeáveis:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
As propriedades de endereçamento relacionadas ao mesmo usuário devem receber o mesmo nome. Os gateways dependem dessa Convenção de nomenclatura, o que permite que eles correspondam a um endereço com o tipo de endereço correto. Para análise de endereço, o mapeamento entre endereço e tipo de endereço deve ser preciso.
  
As propriedades nomeadas de MAPI são representadas com a estrutura de dados **MAPINAMEID** , que especifica que o nome da propriedade pode ser uma cadeia de caracteres Unicode ou um inteiro de 32 bits. Para obter mais informações, consulte [MAPINAMEID](mapinameid.md). O nome de número inteiro é recomendado para grupos de endereços porque é uma maneira simples de diferenciar entre conjuntos de propriedades mapeáveis e pode servir facilmente como um índice para o usuário. A alternativa ao uso de inteiros é atribuir uma cadeia de caracteres como o nome para todas as cinco Propriedades mapeáveis de um usuário. Se apenas um usuário requer mapeamento, a atribuição de uma cadeia de caracteres é aceitável. No enTanto, quando há vários usuários, é melhor usar a nomenclatura de inteiro. O nome, se for numérico ou baseado em cadeia de caracteres, deve ser armazenado em uma propriedade específica da classe de mensagem ou em uma propriedade que pertença a um conjunto de propriedades definido pelo aplicativo cliente. 
  
> [!NOTE]
> Evite traduzir nomes de inteiros para cadeias de caracteres, como "route_recipient_1" e "route_recipient_2". Esse esforço é desnecessário. 
  
Para ilustrar como essa Convenção de nomenclatura funciona, considere um aplicativo de roteamento que envia uma mensagem para cada membro de uma equipe de quatro pessoas. Quando um membro recebe a mensagem, ele deve respondê-lo antes de poder ser enviado junto com as respostas compiladas para o próximo membro. A mensagem original contém uma lista de destinatários com uma entrada: o primeiro membro da equipe. Incorporado dentro da mensagem estão as propriedades do gateway que podem ser mapeados para os outros três membros da equipe. Cada membro tem cinco Propriedades de usuário principais que residem nos conjuntos de propriedades do gateway-mapeáveis, que recebem um número exclusivo como um nome. 
  
A tabela a seguir ilustra as configurações para cada conjunto de propriedades mapeadas de gateway armazenadas para os três membros restantes da equipe para os quais a mensagem é roteada quando o primeiro membro da equipe é concluído com ele.
  
|**Property Set**|**Segundo membro <br/> da equipe**|**Terceiro membro <br/> da equipe**|**Quarto membro <br/> da equipe**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Endereço = 0  <br/> |Endereço = 1  <br/> |Endereço = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Tipo de endereço = 0  <br/> |Tipo de endereço = 1  <br/> |Tipo de endereço = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nome para exibição = 0  <br/> |Nome para exibição = 1  <br/> |Nome para exibição = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |Identificador de entrada = 0  <br/> |Identificador de entrada = 1  <br/> |Identificador de entrada = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Chave de pesquisa = 0  <br/> |Chave de pesquisa = 1  <br/> |Chave de pesquisa = 2  <br/> |
   
Os clientes que usam chaves de pesquisa mapeadas como referências a outras propriedades de mensagem devem reconhecer que as outras propriedades de mensagem não serão traduzidas, a menos que sejam colocadas em um desses conjuntos de propriedades mapeados. Quando uma mensagem com referências não mapeadas para chaves de pesquisa mapeadas é enviada para um destino em outro domínio de mensagens, as referências são inválidas. Para permitir que essas outras propriedades permaneçam sincronizadas com as chaves de pesquisa, você pode atribuir nomes de cadeia de caracteres no conjunto de propriedades PS_ROUTING_SEARCH_KEY que não interfiram com os nomes fornecidos a qualquer uma das propriedades principais mapeáveis. Por exemplo, suponha que um cliente precisa transmitir uma propriedade que contém a chave de pesquisa para a última pessoa em uma lista de roteamento longa. O cliente pode criar uma propriedade nomeada no conjunto de propriedades PS_ROUTING_SEARCH_KEY chamado "last_search_key". Como ela é armazenada em um conjunto de propriedades mapeáveis, a propriedade "last_search_key" é convertida junto com o restante das propriedades do gateway-mapeáveis.
  

