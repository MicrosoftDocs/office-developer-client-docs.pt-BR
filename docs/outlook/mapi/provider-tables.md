---
title: Tabelas de provedores
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 99709a4c-cb52-436e-a322-02ded5d65ce5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a613bd744a113b4378c5bef94fb51f6ae3aa4041
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770199"
---
# <a name="provider-tables"></a>Tabelas de provedores

  
  
**Aplica-se a**: Outlook 
  
Uma tabela de provedor contém informações sobre provedores de serviços. Há duas tabelas do provedor diferente, ambos implementadas pelo MAPI e usado pelos clientes. A primeira tabela acessada chamando o método [IMsgServiceAdmin::GetProviderTable](imsgserviceadmin-getprovidertable.md) , mantém informações sobre todos os provedores para o perfil atual. A segunda tabela, acessada por meio de [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), cria uma tabela que armazena informações sobre todos os provedores de serviço para um serviço de mensagem.
  
Nestas duas tabelas têm outra diferença. A tabela de provedor disponível por meio de **IMsgServiceAdmin::GetProviderTable** contém somente as linhas que representam os provedores de serviço, enquanto a tabela disponível por meio de **IProviderAdmin::GetProviderTable** pode incluir linhas que representam informações adicionais associadas a um provedor de serviços. Essas informações extras são adicionadas ao perfil com a palavra-chave "Seções" de Mapisvc. Quando um provedor tem seções extras de perfil, ele armazena os valores **MAPIUID** para estas seções na propriedade **PR_SERVICE_EXTRA_UIDS** ([PidTagServiceExtraUids](pidtagserviceextrauids-canonical-property.md)). **PR_SERVICE_EXTRA_UIDS** é salvo na seção de perfil de serviço de mensagem. 
  
As seguintes propriedades compõem a coluna necessária definida em ambos os tipos de tabelas de provedor:
  
|||
|:-----|:-----|
|**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_PROVIDER_ORDINAL** ([PidTagProviderOrdinal](pidtagproviderordinal-canonical-property.md))  <br/> |**PR_PROVIDER_UID** ([PidTagProviderUid](pidtagprovideruid-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
|**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
A tabela de provedor pode ser usada para exibir a ordem de transporte atual ou para alterá-lo. Para exibir a ordem atual, crie uma restrição para recuperar apenas aquelas linhas com a propriedade **PR_RESOURCE_TYPE** definida como MAPI_TRANSPORT_PROVIDER. Use **PR_PROVIDER_ORDINAL** como uma chave de classificação para classificar a tabela e recuperar todas as linhas com o método [IMAPITable:: QueryRows](imapitable-queryrows.md) ou a função [HrQueryAllRows](hrqueryallrows.md) . 
  
Para alterar a ordem de transporte, aplicar a mesma restrição e recuperar as linhas. Em seguida, crie uma matriz de valores da propriedade **PR_PROVIDER_UID** que representa os identificadores exclusivos para os provedores de transporte. Quando os identificadores estiverem na ordem desejada, envie-os para o método [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md) . 
  
Depois que uma tabela de provedor foi disponibilizada, ele não refletirá as alterações subsequentes, como a adição ou exclusão de um provedor.
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

