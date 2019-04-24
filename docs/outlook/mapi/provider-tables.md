---
title: Tabelas de provedor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2b81f4aebae692d28ed492df102d59ba34debf63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328459"
---
# <a name="provider-tables"></a>Tabelas de provedor

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma tabela de provedor contém informações sobre provedores de serviços. Há duas tabelas de provedor diferentes, implementadas por MAPI e usadas por clientes. A primeira tabela, acessada chamando o método [IMsgServiceAdmin::](imsgserviceadmin-getprovidertable.md) getprovidertable, contém informações sobre todos os provedores para o perfil atual. A segunda tabela, acessada por meio de [IProviderAdmin::](iprovideradmin-getprovidertable.md)getprovidertable, cria uma tabela que armazena informações sobre todos os provedores de serviço de um serviço de mensagens.
  
Essas duas tabelas têm outra diferença. A tabela de provedor disponível através de **IMsgServiceAdmin::** getprovidertable contém apenas linhas que representam provedores de serviço enquanto a tabela disponível por meio do **IProviderAdmin::** getprovidertable pode incluir linhas que representam informações adicionais associadas a um provedor de serviços. Essas informações extras são adicionadas ao perfil com a palavra-chave "seções" de MAPISVC. INF. Quando um provedor tem seções de perfil extra, armazena os valores **MAPIUID** dessas seções na propriedade **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** é salvo na seção perfil de serviço de mensagens. 
  
As propriedades a seguir compõem o conjunto de colunas necessárias nos dois tipos de tabelas de provedor:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
A tabela do provedor pode ser usada para exibir a ordem de transporte atual ou para alterá-la. Para exibir a ordem atual, crie uma restrição para recuperar somente as linhas com a propriedade **PR_RESOURCE_TYPE** definida como MAPI_TRANSPORT_PROVIDER. Em seguida, use **PR_PROVIDER_ORDINAL** como uma chave de classificação para classificar a tabela e recuperar todas as linhas com o método IMAPITable [:: QueryRows](imapitable-queryrows.md) ou a função [HrQueryAllRows](hrqueryallrows.md) . 
  
Para alterar a ordem de transporte, aplique a mesma restrição e recupere as linhas. Em seguida, crie uma matriz de valores da propriedade **PR_PROVIDER_UID** que representa os identificadores exclusivos para os provedores de transporte. Quando os identificadores estiverem na ordem desejada, passe-os para o método [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) . 
  
Após a disponibilização de uma tabela de provedor, ela não refletirá as alterações subsequentes, como a adição ou a exclusão de um provedor.
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

