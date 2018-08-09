---
title: Tabelas de serviços de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 81772115fcd4f081718dd560759f6ab93dc7c11c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768144"
---
# <a name="message-service-tables"></a>Tabelas de serviços de mensagens

  
  
**Aplica-se a**: Outlook 
  
A tabela de serviço de mensagem contém informações sobre os serviços de mensagem no perfil atual. Há uma tabela de serviço de mensagem para cada sessão MAPI, implementada por MAPI e usado pelos aplicativos de cliente para fins especiais que oferecem suporte à configuração. 
  
A tabela de serviço de mensagem é uma tabela estática.
  
Os clientes de acessar a tabela de serviços de mensagem chamando o método [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) . 
  
As seguintes propriedades compõem a coluna necessária definida na tabela de serviço de mensagem:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** é o nome para exibição para o serviço de mensagem e a coluna de chaves de classificação padrão. 
  
 **PR_INSTANCE_KEY** serve como a coluna de índice para a tabela, que identifica unicamente uma linha. 
  
 **PR_RESOURCE_FLAGS** descreve os recursos do serviço de mensagem. 
  
 **PR_SERVICE_DLL_NAME** é o nome da DLL que contém a implementação do serviço de mensagem. 
  
 **PR_SERVICE_ENTRY_NAME** é o nome da função de ponto de entrada do serviço de mensagem que está em conformidade com o protótipo [MSGSERVICEENTRY](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** é uma entrada necessária na seção **[Services]** em MAPISVC. O valor dessa propriedade nunca será alterado ou localizado. **PR_SERVICE_NAME** pode ser usado para identificar programaticamente o serviço de mensagem. 
  
 **PR_SERVICE_SUPPORT_FILES** é uma lista dos arquivos que devem ser instalados com o serviço de mensagem. 
  
 **PR_SERVICE_UID** é um identificador exclusivo para o serviço de mensagem. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

