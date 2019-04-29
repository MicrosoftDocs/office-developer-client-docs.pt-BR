---
title: IMAPIStatus IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus
api_type:
- COM
ms.assetid: 17b2aa43-0267-45b6-8c57-11b7a5c67333
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f90cf661c069ecd476bd02c5719147633a8392e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408296"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus : IMAPIProp

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece informações de status sobre o subsistema MAPI, o catálogo de endereços integrado e o spooler MAPI. Um provedor de serviços implementa o **IMAPIStatus** para fornecer informações sobre seu próprio status. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Exposto por:  <br/> |Objetos de status  <br/> |
|Implementado por:  <br/> |Provedores de serviços e MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIStatus  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPISTATUS  <br/> |
|Modelo de transação:  <br/> |Não-Transacted  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Confirma as informações de status externas disponíveis para o recurso MAPI ou provedor de serviços.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Exibe uma folha de propriedades que permite que o usuário altere a configuração de um provedor de serviços.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Modifica a senha de um provedor de serviços sem exibir uma interface de usuário.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Força todas as mensagens aguardando para serem enviadas ou recebidas para serem carregadas ou baixadas imediatamente.  <br/> |
   
|**Propriedades necessárias**|**Acesso**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Comentários

Os objetos de status que o MAPI implementa suporta os seguintes métodos:
  
|**Objeto status**|**Métodos com suporte**|
|:-----|:-----|
|Subsistema MAPI  <br/> |**ValidateState** somente  <br/> |
|Catálogo de endereços MAPI  <br/> |**ValidateState** somente  <br/> |
|Spooler MAPI  <br/> |**ValidateState** e **FlushQueues** <br/> |
   
Os objetos de status que o MAPI implementa precisam ter uma versão somente leitura dos métodos da interface [IMAPIProp](imapipropiunknown.md) e para dar suporte ao método **ValidateState** . Os provedores de transporte também devem oferecer suporte a **FlushQueues**. Todos os provedores devem suportar o **SettingsDialog**; o suporte para **ChangePassword** é opcional. 
  
Os clientes usam objetos de status para executar a configuração e para saber mais sobre o estado da sessão. Eles acessam um objeto status chamando o método **OpenStatusEntry** de um objeto de logon do provedor de serviços ou o método [IMAPISession::](imapisession-getstatustable.md) getstatustable para recuperar o objeto status. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

