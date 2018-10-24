---
title: Tabela de status e objetos de status
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 203765c1-4b08-4032-a5bf-18f3e752a899
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7ebd0c21a43ddb1deb01699f0ddf77d319216a4d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590061"
---
# <a name="status-table-and-status-objects"></a>Tabela de status e objetos de status

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI fornece uma tabela com informações sobre o status do subsistema de MAPI, spooler MAPI, catálogo de endereços ou um provedor de serviço específico. Você pode acessar esta tabela chamando [IMAPISession::GetStatusTable](imapisession-getstatustable.md).
  
Cada linha da tabela de status representa um objeto de status implementado por MAPI ou um provedor de serviços. Você pode usar um objeto de status para exibir a folha de propriedades de configuração de um provedor, para alterar uma senha de provedor, para carregar ou baixar mensagens de e para se comunicar com um provedor de transporte específica. 
  
Há duas maneiras de acessar um objeto de status:
  
- A tabela de status
    
- Por meio de um logon método do objeto **OpenStatusEntry** 
    
Porque os objetos de logon não estão disponíveis para os clientes, você deve usar a tabela de status para acessar objetos de status. A abordagem da tabela de status é indireta, exigindo algumas chamadas antes do objeto de status é aberto e um ponteiro para sua implementação **IMAPIStatus** retornado. 
  
 **Para usar a tabela de status para abrir um objeto de status**
  
1. Chame **IMAPIStatus::GetStatusTable** para recuperar um ponteiro [IMAPITable](imapitableiunknown.md) . 
    
2. Chamar o método de [IMAPITable::SetColumns](imapitable-setcolumns.md) da tabela status para limitar a coluna definida como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) e **PR_DISPLAY_NAME** ([ PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Limite o modo de exibição de tabela para um objeto de status específico. Implementações de MAPI, um cliente pode definir uma restrição de propriedade usando **PR_RESOURCE_TYPE**. Implementações de provedor de serviço, um cliente pode restringir em **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), o nome do provedor, ou em **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), o nome do provedor DLL arquivo.
    
4. Chame [IMAPITable:: Restrict](imapitable-restrict.md) para definir a restrição. 
    
5. Chame [HrQueryAllRows](hrqueryallrows.md), passando na estrutura de [SPropertyRestriction](spropertyrestriction.md) , para recuperar a linha que representa o status do provedor. 
    
6. Chame [IMAPISession::OpenEntry](imapisession-openentry.md), especificando o identificador de entrada da linha da tabela de status, para abrir o objeto de status e recuperar um ponteiro **IMAPIStatus** . 
    
Para exibir uma folha de propriedades, chame o status método do objeto [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para o provedor de destino. **SettingsDialog** exibe uma folha de propriedades para exibição e, em alguns casos, alterando as propriedades de configuração de um provedor. 
  
Para se comunicar com um provedor de transporte, chame o método de [IMAPIStatus::ValidateState](imapistatus-validatestate.md) do objeto seu status. **ValidateState** pode reconfigurar um provedor de transporte, impedir a exibição de uma interface de usuário do provedor e controlar uma sessão que envolve o download de cabeçalhos de mensagem de um servidor remoto, dependendo dos sinalizadores que você passa no. Por exemplo, para cancelar o download de cabeçalhos remotos, passe o sinalizador ABORT_XP_HEADER_OPERATION para **ValidateState**. Para conectar ou desconectar o servidor remoto, passe FORCE_XP_CONNECT ou FORCE_XP_DISCONNECT. Para reconfigurar o provedor, passe CONFIG_CHANGED. 
  
Clientes que implementam o envio ou recebimento de mensagens por demanda chame o método de [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) de um provedor de transporte ou o spooler MAPI. Você pode passar três sinalizadores para o método: FLUSH_UPLOAD, FLUSH_DOWNLOAD e FLUSH_FORCE. FLUSH_UPLOAD instrui o provedor ou o spooler MAPI para enviar todas as mensagens aguardando na fila de saída, enquanto FLUSH_DOWNLOAD instrui o provedor ou o spooler MAPI para receber todas as mensagens de entrada. FLUSH_FORCE pode ser definido com qualquer um dos outros sinalizadores para fazer com que o objeto de status executar o flush independentemente do tempo. 
  
Não espera poder chamar **SettingsDialog** ou [ChangePassword](imapistatus-changepassword.md) em qualquer um do subsistema MAPI, spooler MAPI ou endereço de objetos de status do catálogo. O subsistema de e para o endereço objetos de status de catálogo só oferecem suporte a **ValidateState**; o objeto de status do MAPI spooler suporta **FlushQueues** além dos **ValidateState**.
  
## <a name="see-also"></a>Confira também



[Tabelas de status](status-tables.md)
  
[Objetos de Status MAPI](mapi-status-objects.md)

