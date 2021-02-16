---
title: Perfis MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9db1f8e163e44a44df1e798cebccb3639325275e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340079"
---
# <a name="mapi-profiles"></a>Perfis MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um perfil armazena informações sobre provedores de serviços e serviços de mensagens instalados em um computador. Para cada sessão, um cliente no momento do logon seleciona um perfil que descreve os provedores e serviços a serem usados. Um cliente pode escolher entre um conjunto de perfis e, se desejado, estabelecer um como padrão. O perfil padrão é o perfil selecionado automaticamente quando um cliente inicia uma sessão e não especificou explicitamente um perfil.
  
Além disso, nestes tópicos, você encontrará uma discussão sobre o cache de apelidos, que é armazenado em um fluxo binário.
  
- [Cache de apelidos](nickname-cache.md)
    
- [Fluxo de Preenchimento Automático](autocomplete-stream.md)
    
- [Análise de arquivo binário](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Seções de Perfil

Os perfis são divididos em seções que os clientes e provedores de serviços acessam para exibir as propriedades de perfil para os usuários ou para fazer alterações na configuração. Uma seção de perfil é um objeto MAPI que implementa a interface **IProfSect,** uma interface que deriva de **IMAPIProp** e não tem métodos adicionais. Para obter mais informações, consulte [IProfSect : IMAPIProp](iprofsectimapiprop.md). Sua única finalidade é manipular as propriedades de uma seção de perfil. Para recuperar um **ponteiro IProfSect** para uma seção de perfil específica, os clientes e provedores de serviços chamam os métodos a seguir. 
  
|||
|:-----|:-----|
|Os clientes podem chamar:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Os provedores de serviços podem chamar:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Clientes ou provedores podem chamar:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Os perfis são organizados hierarquicamente de forma muito parecido com o MAPISVC. Arquivo INF. Na parte superior da hierarquia, há seções de perfil que contêm informações relevantes para o perfil. O nível intermediário inclui seções que contêm informações sobre um determinado serviço de mensagens e o nível inferior inclui seções que contêm informações sobre um dos provedores de serviços em um serviço de mensagens. 
  
Cada perfil tem várias propriedades necessárias que são armazenadas em uma ou mais das seções do perfil. Por exemplo, cada perfil tem PR_PROFILE_NAME **(** [PidTagProfileName](pidtagprofilename-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) propriedades. A chave de pesquisa de um perfil é definida como o valor definido em MAPIGUID. H como MUID_PROFILE_INSTANCE e é sempre garantido ser exclusivo entre todos os perfis. Embora dois perfis possam ter o mesmo nome, eles não podem ter a mesma chave de pesquisa. As chaves de pesquisa devem ser tratadas como dados binários em vez de dados de qualquer tipo específico.
  
Os provedores de armazenamento de mensagens são obrigados a incluir a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)do seu armazenamento de mensagens nas seções de perfil para o perfil e para seu provedor de armazenamento de mensagens e para manter essas entradas sincronizadas. Quando um armazenamento de mensagens é criado, o provedor **define PR_DISPLAY_NAME** com base no valor armazenado nessas seções de perfil. 
  
Há duas diferenças principais entre seções de perfil e outros objetos que herdam de **IMAPIProp:** 
  
- As seções de perfil não são suportadas por transações.
    
- As seções de perfil não têm suporte para propriedades nomeadas, retornando MAPI_E_NO_SUPPORT de suas implementações **IMAPIProp::GetIDsFromNames** e **IMAPIProp::GetNamesFromIDs.** Para obter mais informações, consulte [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Como as seções de perfil não suportam transações, qualquer alteração feita com chamadas para **IMAPIProp::CopyProps**, **CopyTo** ou **SetProps** entrou em vigor imediatamente. Para obter mais informações, [consulte IMAPIProp::CopyProps](imapiprop-copyprops.md). Clientes e provedores de serviços podem chamar o método **IMAPIProp::SaveChanges** da seção de perfil e ele terá êxito, mas não afeta os dados da seção de perfil. Para obter mais informações, [consulte IMAPIProp::SaveChanges](imapiprop-savechanges.md). As alterações que ocorrem imediatamente podem afetar como os provedores de serviços implementam as folhas de propriedades que os clientes usam para exibir as propriedades de perfil para os usuários. Provedores de serviços que querem que os usuários sejam capazes de adiar ou desfazer alterações devem implementar suas folhas de propriedades com cópias de seções de perfil em vez das seções reais. Usando cópias, os usuários podem fazer alterações e, em seguida, cancelar essas alterações, deixando as seções de perfil originais intocadas. 
  
A ordem na qual as informações aparecem em um perfil afeta como o MAPI configura recursos e faz atribuições em uma sessão. As atribuições a seguir são afetadas pela ordem do perfil:
  
- Armazenamento de mensagens padrão
    
- Personal address book
    
- Caminho de pesquisa do armazenamento de mensagens padrão
    
- Caminho de pesquisa do livro de endereços padrão
    
- Ordem do provedor de transporte
    
MAPI sets the default message store to be the first message store in the profile that has the STATUS_DEFAULT_STORE flag set in its **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) property, which indicates that it can be the default store. Os clientes podem substituir essa configuração chamando **IMAPISession::SetDefaultStore**. Para obter mais informações, [consulte IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI creates a transport order for handling outgoing and incoming messages. Quando mais de um provedor de transporte é registrado para uma mensagem de um tipo específico, o MAPI usa essa ordem para determinar qual provedor deve lidar com a mensagem. MAPI sets the transport order to be the order in which the transport providers were added to the profile with one exception -- the transports that set the STATUS_XP_PREFER_LAST flag in their **PR_RESOURCE_FLAGS** property are positioned last in the order. Os clientes podem definir a ordem de transporte **chamando IMsgServiceAdmin::MsgServiceTransportOrder**. Para obter mais informações, consulte [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Essas diretrizes para ordenação de provedores de serviços e serviços de mensagens podem, às vezes, conflitar. Se houver um conflito, seu código deverá resolver o conflito. Você pode usar o programa Painel de Controle de Email para inspecionar um perfil criado para determinar se os provedores foram configurados conforme o esperado.
  

