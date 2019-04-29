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
ms.openlocfilehash: 14f9bff8dbf55456c37e70e1ae7a0c236471b6c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410599"
---
# <a name="mapi-address-book"></a>Catálogo de endereços MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O catálogo de endereços integrado é um objeto que o MAPI implementa para fornecer acesso a uma coleção integrada de informações de endereçamento de todos os provedores de catálogo de endereços no perfil. Com o catálogo de endereços, os aplicativos cliente e os provedores de serviços não precisam diferenciar entre os esquemas de endereçamento exclusivos dos sistemas de mensagens. Em vez disso, eles podem pesquisar os endereços de qualquer destinatário em qualquer sistema de mensagens, desde que o provedor de catálogo de endereços do sistema de mensagens esteja instalado.
  
O catálogo de endereços pode ser acessado programaticamente, sem intervenção do usuário ou interativamente por meio do uso de caixas de diálogo comuns. MAPI inclui caixas de diálogo para exibir uma lista resumida das entradas no catálogo de endereços, informações detalhadas sobre um determinado destinatário, um aviso quando um usuário cria um destinatário que não pode ser mapeado para um endereço exclusivo e um conjunto de formulários de modelo para criar novos Eles.
  
O catálogo de endereços MAPI é semelhante em estrutura a um repositório de mensagens, pois ele é organizado hierarquicamente. O catálogo de endereços fornece acesso a três tipos de objetos implementados por um provedor de catálogo de endereços:
  
- Abrir o contêiner de um objeto do catálogo de endereços.
    
- 0" não é um objeto de lista de distribuição.
    
- Um objeto de usuário de mensagens.
    
Cada um desses tipos de objetos é acessado por meio de seu identificador de entrada exclusivo que é atribuído pelo seu provedor de catálogo de endereços. 
  
Os contêineres do catálogo de endereços são semelhantes às pastas nas quais eles contêm objetos de tipos diferentes. Um contêiner de catálogo de endereços pode conter outros contêineres de catálogo de endereços, bem como usuários de mensagens e de lista de distribuição. Os contêineres do catálogo de endereços são usados para organizar e armazenar objetos de catálogo de endereços.
  
Para obter a aparência integrada do catálogo de endereços, os provedores de catálogos de endereços expõem zero, um ou mais de seus contêineres de nível superior para MAPI que os mescla e exibe os resultados em um único contêiner de nível superior. Os provedores de catálogos de endereços podem optar por expor um conjunto de contêineres para um tipo de sessão de mensagens e um conjunto diferente para outra sessão. Também é possível que os provedores de catálogo de endereços não tenham contêineres de nível superior e exponham apenas uma lista de modelos que podem ser usados para criar destinatários.
  
Os destinatários da mensagem são implementados com o usuário de mensagens e os objetos de lista de distribuição. Os usuários de mensagens são destinatários individuais; as listas de distribuição são destinatários de grupo. Cada usuário de sistema de mensagens tem um endereço exclusivo de um tipo específico tratado por um sistema de mensagens específico. Uma lista de distribuição é uma coleção nomeada de destinatários. As listas de distribuição podem conter objetos de usuário de mensagens e outras listas de distribuição. Quando um usuário de um aplicativo cliente envia uma mensagem para uma lista de distribuição, a mensagem é enviada a cada um dos membros do usuário de mensagens da lista. 
  
Os usuários de mensagens e as listas de distribuição têm um conjunto de cinco propriedades conhecidas como as propriedades de endereço base. Essas são propriedades obrigatórias e são descritas brevemente da seguinte maneira.
  
|**Propriedade de endereço base**|**Descrição**|
|:-----|:-----|
|**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))  <br/> |Tipo de endereço do destinatário. Cada tipo de endereço segue um formato específico e é usado com um sistema de mensagens específico.  <br/> |
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Nome para exibição do destinatário.  <br/> |
|**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))  <br/> |Endereço do destinatário.  <br/> |
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Identificador de entrada usado para acessar o destinatário.  <br/> |
|**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))  <br/> |Chave semelhante binária usada para identificar o destinatário.  <br/> |
   
MAPI define muitos grupos de propriedades que são variações das propriedades de endereço base. Esses outros grupos descrevem os usuários de mensagens e as listas de distribuição em diferentes situações. Por exemplo, um grupo de propriedades descreve o remetente de representante de uma mensagem e outro grupo o destinatário do representante.
  

