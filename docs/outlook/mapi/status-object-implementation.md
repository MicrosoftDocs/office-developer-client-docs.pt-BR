---
title: Implementação do objeto de status
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e97efb70716ffbd7fa98f980ce8520cfcb988532
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336334"
---
# <a name="status-object-implementation"></a>Implementação do objeto de status

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Todos os provedores de serviços devem implementar um objeto de status e fornecer propriedades dele para a tabela de status da sessão. Você pode incluir uma ou mais linhas na tabela de status, dependendo do número de recursos que você controlar. Um provedor de transporte, por exemplo, deve criar uma linha na tabela de status para cada fila de mensagens gerenciada. Quando ocorrerem alterações, a linha da tabela de status apropriada deverá ser atualizada. Os objetos de status são implementados para fornecer acesso às informações incluídas na tabela de status e a informações adicionais não incluídas na tabela.
  
### <a name="to-implement-a-status-object"></a>Para implementar um objeto de status

1. Implemente **o método OpenStatusEntry** do objeto de logon. Quando os clientes querem abrir seu objeto de status, eles chamam [IMAPISession::OpenEntry](imapisession-openentry.md). O MAPI atende à solicitação aberta chamando o método **OpenStatusEntry** do provedor, fazendo com que seu provedor abra seu objeto de status e retorne ao cliente um ponteiro para sua implementação **IMAPIStatus.** Na implementação **de OpenStatusEntry,** conclua as seguintes etapas: 
    
   1. Execute as seguintes tarefas se o objeto de logon ainda não tiver criado um objeto de status:
    
      1. Chame o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) do objeto de suporte para acessar a seção de perfil do provedor. 
          
      2. Criar um novo objeto de status.
          
      3. Armazene uma referência à seção de perfil no objeto de status do provedor e chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) da seção de perfil para incrementar sua contagem de referência. 
          
      4. Armazene uma referência ao objeto de logon no objeto de status do provedor e chame o método **IUnknown::AddRef** do objeto de logon para incrementar sua contagem de referência. 
          
      5. Armazene uma referência ao objeto de status no objeto de logon do provedor.
    
   2. Chame o método **IUnknown::AddRef** do objeto de status para incrementar sua contagem de referência no objeto de logon. 
    
   3. De definir a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) do objeto de status como MAPI_STATUS.
    
   4. De definir  _o parâmetro de saída lppMAPIStatus_ para apontar para o objeto de status e retornar. 
    
   5. Verifique o _parâmetro de entrada ulFlags._ Se ele estiver definido como MAPI_MODIFY e seu provedor oferece suporte ao acesso de leitura/gravação ao seu objeto de status, retorne um objeto que pode ser escrito. No entanto, se o provedor não suportar o acesso de leitura/gravação ao seu objeto de status, não falhará. Retornar um objeto de status que seja somente leitura. Os clientes que esperam receber objetos de status de leitura/gravação devem verificar se a permissão de leitura/gravação foi concedida antes de tentar fazer qualquer alteração. 
    
2. Definir todas as propriedades necessárias do objeto de status e da tabela de status. As propriedades que você incluir na linha da tabela de status devem estar disponíveis por meio do objeto de status, exceto pelas propriedades calculadas por MAPI. As propriedades necessárias são as seguinte:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implemente [os métodos IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) apropriados para seu provedor. Dependendo do seu provedor, você não precisa implementar todos os quatro métodos em **IMAPIStatus**. Cada provedor deve implementar uma versão somente leitura dos métodos da interface [IMAPIProp : IUnknown](imapipropiunknown.md) e o método [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) 

   Os provedores de transporte também devem implementar [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)e todos os provedores devem dar suporte a [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md). No entanto, o suporte [para IMAPIStatus::ChangePassword](imapistatus-changepassword.md) é opcional. Somente provedores de serviços que exigem senhas e querem permitir que os usuários as alterem programaticamente precisam implementar esse método. Para cada método que você suporta, de definir o bit correspondente na **PR_RESOURCE_METHODS** propriedade. Por exemplo, se você tiver suporte **apenas para ValidateState** e **SettingsDialog,** **PR_RESOURCE_METHODS** para o seguinte: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Os clientes devem verificar o valor de **PR_RESOURCE_METHODS** antes de tentar chamar seu objeto de status. Manipular chamadas para qualquer um dos seus métodos sem suporte retornando MAPI_E_NO_SUPPORT. 
    
4. Chame [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) durante o logon para adicionar suas linhas à tabela de status. Passe uma matriz de valores de propriedade que contenha as informações de coluna para a linha e 0 para o _parâmetro ulFlags._ Se, em algum momento posteriormente, na sessão, o status do provedor mudar e for necessário atualizar as informações da coluna, chame **ModifyStatusRow** novamente com o sinalizador STATUSROW_UPDATE definido. 
    
Para obter mais informações sobre objetos de status, consulte [MAPI Status Objects](mapi-status-objects.md).
  
## <a name="see-also"></a>Confira também

- [Provedores de Serviços MAPI](mapi-service-providers.md)

