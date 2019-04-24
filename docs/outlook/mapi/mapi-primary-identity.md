---
title: Identidade principal de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8787a873-6752-4b17-8ea3-8fed793e1371
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5bf88de280b012c54d4caaac6bdfe877f476ac37
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345791"
---
# <a name="mapi-primary-identity"></a>Identidade principal de MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A maioria das sessões MAPI tem um provedor de serviços específico que fornece a identidade principal da sessão. Normalmente, é um provedor de catálogo de endereços, que fornece a identidade por meio de um de seus objetos de usuário de mensagens ou listas de distribuição. Na verdade, a MAPI recomenda que os serviços de mensagens que incluem um provedor de catálogo de endereços usem um de seus objetos para a identidade principal. Quando um provedor de serviços que pertence a um serviço de mensagens fornece a identidade principal, todos os outros provedores de serviços no serviço de mensagens compartilham essa identidade.
  
O MAPISVC. O arquivo de configuração INF tem entradas relacionadas à identidade no nível do serviço de mensagens e do provedor de serviços. As seções do serviço de mensagens devem incluir uma entrada que indica se o serviço pode ou não fornecer a identidade principal; as seções do provedor de serviços incluem uma entrada semelhante somente quando o provedor pode fornecer uma identidade.
  
A tabela a seguir lista as entradas que aparecem nas seções serviço de mensagens e provedor de serviços no MAPISVC. Arquivo INF.
  
|**Fornecedor de identidade principal**|**Configuração PR_RESOURCE_FLAGS**|
|:-----|:-----|
|Serviço de mensagens  <br/> | `SERVICE_PRIMARY_IDENTITY` <br/> |
|Não é o serviço de mensagens  <br/> | `SERVICE_NO_PRIMARY_IDENTITY` <br/> |
|Provedor de serviços  <br/> | `STATUS_PRIMARY_IDENTITY` <br/> |
   
Embora vários serviços de mensagens possam declarar sua capacidade de fornecer uma identidade primária da sessão, apenas um serviço de mensagem é selecionado para fazê-lo. Essa seleção pode ocorrer:
  
- Quando um perfil é criado.
    
- Quando um cliente chama **IMsgServiceAdmin:: SetPrimaryIdentity** para estabelecer explicitamente um determinado serviço de mensagens como o provedor da identidade da sessão. Para obter mais informações. Consulte [IMsgServiceAdmin:: SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md).
    
Quando um perfil é criado, o MAPI designa o primeiro serviço de mensagens a ser configurado que inclui um provedor com o sinalizador STATUS_PRIMARY_IDENTITY definido em sua propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) para fornecer a identidade primária . Dentro do serviço de mensagens designado, o primeiro provedor a ser configurado com esse sinalizador de recurso definido é escolhido para fornecer a identidade para o serviço. O sinalizador STATUS_PRIMARY_IDENTITY está desativado para todos os outros provedores no serviço designado e outros serviços de mensagens no perfil. Se, a qualquer momento, o provedor de fornecimento da identidade principal for removido do perfil, o MAPI atribuirá à função o próximo provedor a ser configurado que possa fornecer a identidade. Isso é determinado pela aparência da `PR_RESOURCE_FLAGS=STATUS_PRIMARY_IDENTITY` entrada na seção do provedor em MAPISVC. inf. 
  
Quando um cliente chama o método **IMsgServiceAdmin:: SetPrimaryIdentity** do serviço de mensagens, ele especifica o MAPIUID para um provedor de serviços no serviço de destino. Para obter mais informações, consulte [MAPIUID](mapiuid.md). O provedor de serviços representado pelo **MAPIUID** é atribuído para fornecer a identidade principal para o serviço de mensagens e para a sessão, e todos os outros provedores no serviço compartilharão essa identidade. 
  
Cada provedor no serviço de mensagens responsável por fornecer a identidade principal atualiza sua linha na tabela de status para incluir as propriedades a seguir.
  
|**Propriedade Identity principal**|**Definida como**|
|:-----|:-----|
|**PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md))  <br/> |Nome para exibição do objeto que fornece a identidade principal.  <br/> |
|**PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md))  <br/> |Chave de pesquisa do objeto que fornece a identidade principal.  <br/> |
|**PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md))  <br/> |Identificador de entrada para o objeto que fornece a identidade principal.  <br/> |
   
 **Para recuperar o identificador de entrada para o objeto que fornece a identidade principal**
  
- Chame o método **IMAPISession:: QueryIdentity** . Para obter mais informações, consulte [IMAPISession:: QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** pesquisa a tabela de status da linha que contém o valor STATUS_PRIMARY_IDENTITY em sua coluna **PR_RESOURCE_FLAGS** e retorna o **PR_IDENTITY_ENTRYID** correspondente como o identificador de entrada para o primário ladrões. 
    

