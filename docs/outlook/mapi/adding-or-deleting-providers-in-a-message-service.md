---
title: Adicionar ou excluir provedores em um serviço de mensagens
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329558"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Adicionar ou excluir provedores em um serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para adicionar ou excluir provedores de serviço em um serviço de mensagens, use a interface [IProviderAdmin: IUnknown](iprovideradminiunknown.md) . Você pode recuperar um ponteiro do **IProviderAdmin** chamando [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md). A tabela do provedor, acessada por meio de [IProviderAdmin::](iprovideradmin-getprovidertable.md)getprovidertable, lista informações sobre os provedores de serviço atualmente instalados no serviço de mensagens. Os clientes e provedores de serviços podem usar a tabela do provedor para acessar o nome do arquivo DLL do provedor, por exemplo, ou o **MAPIUID**, o nome para exibição e o tipo do provedor, bem como as informações sobre o serviço de mensagens. Para obter mais informações, consulte [tabelas do provedor](provider-tables.md).
  
 **Para adicionar ou excluir um provedor de serviços em um serviço de mensagens**
  
1. Chame o **** método adminservices para acessar um objeto de administração de serviço de mensagens. 
    
2. Chame [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) para acessar a tabela de serviço de mensagens. 
    
3. Criar uma restrição de propriedade usando uma estrutura [SPropertyRestriction](spropertyrestriction.md) que corresponda a **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) com o nome do serviço de mensagens a ser adapta. 
    
4. Chame o método imApitable [:: FindRow](imapitable-findrow.md) da tabela de serviço de mensagens para localizar a linha na tabela que representa o serviço de mensagem de destino. 
    
5. Chame [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) para recuperar um ponteiro do **IProviderAdmin** . Passe a coluna **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha da tabela do serviço de mensagens como o parâmetro _lpUID_ . 
    
6. Chame [IProviderAdmin::](iprovideradmin-getprovidertable.md) getprovidertable para acessar a tabela de provedor. 
    
7. Criar uma restrição de propriedade usando uma estrutura SPropertyRestriction que corresponda a **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) com o nome do provedor de serviços a ser adicionado ou excluído. 
    
8. Chame o método imApitable [:: FindRow](imapitable-findrow.md) da tabela do provedor para localizar a linha na tabela que representa o provedor de serviço de destino. 
    
9. Chame [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md) para adicionar o provedor ou [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md) para removê-lo do serviço de mensagens. Para o **CreateProvider**, passe a propriedade **PR_DISPLAY_NAME** do provedor como o parâmetro _lpszProvider_ . Para qualquer um dos métodos, passe a propriedade **PR_SERVICE_UID** do provedor como o parâmetro _lpUID_ . Após o provedor de serviços ter sido adicionado ou excluído, a alteração não será aparente até que uma nova sessão seja criada. 
    
Outra técnica para adicionar um provedor de serviços, especificamente um provedor de armazenamento de mensagens, a um perfil envolve a criação de um identificador de entrada para o provedor. Como construir um identificador de entrada exige conhecimento de seu formato, essa técnica só poderá ser usada se o provedor de serviços tiver feito seu formato de identificador de entrada público. 
  
Com o identificador de entrada recentemente construído, um cliente pode chamar [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md). O MAPI cria automaticamente uma seção de perfil no perfil para o provedor de serviços, mas não a adiciona a um serviço de mensagens. 
  
Alguns serviços de mensagens não permitem esse tipo de modificação dinâmica; Se é ou não compatível com o serviço de mensagens. Outro recurso que pode ou não ter suporte é a capacidade de acessar diretamente as seções de perfil particular de um serviço de mensagens. Se o serviço de mensagens que você está usando permitir esse acesso, ele publicará o **GUID** que representa a seção particular em MAPISVC. inf. Você pode passar este **GUID** em uma chamada para [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) para acessar a seção Profile. 
  

