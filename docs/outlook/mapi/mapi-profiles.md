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
  
Um perfil armazena informações sobre provedores de serviço e serviços de mensagens que estão instalados em um computador. Para cada sessão, um cliente no horário de logon seleciona um perfil que descreve os provedores e serviços a serem usados. Um cliente pode escolher entre uma coleção de perfis e, se desejar, estabelecer um como padrão. O perfil padrão é o perfil selecionado automaticamente quando um cliente inicia uma sessão e não especificou explicitamente um perfil.
  
Além disso, nestes tópicos, você encontrará uma discussão sobre o cache de Alcunha, que é armazenado em um fluxo binário.
  
- [Cache de apelidos](nickname-cache.md)
    
- [Fluxo de preenchimento automático](autocomplete-stream.md)
    
- [Análise de arquivo binário](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Seções de perfil

Os perfis são divididos em seções que os clientes e provedores de serviços acessam para exibir as propriedades de perfil para os usuários ou para fazer alterações na configuração. Uma seção de perfil é um objeto MAPI que implementa a interface **IProfSect** , uma interface derivada de **IMAPIProp** e não tem métodos adicionais. Para obter mais informações, consulte [IProfSect: IMAPIProp](iprofsectimapiprop.md). Sua única finalidade é manipular as propriedades de uma seção de perfil. Para recuperar um ponteiro **IProfSect** para uma seção de perfil específica, clientes e provedores de serviço chamam os seguintes métodos. 
  
|||
|:-----|:-----|
|Os clientes podem chamar:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Os provedores de serviços podem chamar:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Clientes ou provedores podem chamar:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Os perfis são organizados hierarquicamente como o MAPISVC. Arquivo INF. Na parte superior da hierarquia, há seções de perfil que contêm informações relevantes para o perfil. O nível intermediário inclui seções que contêm informações sobre um determinado serviço de mensagens e o nível inferior inclui seções que contêm informações sobre um dos provedores de serviço em um serviço de mensagens. 
  
Todos os perfis têm várias propriedades necessárias que são armazenadas em uma ou mais seções do perfil. Por exemplo, cada perfil tem as propriedades **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) e **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). A chave de pesquisa de um perfil é definida com o valor definido em MAPIGUID. H como MUID_PROFILE_INSTANCE e sempre é garantido como exclusivo entre todos os perfis. Embora dois perfis possam ter o mesmo nome, eles não podem ter a mesma chave de pesquisa. As chaves de pesquisa devem ser tratadas como dados binários em vez de dados de qualquer tipo específico.
  
Os provedores de repositórios de mensagens precisam incluir a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do repositório de mensagens nas seções de perfil para o perfil e para o seu provedor de repositório de mensagens e para manter essas entradas sincronizadas. Quando um repositório de mensagens é criado, o provedor define o **PR_DISPLAY_NAME** com base no valor armazenado nessas seções de perfil. 
  
Há duas diferenças importantes entre seções de perfil e outros objetos que herdam de **IMAPIProp**: 
  
- Seções de perfil não dão suporte a transações.
    
- Seções de perfil não dão suporte a propriedades nomeadas, retornando MAPI_E_NO_SUPPORT de suas implementações do **IMAPIProp:: GetIDsFromNames** e **IMAPIProp:: GetNamesFromIDs** . Para obter mais informações, consulte [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Como as seções de perfil não dão suporte a transações, as alterações feitas com as chamadas para **IMAPIProp:: CopyProps**, **CopyTo**ou SetProps serão efetivadas imediatamente. **** Para obter mais informações, consulte [IMAPIProp:: CopyProps](imapiprop-copyprops.md). Os clientes e provedores de serviço podem chamar o método **IMAPIProp:: SaveChanges** de uma seção de perfil e ele terá êxito, mas não afetará os dados da seção de perfil. Para obter mais informações, consulte [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). As alterações feitas imediatamente podem afetar como os provedores de serviços implementam as folhas de propriedades que os clientes usam para exibir propriedades de perfil para os usuários. Provedores de serviços que desejam que os usuários possam adiar ou desfazer alterações devem implementar suas folhas de propriedades com cópias de seções de perfil em vez das seções reais. Usando cópias, os usuários podem fazer alterações e cancelar mais tarde essas alterações, deixando as seções de perfil originais inalteradas. 
  
A ordem em que as informações aparecem em um perfil afeta como o MAPI configura recursos e faz atribuições em uma sessão. As seguintes atribuições são afetadas pela ordem do perfil:
  
- Repositório de mensagens padrão
    
- Catálogo de endereços pessoal
    
- Caminho de pesquisa do repositório de mensagens padrão
    
- Caminho de pesquisa do catálogo de endereços padrão
    
- Ordem do provedor de transporte
    
MAPI define o repositório de mensagens padrão como o primeiro repositório de mensagens no perfil que tem o sinalizador STATUS_DEFAULT_STORE definido em sua propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)), que indica que ele pode ser o repositório padrão. Os clientes podem substituir essa configuração chamando **IMAPISession:: SetDefaultStore**. Para obter mais informações, consulte [IMAPISession:: SetDefaultStore](imapisession-setdefaultstore.md).
  
O MAPI cria uma ordem de transporte para lidar com mensagens de saída e de entrada. Quando mais de um provedor de transporte for registrado para uma mensagem de um tipo específico, o MAPI usará essa ordem para determinar qual provedor deve lidar com a mensagem. MAPI define a ordem de transporte como a ordem na qual os provedores de transporte foram adicionados ao perfil com uma exceção – os transportes que definem o sinalizador STATUS_XP_PREFER_LAST em sua propriedade **PR_RESOURCE_FLAGS** são posicionados por último na ordem. Os clientes podem definir a ordem de transporte chamando **IMsgServiceAdmin:: MsgServiceTransportOrder**. Para obter mais informações, consulte [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Essas diretrizes para ordenar provedores de serviço e serviços de mensagens podem ocasionalmente entrar em conflito. Se houver um conflito, seu código deverá resolver o conflito. Você pode usar o programa do painel de controle de email para inspecionar um perfil que você criou para determinar se os provedores foram configurados conforme o esperado.
  

