---
title: Registro MAPI e chaves de pesquisa
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: caa7b7f3-a5a1-4f07-98c9-22652ecd5d21
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b1b4c0087cecd9164fc96ce7c5b5415f75dbfb03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434561"
---
# <a name="mapi-record-and-search-keys"></a>Registro MAPI e chaves de pesquisa

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chaves de registro e chaves de pesquisa são identificadores binários atribuídos a vários objetos MAPI. Ao contrário do identificador de entrada de um objeto, seu registro ou chave de pesquisa é diretamente comparável, bem como a transmittable. 
  
## <a name="record-keys"></a>Chaves de registro

Uma chave de registro é usada para comparar dois objetos. O repositório de mensagens e os objetos do catálogo de endereços devem ter chaves de registro, que são armazenadas na propriedade **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)). Como uma chave de registro identifica um objeto e não seus dados, cada instância de um objeto tem uma chave de registro exclusiva. O escopo de uma chave de registro para pastas e mensagens é o repositório de mensagens. O escopo para contêineres do catálogo de endereços, usuários de mensagens e listas de distribuição é o conjunto de contêineres de nível superior fornecido pelo MAPI para uso no catálogo de endereços integrado.
  
As chaves de registro podem ser duplicadas em outro recurso. Por exemplo, diferentes mensagens em dois repositórios de mensagens diferentes podem ter a mesma chave de registro. Isso é diferente dos identificadores de entrada de longo prazo; como os identificadores de entrada de longo prazo contêm uma referência ao provedor de serviços, eles têm um escopo mais amplo. Uma chave de registro do repositório de mensagens é semelhante em escopo a um identificador de entrada de longo prazo; Ele deve ser exclusivo em todos os provedores de repositórios de mensagens. Para garantir essa exclusividade, os provedores de repositórios de mensagens normalmente definem a chave de registro como um valor que é a combinação de sua propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) e um identificador exclusivo para o repositório de mensagens.
  
## <a name="search-keys"></a>Chaves de pesquisa

Uma chave de pesquisa é usada para comparar os dados em dois objetos. A chave de pesquisa de um objeto é armazenada em sua propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Como uma chave de pesquisa representa os dados de um objeto e não o próprio objeto, dois objetos diferentes com os mesmos dados podem ter a mesma chave de pesquisa. Quando um objeto é copiado, por exemplo, o objeto original e sua cópia têm os mesmos dados e a mesma chave de pesquisa.
  
Mensagens e usuários de mensagens têm chaves de pesquisa. A chave de pesquisa de uma mensagem é um identificador exclusivo dos dados da mensagem. Provedores de repositórios de mensagens forneça a propriedade **PR_SEARCH_KEY** de uma mensagem na hora de criação da mensagem. A chave de pesquisa de uma entrada do catálogo de endereços é calculada a partir de seu tipo de endereço (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) e endereço (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Se a entrada do catálogo de endereços for gravável, sua chave de pesquisa pode não estar disponível até que o tipo de endereço e endereço tenha sido definido usando o método [IMAPIProp::](imapiprop-setprops.md) SetProps e a entrada tenha sido salva usando o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Quando essas propriedades de endereço mudam, é possível que a chave de pesquisa correspondente não seja sincronizada com os novos valores até que as alterações tenham sido confirmadas com uma chamada **SaveChanges** . 
  
O valor da chave de registro de um objeto pode ser o mesmo ou diferente do valor de sua chave de pesquisa, dependendo do provedor de serviços. Alguns provedores de serviços usam o mesmo valor para a chave de pesquisa, chave de registro e identificador de entrada de um objeto. Outros provedores de serviços atribuem valores exclusivos para cada um dos seus identificadores de objetos. 
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

