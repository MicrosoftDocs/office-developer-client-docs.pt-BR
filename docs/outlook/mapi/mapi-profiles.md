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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25391427"
---
# <a name="mapi-profiles"></a>Perfis MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um perfil armazena informações sobre provedores de serviço e serviços de mensagem que estão instalados em um computador. Para cada sessão, um cliente na hora do logon seleciona um único perfil que descreve os provedores e serviços a serem usados. Um cliente pode escolher entre uma coleção de perfis e, se desejado, estabeleça uma como padrão. O perfil padrão será o que é selecionada automaticamente quando um cliente inicia uma sessão e não tiver especificado explicitamente um perfil.
  
Também nestes tópicos, você encontrará uma discussão sobre o cache de apelidos, que é armazenado em um stream binário.
  
- [Cache de apelidos](nickname-cache.md)
    
- [Fluxo de preenchimento automático](autocomplete-stream.md)
    
- [Análise de arquivo binário](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Seções de perfil

Perfis são divididos em seções que clientes e provedores de serviços de acesso para exibir propriedades de perfil para os usuários ou fazer alterações na configuração. Uma seção de perfil é um objeto MAPI que implementa a interface **IProfSect** , uma interface que derive da **IMAPIProp** e não tem nenhuma métodos adicionais. Para obter mais informações, consulte [IProfSect: IMAPIProp](iprofsectimapiprop.md). Sua única finalidade é manipular as propriedades de uma seção de perfil. Para recuperar um ponteiro **IProfSect** a uma seção de perfil específico, clientes e provedores de serviços chame os métodos a seguir. 
  
|||
|:-----|:-----|
|Clientes podem chamar:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Provedores de serviços podem chamar:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Clientes ou provedores podem chamar:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Os perfis são organizados hierarquicamente muito semelhante a MAPISVC. Arquivo INF. Na parte superior da hierarquia, há seções de perfil que contêm informações relevantes para o perfil. O nível intermediário inclui seções que contêm informações sobre um serviço de mensagem específica e o nível inferior inclui seções que contêm informações sobre um dos provedores de serviço em um serviço de mensagem. 
  
Cada perfil tem várias propriedades necessárias que são armazenadas em um ou mais das seções do perfil. Por exemplo, cada perfil tem as propriedades de **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) e o **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)). Chave de pesquisa de um perfil é definido como o valor definido em MAPIGUID. H como MUID_PROFILE_INSTANCE e sempre é garantido que ser exclusivo entre todos os perfis. Embora os dois perfis podem ter o mesmo nome, eles não podem ter a mesma chave de pesquisa. Chaves de pesquisa devem ser tratadas como dados binários em vez de dados de qualquer tipo específico.
  
Provedores de armazenamento de mensagem são necessários para incluir propriedade de **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) do seu armazenamento de mensagens nas seções perfil para o perfil e para sua mensagem de provedor de armazenamento e manter essas entradas sincronizadas. Quando um armazenamento de mensagens é criado, o provedor define **PR_DISPLAY_NAME** com base no valor armazenado nestas seções de perfil. 
  
Há dois principais diferenças entre as seções de perfil e outros objetos que herdam **IMAPIProp**: 
  
- As seções de perfil não suportam transações.
    
- As seções de perfil não dão suporte a propriedades nomeadas, retornando MAPI_E_NO_SUPPORT de suas implementações **IMAPIProp::GetIDsFromNames** e **IMAPIProp::GetNamesFromIDs** . Para obter mais informações, consulte [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) e [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Porque as seções de perfil não suportam transações, quaisquer alterações feitas nas chamadas para **IMAPIProp::CopyProps**, **CopyTo**ou **SetProps** imediatamente entrarão em vigor. Para obter mais informações, consulte [IMAPIProp::CopyProps](imapiprop-copyprops.md). Clientes e provedores de serviços podem chamar o método de **IMAPIProp::SaveChanges** de uma seção perfil e ele será bem-sucedida, mas não afeta os dados da seção de perfil. Para obter mais informações, consulte [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Ter alterações ocorrem imediatamente pode afetar como provedores de serviços de implementam as folhas de propriedades que são usadas pelos clientes para exibir propriedades de perfil para os usuários. Provedores de serviços que deseja que os usuários sejam capazes de adiamento ou desfazer alterações devem implementar suas folhas de propriedades com cópias das seções de perfil, em vez das seções reais. Usando cópias, os usuários podem fazer alterações e, em seguida, mais tarde Cancelar essas alterações, deixando inalterada as seções de perfil original. 
  
A ordem na qual informações aparecem em um perfil afeta como MAPI configura recursos e faz as atribuições em uma sessão. As atribuições a seguir são afetadas por ordem de perfil:
  
- Armazenamento de mensagens padrão
    
- Catálogo particular de endereços
    
- Caminho de pesquisa do repositório de mensagem padrão
    
- Padrão de caminho de pesquisa do catálogo de endereços
    
- Ordem de provedor de transporte
    
MAPI define o armazenamento de mensagens padrão a ser o primeiro armazenamento de mensagens no perfil que tem o sinalizador STATUS_DEFAULT_STORE definido em sua propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)), que indica que ele pode ser o repositório padrão. Clientes podem substituir essa configuração chamando **IMAPISession::SetDefaultStore**. Para obter mais informações, consulte [IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI cria uma ordem de transporte para lidar com as mensagens de entrada e saídas. Quando mais de um provedor de transporte foi registrado para uma mensagem de um determinado tipo, o MAPI usa nesta ordem para determinar qual provedor deve lidar com a mensagem. MAPI define a ordem de transporte a ser a ordem na qual o transporte provedores foram adicionados ao perfil com uma exceção – os transportes que defina o sinalizador STATUS_XP_PREFER_LAST em suas propriedades **PR_RESOURCE_FLAGS** posicionados última na ordem. Os clientes podem definir a ordem de transporte chamando **IMsgServiceAdmin::MsgServiceTransportOrder**. Para obter mais informações, consulte [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Estas diretrizes para pedidos de provedores de serviço e serviços de mensagem em alguns casos, podem entrar em conflito. Se houver um conflito, seu código deve resolver o conflito. Você pode usar o programa do painel de controle de email para inspecionar um perfil que você criou para determinar se os provedores foram configurados conforme o esperado.
  

