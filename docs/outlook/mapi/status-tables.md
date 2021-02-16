---
title: Tabelas de Status
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f2b2aca7-757f-4260-96a5-d0af55189711
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d612738ef8bf0e6925d89a5be7cb423695672d28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422359"
---
# <a name="status-tables"></a>Tabelas de Status

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A tabela de status contém informações relacionadas ao estado da sessão atual. Há uma tabela de status para cada sessão MAPI que inclui informações fornecidas por MAPI e por provedores de serviços. MAPI provides data for three rows: a row for the MAPI subsystem, a row for the MAPI spooler, and a row for the integrated address book. Como os provedores de transporte são necessários para fornecer informações de status à tabela de status, há uma linha para cada provedor de transporte ativo. Os provedores de armazenamento de mensagens e de agenda podem optar por dar suporte à tabela de status. 
  
Como cada linha é fornecida por um recurso diferente, o conjunto de colunas pode variar de linha para linha. Há um conjunto de colunas que cada objeto de status é necessário para fornecer e um conjunto de colunas que o MAPI fornece. Um provedor de serviços pode adicionar a esses conjuntos para expor propriedades específicas do provedor. Por exemplo, os provedores de repositório de mensagens **podem** adicionar PR_STORE_RECORD_KEY ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)) para fornecer aos clientes o identificador de seu repositório de mensagens. Os clientes devem ter conhecimento avançado da existência dessas informações extras para poder usá-los. 
  
A tabela a seguir lista as propriedades que devem estar em cada linha de tabela de status. O implementador do objeto de status fornece algumas das propriedades; outros são computados por MAPI.
  
|**Propriedades fornecidas pelo objeto de status**|**Propriedades fornecidas por MAPI**|
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))  <br/> |
|**PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))  <br/> |**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |
|**PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))  <br/> |**PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))  <br/> |
   
Se o objeto de status fornece **uma** identidade, ele deve definir PR_IDENTITY_DISPLAY ([PidTagIdentityDisplay](pidtagidentitydisplay-canonical-property.md)), **PR_IDENTITY_ENTRYID** ([PidTagIdentityEntryId](pidtagidentityentryid-canonical-property.md)) e **PR_IDENTITY_SEARCH_KEY** ([PidTagIdentitySearchKey](pidtagidentitysearchkey-canonical-property.md)), e incluir essas propriedades na tabela. 
  
Quatro propriedades são calculadas por MAPI para cada linha de tabela de status:
  
|||
|:-----|:-----|
|**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |**PR_ROWID** ([PidTagRowid](pidtagrowid-canonical-property.md))  <br/> |
   
O MAPI atribui um identificador de entrada à linha de status para permitir que os clientes abram o objeto de status correspondente. Um identificador de linha também é atribuído para identificar a linha na tabela como uma chave de instância para identificar os dados no objeto de status. A **PR_OBJECT_TYPE** propriedade é definida como MAPI_STATUS. 
  
Para acessar a tabela de status, os clientes chamam o [método IMAPISession::GetStatusTable.](imapisession-getstatustable.md) Essa chamada não deve ser feita imediatamente após a inicialização. Isso ocorre porque **GetStatusTable** precisa aguardar até que o spooler MAPI inicialize os provedores de transporte, uma operação que é adiada até que o cliente tenha concluído seu logon. **GetStatusTable é** uma chamada relativamente rápida depois que o spooler MAPI concluiu seu processamento de inicialização. 
  
As informações da tabela de status podem ser usadas de várias maneiras, como para acessar um objeto de status, para determinar se um cliente está sendo executado em um modo conectado ou offline e para monitorar o estado de um provedor. Por exemplo, os clientes podem abrir um objeto de status de um provedor de serviços específico passando o valor da propriedade **PR_ENTRYID** para o método [IMAPISession::OpenEntry.](imapisession-openentry.md) O objeto de status oferece suporte à interface **IMAPIStatus,** uma interface que contém métodos para alterar uma senha do provedor de serviços, liberar a fila de mensagens, exibir uma folha de propriedades de configuração ou confirmar o status com um provedor diretamente. As informações da tabela de status também podem ser usadas para criar uma caixa de diálogo para informar os clientes sobre o progresso durante uma operação demorada. 
  
Os provedores de serviços que suportam a tabela de status usam o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para criar e atualizar suas linhas. Sempre que ocorrer uma alteração em suas linhas, todos os objetos de pia de aviso registrados para receber notificações da tabela de status deverão ser notificados. Os provedores de serviços podem chamar o método [IMAPISupport::Notify](imapisupport-notify.md) se eles estão usando o utilitário de notificação MAPI ou chamar o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) de cada aviso diretamente. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

