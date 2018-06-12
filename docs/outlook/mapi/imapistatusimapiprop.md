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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e36a987174ffb2abb4c0f5fc95bf695f31af942e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767211"
---
# <a name="imapistatus--imapiprop"></a>IMAPIStatus: IMAPIProp

  
  
**Aplica-se a**: Outlook 
  
Fornece informações de status sobre o MAPI spooler, o catálogo de endereços integrada e o subsistema de MAPI. Um provedor de serviços implementa **IMAPIStatus** para fornecer informações sobre seu próprio status. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Expostos pelo:  <br/> |Objetos de status  <br/> |
|Implementada por:  <br/> |Provedores de serviços e MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIStatus  <br/> |
|Tipo de ponteiro:  <br/> |LPMAPISTATUS  <br/> |
|Modelo de transação:  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[ValidateState](imapistatus-validatestate.md) <br/> |Confirma as informações de status externos disponíveis para o recurso MAPI ou o provedor de serviço.  <br/> |
|[SettingsDialog](imapistatus-settingsdialog.md) <br/> |Exibe uma folha de propriedades que permite ao usuário alterar a configuração de um provedor de serviços.  <br/> |
|[ChangePassword](imapistatus-changepassword.md) <br/> |Modifica a senha de um provedor de serviços sem exibir uma interface do usuário.  <br/> |
|[FlushQueues](imapistatus-flushqueues.md) <br/> |Força todas as mensagens aguardando para ser enviado ou recebido para ser carregadas ou baixadas imediatamente.  <br/> |
   
|**Propriedades necessárias**|**Access**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))  <br/> |Leitura/gravação  <br/> |
|**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |Somente leitura  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |Somente leitura  <br/> |
   
## <a name="remarks"></a>Coment�rios

Os objetos de status que implementa MAPI suportam os seguintes métodos:
  
|**Objeto de status**|**Métodos com suporte**|
|:-----|:-----|
|Subsistema MAPI  <br/> |**ValidateState** apenas  <br/> |
|Catálogo de endereços MAPI  <br/> |**ValidateState** apenas  <br/> |
|Spooler MAPI  <br/> |**ValidateState** e **FlushQueues** <br/> |
   
Os objetos de status que implementa MAPI são necessários para ter uma versão somente leitura dos métodos da interface [IMAPIProp](imapipropiunknown.md) e suporte ao método **ValidateState** . Provedores de transporte também devem oferecer suporte a **FlushQueues**. Todos os provedores devem oferecer suporte a **SettingsDialog**; o suporte para **ChangePassword** é opcional. 
  
Clientes usam objetos de status para executar a configuração e para saber mais sobre o estado da sessão. Eles acessar um objeto de status chamando o método **OpenStatusEntry** de um objeto de logon do provedor de serviço ou o método [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para recuperar o objeto de status. 
  
## <a name="see-also"></a>Confira também



[Interfaces MAPI](mapi-interfaces.md)

