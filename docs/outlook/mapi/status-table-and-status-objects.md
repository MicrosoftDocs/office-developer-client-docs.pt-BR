---
title: Tabela de Status e Objetos de Status
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425173"
---
# <a name="status-table-and-status-objects"></a>Tabela de Status e Objetos de Status

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI provides a table with information about the status of the MAPI subsystem, MAPI spooler, address book, or a particular service provider. Você pode acessar esta tabela chamando [IMAPISession::GetStatusTable](imapisession-getstatustable.md).
  
Cada linha na tabela de status representa um objeto de status implementado por MAPI ou um provedor de serviços. Você pode usar um objeto de status para exibir a folha de propriedades de configuração de um provedor, alterar uma senha de provedor, carregar ou baixar mensagens e se comunicar com um provedor de transporte específico. 
  
Há duas maneiras de acessar um objeto de status:
  
- Por meio da tabela de status
    
- Por meio do método **OpenStatusEntry** de um objeto de logon 
    
Como os objetos de logon não estão disponíveis para os clientes, você deve usar a tabela de status para acessar objetos de status. A abordagem da tabela de status é indireta, exigindo algumas chamadas antes de o objeto de status ser aberto e um ponteiro para sua **implementação IMAPIStatus** retornado. 
  
 **Para usar a tabela de status para abrir um objeto de status**
  
1. Chame **IMAPIStatus::GetStatusTable** para recuperar um [ponteiro IMAPITable.](imapitableiunknown.md) 
    
2. Chame o método [IMAPITable::SetColumns](imapitable-setcolumns.md) da tabela de status para limitar o conjunto de colunas **a PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) e **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Limite o exibição de tabela a um objeto de status específico. Para implementações de MAPI, um cliente pode definir uma restrição de propriedade usando **PR_RESOURCE_TYPE**. Para implementações de provedor de serviços, um cliente pode restringir PR_PROVIDER_DISPLAY **(** [PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), o nome do provedor ou em **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), o nome do arquivo DLL do provedor.
    
4. Chame [IMAPITable::Restrict](imapitable-restrict.md) para definir a restrição. 
    
5. Chame [HrQueryAllRows](hrqueryallrows.md), passando a estrutura [SPropertyRestriction,](spropertyrestriction.md) para recuperar a linha que representa o status do provedor. 
    
6. Chame [IMAPISession::OpenEntry](imapisession-openentry.md), especificando o identificador de entrada da linha da tabela de status, para abrir o objeto de status e recuperar um ponteiro **IMAPIStatus.** 
    
Para exibir uma folha de propriedades, chame o método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) do objeto de status para o provedor de destino. **SettingsDialog** exibe uma folha de propriedades para exibição e, em alguns casos, alterando as propriedades de configuração de um provedor. 
  
Para se comunicar com um provedor de transporte, chame o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) do objeto de status. **ValidateState** pode reconfigurar um provedor de transporte, impedir que o provedor de exibir uma interface do usuário e controlar uma sessão que envolve o download de headers de mensagens de um servidor remoto, dependendo dos sinalizadores passados. Por exemplo, para cancelar o download de títulos remotos, passe o sinalizador ABORT_XP_HEADER_OPERATION para **ValidateState**. Para se conectar ou desconectar do servidor remoto, passe FORCE_XP_CONNECT ou FORCE_XP_DISCONNECT. Para reconfigurar o provedor, passe CONFIG_CHANGED. 
  
Clientes que implementam o envio ou o recebimento de mensagens sob demanda chamam um provedor de transporte ou o método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) do spooler MAPI. Você pode passar três sinalizadores para o método: FLUSH_UPLOAD, FLUSH_DOWNLOAD e FLUSH_FORCE. FLUSH_UPLOAD instrui o provedor ou o spooler MAPI a enviar todas as mensagens em espera na fila de saída enquanto o FLUSH_DOWNLOAD instrui o provedor ou o spooler MAPI a receber qualquer mensagem de entrada. FLUSH_FORCE pode ser definido com qualquer um dos outros sinalizadores para fazer com que o objeto de status execute a liberação independentemente do tempo. 
  
Não espere chamar **SettingsDialog** ou [ChangePassword](imapistatus-changepassword.md) em nenhum dos objetos de status do subsistema MAPI, do spooler MAPI ou do livro de endereços. Tanto o subsistema quanto os objetos de status do livro de endereços só suportam **ValidateState**; o objeto de status do spooler MAPI **dá suporte a FlushQueues,** além de **ValidateState**.
  
## <a name="see-also"></a>Confira também



[Tabelas de Status](status-tables.md)
  
[Objetos de status MAPI](mapi-status-objects.md)

