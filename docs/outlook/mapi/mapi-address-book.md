---
title: Catálogo de endereços MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6703ba3f-54a5-4059-b10a-1d42a9e81be1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b328a65f400e424fb2cd177e710fb8bcffa392c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767797"
---
# <a name="mapi-address-book"></a>Catálogo de endereços MAPI

  
  
**Aplica-se a**: Outlook 
  
O catálogo de endereços integrada é um objeto que implementa a MAPI para fornecer acesso a uma coleção integrada de informações de endereçamento de todos os provedores de catálogo de endereços no perfil. Com o catálogo de endereços, provedores de serviços e aplicativos cliente não precisará diferenciar entre os esquemas de endereçamento exclusivos de sistemas de mensagens. Em vez disso, elas podem consultar os endereços de quaisquer destinatários em qualquer sistema de mensagens, desde que o provedor de catálogo de endereços para o sistema de mensagens está instalado.
  
O catálogo de endereços pode ser acessado por meio de programação, sem a intervenção do usuário ou interativamente devido ao uso de caixas de diálogo comuns. MAPI inclui caixas de diálogo para exibir uma lista resumida das entradas no catálogo de endereços, informações detalhadas sobre um destinatário específico, um aviso quando um usuário cria um destinatário que não pode ser mapeado para um endereço exclusivo e um conjunto de formulários de modelo para a criação de novos destinatários.
  
O catálogo de endereços MAPI é semelhante na estrutura a um armazenamento de mensagens estão organizados hierarquicamente. O catálogo de endereços fornece acesso a três tipos de objetos implementados por um fornecedor de catálogo de endereços:
  
- Um objeto de contêiner de catálogo de endereços.
    
- Um objeto de lista de distribuição.
    
- Um objeto de usuário de mensagens.
    
Cada um desses tipos de objetos é acessado através de seu identificador exclusivo de entrada que é atribuído pelo seu provedor de catálogo de endereços. 
  
Contêineres de catálogo de endereços são semelhantes às pastas em que eles objetos de tipos diferentes de espera. Um contêiner de catálogo de endereços pode conter outros contêineres do catálogo de endereços, bem como objetos de usuário e a distribuição da lista de mensagens. Contêineres de catálogo de endereços são usados para organizar e armazenar objetos de catálogo de endereços.
  
Para obter a aparência de integrado do catálogo de endereços, provedores de catálogo de endereços exponham zero, um ou mais dos seus contêineres de nível superior a MAPI que mescla-los e exibe os resultados em um único contêiner de nível superior. Provedores de catálogo de endereços podem optar por expor um conjunto de recipientes para um tipo de sessão e um conjunto diferente de mensagens para outra sessão. Também é possível para provedores de catálogo de endereços não ter nenhum recipientes de nível superior e expor somente uma lista de modelos que podem ser usados para criar os destinatários.
  
Os destinatários da mensagem são implementados com mensagens do usuário e objetos de lista de distribuição. Mensagens de usuários são destinatários individuais; as listas de distribuição são os destinatários do grupo. Cada usuário mensagens tem um endereço exclusivo de um determinado tipo manipulado por um sistema de mensagens específico. Uma lista de distribuição é um conjunto nomeado de destinatários. Listas de distribuição podem conter objetos de usuário de mensagens e outras listas de distribuição. Quando um usuário de um aplicativo cliente envia uma mensagem para uma lista de distribuição, a mensagem está sendo enviada para cada um dos membros de usuário mensagens da lista. 
  
Usuários de mensagens e listas de distribuição têm um conjunto de cinco propriedades que são conhecidas como as propriedades de endereço base. Essas são as propriedades necessárias e são descritas resumidamente como a seguir.
  
|**Propriedade endereço base**|**Descrição**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tipo de endereço do destinatário. Cada tipo de endereço segue um determinado formato e é usado com um sistema de mensagens específico.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Nome para exibição para o destinatário.  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Endereço do destinatário.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Identificador de entrada usado para acessar o destinatário.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Tecla comparável binária usada para identificar o destinatário.  <br/> |
   
MAPI define vários grupos de propriedades que são variações das propriedades de endereço base. Esses outros grupos descrevem mensagens de usuários e listas de distribuição em situações diferentes. Por exemplo, um grupo de propriedades descreve o remetente do representante de uma mensagem e o destinatário do representante de outro grupo.
  

