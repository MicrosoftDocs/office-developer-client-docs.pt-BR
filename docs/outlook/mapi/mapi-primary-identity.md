---
title: Identidade primária de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bd6fe1298a38733cb9d4916a931138c616e110bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767908"
---
# <a name="mapi-primary-identity"></a>Identidade primária de MAPI

  
  
**Aplica-se a**: Outlook 
  
A maioria das sessões MAPI tem um provedor de serviço específico que fornece a identidade principal para a sessão. Normalmente, ele é um provedor de catálogo de endereços, que fornece a identidade por meio de uma de suas mensagens de objetos de usuário ou listas de distribuição. Na verdade, MAPI recomenda que os serviços de mensagem que inclui um provedor de catálogo de endereços usam um dos seus objetos referente à identidade do principal. Quando um provedor de serviços que pertence a um serviço de mensagem fornece a identidade principal, todos os outros provedores de serviço no serviço de mensagem compartilham essa identidade.
  
O MAPISVC. Arquivo de configuração INF possui entradas relacionadas à identidade no nível do provedor de serviço e serviço de mensagem. Seções do serviço de mensagem devem incluir uma entrada que afirma que se ou não o serviço pode fornecer a identidade principal; seções do provedor de serviço incluem uma entrada semelhante somente quando o provedor pode fornecer uma identidade.
  
A tabela a seguir lista as entradas que aparecem no serviço de mensagem e seções de provedor de serviço no MAPISVC. Arquivo INF.
  
|**Fornecedor de identidade primária**|**Configuração de PR_RESOURCE_FLAGS**|
|:-----|:-----|
|Serviço de mensagem  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Não, o serviço de mensagem  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Provedor de serviços  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Embora vários serviços de mensagem podem declarar a capacidade de fornecer a identidade de uma sessão principal, o serviço de apenas uma mensagem é selecionado para fazê-lo. Esta seleção pode ocorrer:
  
- Quando um perfil é criado.
    
- Quando um cliente chama **IMsgServiceAdmin::SetPrimaryIdentity** para estabelecer explicitamente um serviço de mensagem específica como um provedor de identidade a sessão. Para obter mais informações. Consulte [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Quando um perfil é criado, MAPI designa o primeiro serviço de mensagem a ser configurado que inclui um provedor com o sinalizador STATUS_PRIMARY_IDENTITY definido em sua propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) para fornecer a identidade principal . Dentro do serviço de mensagem designados, o primeiro provedor a ser configurado com esse sinalizador definido de recursos é escolhido para fornecer a identidade do serviço. O sinalizador STATUS_PRIMARY_IDENTITY está desmarcado para todos os outros provedores no serviço de designada e outros serviços de mensagem no perfil. Se a qualquer momento, o provedor fornecendo identidade primária for removido do perfil, MAPI atribui a função que pode fornecer a identidade para o próximo provedor a ser configurado. Isso é determinado pela aparência do `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` entrada na seção do provedor em MAPISVC. 
  
Quando um cliente chama o método de **IMsgServiceAdmin::SetPrimaryIdentity** do serviço de uma mensagem, ela especifica a MAPIUID para um provedor de serviço dentro do serviço de destino. Para obter mais informações, consulte [MAPIUID](mapiuid.md). O provedor de serviço representado pelo **MAPIUID** é atribuído ao fornecer a identidade principal para o serviço de mensagem e para a sessão e todos os outros provedores no serviço compartilharão essa identidade. 
  
Cada provedor no serviço de mensagem responsável por fornecer a identidade principal atualiza sua linha da tabela de status para incluir as propriedades a seguir.
  
|**Propriedade identity principal**|**Definida como**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nome para exibição do objeto fornecendo a identidade principal.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Chave de pesquisa para o objeto fornecendo a identidade principal.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificador de entrada para o objeto fornecendo a identidade principal.  <br/> |
   
 **Para recuperar o identificador de entrada para o objeto fornecendo a identidade principal**
  
- Chame o método **IMAPISession::QueryIdentity** . Para obter mais informações, consulte [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** procura na tabela de status para a linha que contém o valor STATUS_PRIMARY_IDENTITY em uma coluna **PR_RESOURCE_FLAGS** e retorna o correspondente **PR_IDENTITY_ENTRYID** como o identificador de entrada para o principal identidade. 
    

