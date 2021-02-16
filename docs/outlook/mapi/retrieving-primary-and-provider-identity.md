---
title: Recuperando a identidade principal e do provedor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d81bb81d-1708-4a8d-a4d5-c3ba087db9b7
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f59695eca2af71dd592c5b3a755d021ac53b3e31
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430809"
---
# <a name="retrieving-primary-and-provider-identity"></a>Recuperando a identidade principal e do provedor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Provedores de serviços, normalmente provedores de agendamento de endereços, têm a opção de fornecer uma identidade que pode ser usada para representar a sessão em uma variedade de situações. Três propriedades descrevem a identidade de um provedor:
  
- **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) 
    
- **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)) 
    
- **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) 
    
Essas propriedades são definidas para o identificador de entrada, o nome de exibição e a chave de pesquisa do objeto de identidade correspondente, que normalmente é um usuário de mensagens. Os provedores que fornecem uma identidade também configuram o sinalizador STATUS_PRIMARY_IDENTITY na propriedade **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)).
  
Dependendo das suas necessidades, você pode usar a identidade de um provedor específico ou a identidade principal da sessão. Você pode usar a identidade de um provedor também para fins de exibição ou para recuperar propriedades, **como PR_RESOURCE_PATH** ([PidTagResourcePath](pidtagresourcepath-canonical-property.md)). **PR_RESOURCE_PATH**, se definido, contém o caminho para arquivos usados ou criados pelo provedor. Recupere a **PR_RESOURCE_PATH** para o provedor que fornece a identidade principal quando você deseja localizar arquivos pertencentes ao usuário da sessão. 
  
 **Para recuperar a identidade de um provedor específico**
  
1. Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status. 
    
2. Crie uma restrição usando uma estrutura [SPropertyRestriction](spropertyrestriction.md) para corresponder à coluna **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)) com o nome do provedor especificado. 
    
3. Chame [IMAPITable::FindRow](imapitable-findrow.md) para localizar a linha do provedor. A identidade do provedor será armazenada na coluna **PR_IDENTITY_ENTRYID,** se existir. 
    
 **Para recuperar a identidade principal de uma sessão**
  
- Chame [IMAPISession::QueryIdentity](imapisession-queryidentity.md). **QueryIdentity** baseia a identidade da sessão na existência do STATUS_PRIMARY_IDENTITY valor na coluna **PR_RESOURCE_FLAGS** para uma das linhas na tabela de status. Se nenhuma das linhas de status tiver esse valor definido, **QueryIdentity** atribuirá identidade ao primeiro provedor de serviços que define as três PR_IDENTITY propriedades. Se nenhum provedor de serviços fornece uma identidade, **QueryIdentity retorna** MAPI_W_NO_SERVICE. Quando isso acontece, você deve criar uma cadeia de caracteres para representar um usuário genérico que pode servir como a identidade principal. 
    
 **Para definir explicitamente a identidade principal de uma sessão**
  
- Chame [IMsgServiceAdmin::SetPrimaryIdentity](imsgserviceadmin-setprimaryidentity.md). Passe o **MAPIUID para** o provedor de serviços de destino. 
    

