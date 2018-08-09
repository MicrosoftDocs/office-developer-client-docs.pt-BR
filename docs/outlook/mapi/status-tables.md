---
title: Tabelas de status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: afbef333af46051284fa51d52c2e3f77607b0b13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770508"
---
# <a name="status-tables"></a>Tabelas de status

  
  
**Aplica-se a**: Outlook 
  
A tabela de status contém informações relacionadas para o estado da sessão atual. Há uma tabela de status para cada sessão MAPI que inclui informações fornecidas por MAPI e por provedores de serviços. MAPI fornece dados para três linhas: uma linha para o subsistema de MAPI, uma linha para o spooler MAPI e uma linha para o catálogo de endereços integrada. Porque os provedores de transporte são necessários para fornecer informações de status à tabela de status, há uma linha para cada provedor de transporte ativa. Provedores de armazenamento de mensagens e o catálogo de endereços podem escolher se deseja oferecer suporte a tabela de status. 
  
Como cada linha é fornecida por um recurso diferente, o conjunto de colunas pode variar a cada linha. Não há um conjunto de colunas que cada objeto de status é necessário fornecer e um conjunto de colunas que fornece de MAPI. Um provedor de serviços pode adicionar a esses conjuntos expor propriedades específicas do provedor. Por exemplo, provedores de armazenamento de mensagem podem adicionar **PR_STORE_RECORD_KEY** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) para fornecer a clientes com o identificador do seu armazenamento de mensagens. Clientes devem ter conhecimento de avanço da existência dessas informações extras para poder usá-lo. 
  
A tabela a seguir lista as propriedades que devem estar em cada linha da tabela de status. O implementador do objeto status fornece algumas das propriedades; outras pessoas estão computadas pelo MAPI.
  
|**Propriedades fornecidos pelo objeto de status**|**Propriedades fornecidos pelo MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Se o objeto de status fornece uma identidade, ele deve definir **PR_IDENTITY_DISPLAY** ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) e **PR_IDENTITY_SEARCH_KEY** ([ PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)) e incluir essas propriedades na tabela. 
  
Quatro propriedades são computadas pelo MAPI para cada linha da tabela de status:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
MAPI atribui um identificador de entrada para a linha de status para permitir que clientes abrir o objeto de status correspondente. Um identificador de linha também é atribuído para identificar a linha da tabela, como é uma chave de instância para identificar os dados no objeto de status. A propriedade **PR_OBJECT_TYPE** é definida como MAPI_STATUS. 
  
Para acessar a tabela de status, os clientes chame o método de [IMAPISession::GetStatusTable](imapisession-getstatustable.md) . Essa chamada não deve ser feita imediatamente na inicialização. Isso ocorre porque **GetStatusTable** precisa aguardar o MAPI spooler inicializar os provedores de transporte, uma operação que é adiado até após o cliente ter concluído o seu logon. **GetStatusTable** é uma chamada de relativamente rápida após o MAPI spooler concluiu seu processamento de inicialização. 
  
Informações de tabela de status podem ser usadas em uma variedade de formas, tais como para acessar um objeto de status, para determinar se um cliente está sendo executado em um modo conectado ou offline e para monitorar o estado de um provedor. Por exemplo, clientes podem abrir o objeto de status do provedor de um serviço específico, passando o valor da propriedade **PR_ENTRYID** para o método [IMAPISession::OpenEntry](imapisession-openentry.md) . O objeto de status suporta a interface **IMAPIStatus** , uma interface que contém os métodos para alterar uma senha de provedor de serviço, liberar a fila de mensagens, uma folha de propriedades de configuração de exibição ou confirmar o status diretamente com um provedor. Informações da tabela de status também podem ser usadas para criar uma caixa de diálogo para informar os clientes de andamento durante uma operação demorada. 
  
Provedores de serviços que têm suporte para a tabela de status usam o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para criar e atualizar seu linha. Sempre que ocorre uma alteração à sua linha, todos os objetos de coletor de eventos registrados para receber notificações de status de tabela devem ser notificados de aviso. Provedores de serviços podem chamar o método [IMAPISupport::Notify](imapisupport-notify.md) se estiver usando o utilitário de notificação de MAPI ou chamar o método de [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) do coletor de eventos cada advise diretamente. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

