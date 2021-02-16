---
title: Tabelas do provedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408968"
---
# <a name="provider-tables"></a>Tabelas do provedor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de provedor contém informações sobre provedores de serviços. Há duas tabelas de provedores diferentes, ambas implementadas pelo MAPI e usadas por clientes. A primeira tabela, acessada chamando o método [IMsgServiceAdmin::GetProviderTable,](imsgserviceadmin-getprovidertable.md) contém informações sobre todos os provedores do perfil atual. A segunda tabela, acessada por [meio de IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), cria uma tabela que armazena informações sobre todos os provedores de serviços para um serviço de mensagens.
  
Essas duas tabelas têm outra diferença. A tabela do provedor disponível por meio de **IMsgServiceAdmin::GetProviderTable** contém apenas linhas que representam provedores de serviços enquanto a tabela disponível por meio de **IProviderAdmin::GetProviderTable** pode incluir linhas que representam informações adicionais associadas a um provedor de serviços. Essas informações extras são adicionadas ao perfil com a palavra-chave "Sections" de MAPISVC.INF. Quando um provedor tem seções de perfil extras, ele armazena os valores **MAPIUID** para essas seções na propriedade **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** é salvo na seção de perfil de serviço de mensagens. 
  
As propriedades a seguir compom o conjunto de colunas necessário em ambos os tipos de tabelas de provedor:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
A tabela do provedor pode ser usada para exibir a ordem de transporte atual ou alterá-la. Para exibir a ordem atual, crie uma restrição para recuperar somente as linhas com a propriedade **PR_RESOURCE_TYPE** definida como MAPI_TRANSPORT_PROVIDER. Em **seguida, PR_PROVIDER_ORDINAL** como uma chave de classificação para classificar a tabela e recuperar todas as linhas com o método [IMAPITable::QueryRows](imapitable-queryrows.md) ou a função [HrQueryAllRows.](hrqueryallrows.md) 
  
Para alterar a ordem de transporte, aplique a mesma restrição e recupere as linhas. Em seguida, crie uma matriz de valores **PR_PROVIDER_UID** propriedade que representa os identificadores exclusivos para os provedores de transporte. Quando os identificadores estão na ordem desejada, passe-os para o [método IMsgServiceAdmin::MsgServiceTransportOrder.](imsgserviceadmin-msgservicetransportorder.md) 
  
Depois que uma tabela de provedor tiver sido disponibilizada, ela não refletirá alterações subsequentes, como a adição ou exclusão de um provedor.
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

