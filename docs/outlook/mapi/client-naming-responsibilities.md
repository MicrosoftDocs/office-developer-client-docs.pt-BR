---
title: Responsabilidades de nomenclatura de cliente
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: dbb6ba5f-18c8-426f-9f50-ce6f2fd1dc5b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: a97d108b2f36b40e5f8818ea81c138d7384ce9b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766295"
---
# <a name="client-naming-responsibilities"></a>Responsabilidades de nomenclatura de cliente

  
  
**Aplica-se a**: Outlook 
  
Os clientes devem seguir uma convenção de nomenclatura para suas propriedades que precisam ser traduzidos por um gateway. Todas as propriedades a serem convertidos devem ser criadas como propriedades nomeadas em um dos conjuntos de cinco propriedade designados para manter as propriedades podem ser mapeadas:
  
PS_ROUTING_EMAIL_ADDRESSES
  
PS_ROUTING_ADDRTYPE
  
PS_ROUTING_DISPLAY_NAME
  
PS_ROUTING_ENTRYID
  
PS_ROUTING_SEARCH_KEY
  
Lidando com as propriedades que se relacionam com o mesmo usuário deve ser fornecido o mesmo nome. Gateways contam com essa convenção de nomenclatura, que permite que eles corresponder a um endereço com seu tipo de endereço correto. Para análise de endereço, o mapeamento entre o endereço e o tipo de endereço deve ser exatos.
  
MAPI denominada propriedades são representadas com a estrutura de dados **MAPINAMEID** , que especifica se o nome da propriedade pode ser uma cadeia de caracteres Unicode ou um inteiro de 32 bits. Para obter mais informações, consulte [MAPINAMEID](mapinameid.md). Inteiro de nomenclatura é recomendada para grupos de endereços porque ele é uma maneira simples para diferenciar entre conjuntos de propriedades podem ser mapeados, e ele facilmente pode servir como um índice para o usuário. Uma alternativa ao uso de números inteiros é atribuir uma cadeia de caracteres, como o nome para todos os cinco das propriedades de um usuário podem ser mapeados. Se apenas um usuário requer o mapeamento, atribuir uma cadeia de caracteres é aceitável. No entanto, quando houver vários usuários, é melhor usar a nomenclatura de inteiro. O nome, se ele ser numérico ou baseado em cadeia de caracteres deve ser armazenado em uma propriedade de específicas de classe de mensagem ou em uma propriedade que pertencem a um conjunto de propriedades que é definido pelo aplicativo cliente. 
  
> [!NOTE]
> Evitar a converter nomes de inteiro em cadeias de caracteres, como "route_recipient_1" e "route_recipient_2". Essa iniciativa é desnecessária. 
  
Para ilustrar como funciona a essa convenção de nomenclatura, considere a possibilidade de um aplicativo de roteamento que envia uma mensagem para cada membro de uma equipe de quatro pessoas. Quando um membro recebe a mensagem, ele deve responder a ele para que possa ser enviado, juntamente com as respostas compiladas para o próximo membro. A mensagem original contém uma lista de destinatários com uma entrada: o primeiro membro da equipe. Incorporado dentro da mensagem são as propriedades podem ser mapeados gateway para os outros membros da equipe três. Cada membro tem cinco propriedades de usuário principal que residem nos conjuntos de propriedades podem ser mapeados gateway, que são atribuídos a um número exclusivo, como um nome. 
  
A tabela a seguir ilustra as configurações para cada conjunto de propriedades podem ser mapeados gateway armazenados para os três restantes membros da equipe a quem a mensagem é roteada quando o primeiro membro da equipe for concluído com ele.
  
|**Conjunto de propriedades**|**Segunda equipe <br/> membro**|**Terceiro equipe <br/> membro**|**Quarto da equipe <br/> membro**|
|:-----|:-----|:-----|:-----|
|PS_ROUTING_EMAIL_ADDRESSES  <br/> |Endereço = 0  <br/> |Endereço = 1  <br/> |Endereço = 2  <br/> |
|PS_ROUTING_ADDRTYPE  <br/> |Tipo de endereço = 0  <br/> |Tipo de endereço = 1  <br/> |Tipo de endereço = 2  <br/> |
|PS_ROUTING_DISPLAY_NAME  <br/> |Nome para exibição = 0  <br/> |Nome para exibição = 1  <br/> |Nome para exibição = 2  <br/> |
|PS_ROUTING_ENTRYID  <br/> |O identificador de entrada = 0  <br/> |O identificador de entrada = 1  <br/> |O identificador de entrada = 2  <br/> |
|PS_ROUTING_SEARCH_KEY  <br/> |Chave de pesquisa = 0  <br/> |Chave de pesquisa = 1  <br/> |Chave de pesquisa = 2  <br/> |
   
Clientes que usam chaves de pesquisa podem ser mapeados como referências a outras propriedades de mensagem devem reconhecer que as outras propriedades de mensagem não serão traduzidas, a menos que eles são colocados em um desses conjuntos de propriedade podem ser mapeados. Quando uma mensagem com referências não mapeadas para chaves de pesquisa mapeado é enviada para um destino em outro domínio de mensagens, as referências são inválidas. Para habilitar essas outras propriedades permaneça sincronizado com as chaves de pesquisa, você pode atribuir a eles nomes de cadeia de caracteres no conjunto de propriedades PS_ROUTING_SEARCH_KEY que não interferem os nomes de dado a qualquer uma das propriedades podem ser mapeados core. Por exemplo, suponha que um cliente precisa transmitir uma propriedade que contém a chave de pesquisa para a última pessoa em uma lista de circulação longos. O cliente pode criar uma propriedade nomeada no conjunto de propriedades PS_ROUTING_SEARCH_KEY chamado "last_search_key". Porque ele está armazenado em um conjunto de propriedades podem ser mapeados, a propriedade "last_search_key" é traduzida junto com o restante das propriedades podem ser mapeados gateway.
  

