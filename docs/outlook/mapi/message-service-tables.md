---
title: Tabelas de serviço de mensagens
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422492"
---
# <a name="message-service-tables"></a>Tabelas de serviço de mensagens

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela de serviço de mensagens contém informações sobre os serviços de mensagens no perfil atual. Há uma tabela de serviço de mensagens para cada sessão MAPI, implementada por MAPI e usada por aplicativos clientes de propósito especial que oferecem suporte à configuração. 
  
A tabela de serviço de mensagens é uma tabela estática.
  
Os clientes acessam a tabela de serviço de mensagens chamando o método [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) . 
  
As propriedades a seguir compõem o conjunto de colunas necessárias na tabela de serviço de mensagens:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** é o nome de exibição para o serviço de mensagem e a coluna de chave de classificação padrão. 
  
 **PR_INSTANCE_KEY** serve como a coluna de índice para a tabela, identificando exclusivamente uma linha. 
  
 **PR_RESOURCE_FLAGS** descreve os recursos do serviço de mensagens. 
  
 **PR_SERVICE_DLL_NAME** é o nome da dll que contém a implementação do serviço de mensagens. 
  
 **PR_SERVICE_ENTRY_NAME** é o nome da função de ponto de entrada do serviço de mensagens que está de acordo com o protótipo do [MSGSERVICEENTRY](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** é uma entrada necessária na seção **[serviços]** no MAPISVC. inf. O valor dessa propriedade nunca será alterado ou localizado. O **PR_SERVICE_NAME** pode ser usado para identificar programaticamente o serviço de mensagens. 
  
 **PR_SERVICE_SUPPORT_FILES** é uma lista de arquivos que devem ser instalados com o serviço de mensagens. 
  
 **PR_SERVICE_UID** é um identificador exclusivo para o serviço de mensagens. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

