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
  
Chaves de registro e chaves de pesquisa são identificadores binários atribuídos a muitos objetos MAPI. Ao contrário do identificador de entrada de um objeto, seu registro ou chave de pesquisa é diretamente comparável, bem como transmitível. 
  
## <a name="record-keys"></a>Chaves de Registro

Uma tecla de registro é usada para comparar dois objetos. Os objetos do armazenamento de mensagens e do livro de endereços devem ter chaves de registro, que são armazenadas **na** PR_RECORD_KEY ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) . Como uma chave de registro identifica um objeto e não seus dados, cada instância de um objeto tem uma chave de registro exclusiva. O escopo de uma chave de registro para pastas e mensagens é o armazenamento de mensagens. O escopo para contêineres de agendamento de endereços, usuários de mensagens e listas de distribuição é o conjunto de contêineres de nível superior fornecido pelo MAPI para uso no livro de endereços integrado.
  
As chaves de registro podem ser duplicadas em outro recurso. Por exemplo, mensagens diferentes em dois armazenamentos de mensagens diferentes podem ter a mesma chave de registro. Isso é diferente dos identificadores de entrada de longo prazo; como os identificadores de entrada de longo prazo contêm uma referência ao provedor de serviços, eles têm um escopo mais amplo. A chave de registro de um armazenamento de mensagens é semelhante em escopo a um identificador de entrada de longo prazo; deve ser exclusivo em todos os provedores de armazenamento de mensagens. Para garantir essa exclusividade, os provedores de repositório de mensagens geralmente configuram sua chave de registro como um valor que é a combinação de sua propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) e um identificador exclusivo para o repositório de mensagens.
  
## <a name="search-keys"></a>Teclas de pesquisa

Uma chave de pesquisa é usada para comparar os dados em dois objetos. A chave de pesquisa de um objeto é armazenada em **sua PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) . Como uma chave de pesquisa representa os dados de um objeto e não o próprio objeto, dois objetos diferentes com os mesmos dados podem ter a mesma chave de pesquisa. Quando um objeto é copiado, por exemplo, o objeto original e sua cópia têm os mesmos dados e a mesma chave de pesquisa.
  
Os usuários de mensagens e mensagens têm chaves de pesquisa. A chave de pesquisa de uma mensagem é um identificador exclusivo dos dados da mensagem. Os provedores de armazenamento de mensagens armazenam a propriedade PR_SEARCH_KEY mensagem **no** momento da criação da mensagem. A chave de pesquisa de uma entrada de livro de endereços é calculada a partir de seu tipo de endereço (**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))) e endereço (**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))). Se a entrada do livro de endereços for writeable, sua chave de pesquisa poderá não estar disponível até que o tipo de endereço e o endereço tenham sido definidos usando o método [IMAPIProp::SetProps](imapiprop-setprops.md) e a entrada tenha sido salva usando o método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Quando essas propriedades de endereço mudam, é possível que a chave de pesquisa correspondente não seja sincronizada com os novos valores até que as alterações tenham sido comprometidas com uma **chamada SaveChanges.** 
  
O valor da chave de registro de um objeto pode ser igual ou diferente do valor de sua chave de pesquisa, dependendo do provedor de serviços. Alguns provedores de serviços usam o mesmo valor para a chave de pesquisa, a chave de registro e o identificador de entrada de um objeto. Outros provedores de serviços atribuem valores exclusivos para cada um dos identificadores de seus objetos. 
  
## <a name="see-also"></a>Confira também



[Desenvolvimento de aplicativos MAPI](mapi-application-development.md)

