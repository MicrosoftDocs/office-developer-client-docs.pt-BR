---
title: Registro MAPI e chaves de pesquisa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4aa641ad0a41ff8015d2ece717d5a4cb3a7c4edf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587310"
---
# <a name="mapi-record-and-search-keys"></a>Registro MAPI e chaves de pesquisa

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chaves de registro e chaves de pesquisa são identificadores binários que são atribuídos a vários objetos MAPI. Ao contrário do identificador de entrada de um objeto, sua chave de registro ou pesquisar diretamente é comparável tão transmittable. 
  
## <a name="record-keys"></a>Chaves do registros

Uma chave de registro é usada para comparar dois objetos. Armazenamento de mensagens e o endereço de objetos de catálogo devem ter as chaves de registro, que são armazenadas em sua propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Como uma chave de registro identifica um objeto e não seus dados, cada instância de um objeto tem uma chave de registro exclusivo. O escopo de uma chave de registro para mensagens e pastas é o armazenamento de mensagens. O escopo dos contêineres do catálogo de endereços, mensagens de usuários e listas de distribuição é o conjunto de nível superior contêineres fornecidos pelo MAPI para uso no catálogo de endereços integrada.
  
Chaves do registros podem ser copiadas em outro recurso. Por exemplo, mensagens diferentes em dois repositórios de mensagem diferente podem ter a mesma chave do registro. Isso é diferente de longo prazo identificadores de entrada; como os identificadores de entrada de longo prazo contenham uma referência para o provedor de serviço, eles têm um escopo mais amplo. Chave de registro de um armazenamento de mensagens é semelhante em escopo a um identificador de entrada de longo prazo; ele deve ser exclusivo entre todos os provedores de armazenamento de mensagem. Para garantir que este exclusividade, provedores de armazenamento de mensagem normalmente defina sua chave do registro como um valor que é a combinação de sua propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) e um identificador exclusivo para o armazenamento de mensagens.
  
## <a name="search-keys"></a>Chaves de pesquisa

Uma chave de pesquisa é usada para comparar os dados nos dois objetos. Chave de pesquisa de um objeto é armazenado em sua propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Como uma chave de pesquisa representa os dados de um objeto e não o próprio objeto, dois objetos diferentes com os mesmos dados podem ter a mesma chave de pesquisa. Quando um objeto é copiado, por exemplo, o objeto original e sua cópia tem os mesmos dados e a mesma chave de pesquisa.
  
Mensagens e mensagens de usuários têm chaves de pesquisa. A chave de pesquisa de uma mensagem é um identificador exclusivo de dados da mensagem. Provedores de armazenamento de mensagem fornecer à propriedade **PR_SEARCH_KEY** da mensagem no momento da criação de mensagem. A chave de pesquisa de uma entrada de catálogo de endereços é calculada a partir de seu tipo de endereço (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) e o endereço (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Se a entrada do catálogo de endereços for gravável, sua chave de pesquisa pode não estar disponível até que o tipo de endereço e o endereço foram definidos usando o método [IMAPIProp::SetProps](imapiprop-setprops.md) e a entrada tiver sido salvo usando o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Quando essas propriedades de endereço alteram, é possível para a chave de pesquisa correspondente para não ser sincronizado com os novos valores até que as alterações forem confirmadas com uma chamada **SaveChanges** . 
  
O valor da chave de registro de um objeto pode ser igual ou diferente do que o valor da sua chave de pesquisa, dependendo do provedor de serviço. Alguns provedores de serviço usam o mesmo valor para a chave de pesquisa de um objeto, a chave do registro e o identificador de entrada. Outros provedores de serviços atribuem valores exclusivos para cada um dos identificadores dos seus objetos. 
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

