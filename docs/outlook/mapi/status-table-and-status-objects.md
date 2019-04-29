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
ms.openlocfilehash: 3eb190069b43ea1960c3b6edf30a9e0b782d2c41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425173"
---
# <a name="status-table-and-status-objects"></a>Tabela de status e objetos de status

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI fornece uma tabela com informações sobre o status do subsistema MAPI, do spooler MAPI, do catálogo de endereços ou de um provedor de serviços específico. Você pode acessar esta tabela chamando [IMAPISession::](imapisession-getstatustable.md)getstatustable.
  
Cada linha na tabela status representa um objeto status implementado por MAPI ou um provedor de serviços. Você pode usar um objeto status para exibir uma folha de propriedades de configuração do provedor, para alterar uma senha de provedor, para carregar ou baixar mensagens e para se comunicar com um determinado provedor de transporte. 
  
Há duas maneiras de acessar um objeto status:
  
- Pela tabela de status
    
- Por meio do método **OpenStatusEntry** de um objeto de logon 
    
Como os objetos de logon não estão disponíveis para clientes, você deve usar a tabela de status para acessar os objetos status. A abordagem da tabela de status é indireta, exigindo algumas chamadas antes que o objeto de status seja aberto e um ponteiro para sua implementação do **IMAPIStatus** seja retornado. 
  
 **Para usar a tabela status para abrir um objeto status**
  
1. Chame **IMAPIStatus::** getstatustable para recuperar um [](imapitableiunknown.md) ponteiro IMAPITable. 
    
2. Chame o método imApitable da tabela de status [::](imapitable-setcolumns.md) SetColumns para limitar o conjunto de colunas a **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) e **PR_DISPLAY_NAME** ([ PidTagDisplayName](pidtagdisplayname-canonical-property.md)).
    
3. Limitar o modo de exibição de tabela a um objeto status específico. Para implementações MAPI, um cliente pode definir uma restrição de propriedade usando **PR_RESOURCE_TYPE**. Para implementações de provedor de serviços, um cliente pode restringir no **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), o nome do provedor ou no **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)), o nome da dll do provedor arquivo.
    
4. Call [IMAPITable:: Restrict](imapitable-restrict.md) para definir a restrição. 
    
5. Chame [HrQueryAllRows](hrqueryallrows.md), passando na estrutura [SPropertyRestriction](spropertyrestriction.md) , para recuperar a linha que representa o status do provedor. 
    
6. Chame [IMAPISession:: OpenEntry](imapisession-openentry.md), especificando o identificador de entrada da linha da tabela de status, para abrir o objeto status e recuperar um ponteiro do **IMAPIStatus** . 
    
Para exibir uma folha de propriedades, chame o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) do objeto status para o provedor de destino. **SettingsDialog** exibe uma folha de propriedades para exibição e, em alguns casos, alterar as propriedades de configuração de um provedor. 
  
Para se comunicar com um provedor de transporte, chame o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) do objeto status. **ValidateState** pode reconfigurar um provedor de transporte, impedir o provedor de exibir uma interface de usuário e controlar uma sessão que envolve o download de cabeçalhos de mensagens de um servidor remoto, dependendo dos sinalizadores passados. Por exemplo, para cancelar o download de cabeçalhos remotos, passe o sinalizador ABORT_XP_HEADER_OPERATION **** para ValidateState. Para conectar ou desconectar do servidor remoto, passe FORCE_XP_CONNECT ou FORCE_XP_DISCONNECT. Para reconfigurar o provedor, passe CONFIG_CHANGED. 
  
Os clientes que implementam o envio ou o recebimento de mensagens sob demanda chamam um provedor de transporte ou o método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) do spooler MAPI. Você pode passar três sinalizadores para o método: FLUSH_UPLOAD, FLUSH_DOWNLOAD e FLUSH_FORCE. FLUSH_UPLOAD instrui o provedor ou o spooler MAPI a enviar mensagens que estão aguardando na fila de saída enquanto o FLUSH_DOWNLOAD instrui o provedor ou o spooler MAPI a receber qualquer mensagem de entrada. FLUSH_FORCE pode ser definido com qualquer um dos outros sinalizadores para fazer com que o objeto status execute a liberação independentemente do intervalo. 
  
Não espere ser possível chamar **SettingsDialog** ou [ChangePassword](imapistatus-changepassword.md) em qualquer um dos objetos de status de subsistema MAPI, spooler MAPI ou catálogo de endereços. Os objetos de status de subsistema e catálogo de endereços **** só dão suporte a ValidateState; o objeto de status do spooler MAPI oferece suporte a **FlushQueues** , além de **ValidateState**.
  
## <a name="see-also"></a>Confira também



[Tabelas de status](status-tables.md)
  
[Objetos de status MAPI](mapi-status-objects.md)

