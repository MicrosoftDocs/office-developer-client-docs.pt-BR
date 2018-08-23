---
title: Recuperar identidade principal e do provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: da11cf684c4bdcfb94d33791ed7c61d2e322e1a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586582"
---
# <a name="retrieving-primary-and-provider-identity"></a>Recuperar identidade principal e do provedor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de serviços, geralmente provedores de catálogo de endereços, tem a opção de fornecer uma identidade que pode ser usada para representar a sessão em uma variedade de situações. Três propriedades descrevem a identidade de um provedor:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Essas propriedades são definidas para o identificador de entrada, nome para exibição e a chave de pesquisa do objeto identidade correspondente, que normalmente é um usuário de mensagens. Provedores de forneçam de uma identidade também definir o sinalizador STATUS_PRIMARY_IDENTITY em suas propriedades **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
Dependendo das suas necessidades, você pode usar a identidade de um determinado provedor ou a identidade principal para a sessão. Você pode usar a identidade de um provedor também para fins de exibição ou para recuperar as propriedades, como **PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, se definida, que contém o caminho para arquivos usados ou criado pelo provedor. Recupere a propriedade **PR_RESOURCE_PATH** para o provedor fornecendo a identidade principal quando você deseja localizar os arquivos que pertencem ao usuário da sessão. 
  
 **Para recuperar a identidade de um provedor específico**
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status. 
    
2. Construa uma restrição usando uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder à coluna **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) com o nome do provedor especificado. 
    
3. Chame [IMAPITable:: FindRow](imapitable-findrow.md) para localizar linha do provedor. Identidade do provedor será armazenada na coluna **PR_IDENTITY_ENTRYID** , se ela existir. 
    
 **Para recuperar a identidade principal para uma sessão**
  
- Chame [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** baseia a identidade de sessão na existência do valor STATUS_PRIMARY_IDENTITY na coluna **PR_RESOURCE_FLAGS** para uma das linhas da tabela de status. Se nenhuma das linhas de status tiver esse valor definido, **QueryIdentity** atribui a identidade para o primeiro provedor de serviços que define as propriedades PR_IDENTITY três. Se nenhum provedor de serviço fornece uma identidade, **QueryIdentity** retorna MAPI_W_NO_SERVICE. Quando isso acontece, você deverá criar uma cadeia de caracteres para representar um usuário genérico que pode servir como a identidade principal. 
    
 **Para definir explicitamente a identidade principal para uma sessão**
  
- Chame [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Passe o **MAPIUID** para o provedor de serviço de destino. 
    

