---
title: Identidade Principal MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5bf88de280b012c54d4caaac6bdfe877f476ac37
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404719"
---
# <a name="mapi-primary-identity"></a>Identidade Principal MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A maioria das sessões MAPI tem um provedor de serviços específico que fornece a identidade principal para a sessão. Normalmente, é um provedor de agendamento de endereços, que fornece identidade por meio de um de seus objetos de usuário de mensagens ou listas de distribuição. Na verdade, o MAPI recomenda que os serviços de mensagens que incluem um provedor de agendamento de endereço usem um de seus objetos para a identidade principal. Quando um provedor de serviços que pertence a um serviço de mensagens fornece a identidade principal, todos os outros provedores de serviços no serviço de mensagens compartilham essa identidade.
  
O MAPISVC. O arquivo de configuração INF tem entradas relacionadas à identidade no nível do serviço de mensagens e do provedor de serviços. As seções do serviço de mensagens devem incluir uma entrada informando se o serviço pode ou não fornecer a identidade principal; as seções do provedor de serviços incluem uma entrada semelhante somente quando o provedor pode fornecer uma identidade.
  
A tabela a seguir lista as entradas que aparecem nas seções do serviço de mensagens e do provedor de serviços no MAPISVC. Arquivo INF.
  
|**Fornecedor de identidade principal**|**PR_RESOURCE_FLAGS configuração**|
|:-----|:-----|
|Serviço de mensagens  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Não é o serviço de mensagens  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Provedor de serviços  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Embora vários serviços de mensagens possam declarar sua capacidade de fornecer a identidade principal de uma sessão, apenas um serviço de mensagens é selecionado para fazer isso. Essa seleção pode ocorrer:
  
- Quando um perfil é criado.
    
- Quando um cliente chama **IMsgServiceAdmin::SetPrimaryIdentity** para estabelecer explicitamente um determinado serviço de mensagens como o provedor da identidade da sessão. Para obter mais informações. Consulte [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Quando um perfil é criado, o MAPI designa o primeiro serviço de mensagem a ser configurado que inclui um provedor com o sinalizador STATUS_PRIMARY_IDENTITY definido em sua propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) para fornecer a identidade principal. Dentro do serviço de mensagens designado, o primeiro provedor a ser configurado com esse conjunto de sinalizadores de recurso é escolhido para fornecer a identidade do serviço. O STATUS_PRIMARY_IDENTITY sinalizador é limpo para todos os outros provedores no serviço designado e outros serviços de mensagem no perfil. Se, a qualquer momento, o provedor que fornece a identidade primária for removido do perfil, o MAPI atribuirá a função ao próximo provedor a ser configurado e poderá fornecer a identidade. Isso é determinado pela aparência da  `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` entrada na seção do provedor em MAPISVC.INF. 
  
Quando um cliente chama o método **IMsgServiceAdmin::SetPrimaryIdentity** de um serviço de mensagens, ele especifica o MAPIUID para um provedor de serviços dentro do serviço de destino. Para obter mais informações, consulte [MAPIUID](mapiuid.md). O provedor de serviços representado pelo **MAPIUID** é atribuído para fornecer a identidade principal para o serviço de mensagens e para a sessão, e todos os outros provedores no serviço compartilharão essa identidade. 
  
Cada provedor no serviço de mensagens responsável por fornecer a identidade principal atualiza sua linha na tabela de status para incluir as propriedades a seguir.
  
|**Propriedade de identidade principal**|**Definida como**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nome de exibição do objeto que fornece a identidade principal.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Chave de pesquisa para o objeto que fornece a identidade principal.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificador de entrada do objeto que fornece a identidade principal.  <br/> |
   
 **Para recuperar o identificador de entrada do objeto que fornece a identidade principal**
  
- Chame o **método IMAPISession::QueryIdentity.** Para obter mais informações, [consulte IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** pesquisa na tabela de status a linha que contém o valor STATUS_PRIMARY_IDENTITY em sua coluna PR_RESOURCE_FLAGS e retorna o **PR_IDENTITY_ENTRYID** correspondente como o identificador de entrada para **a** identidade principal. 
    

