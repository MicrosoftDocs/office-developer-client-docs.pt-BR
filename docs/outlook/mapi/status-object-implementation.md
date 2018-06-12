---
title: Implementação do objeto de status
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 48fd3e28-c2d2-474d-9487-5e2f08ca7319
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 379378f2092f7b119a40ac44cbdcfa03f254b448
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770511"
---
# <a name="status-object-implementation"></a>Implementação do objeto de status

**Aplica-se a**: Outlook 
  
Todos os provedores de serviço devem implementar um objeto de status e forneça as propriedades à tabela de status de sessão. Você pode incluir uma ou mais linhas na tabela de status, dependendo do número de recursos que você controle. Um provedor de transporte, por exemplo, deve criar uma linha da tabela de status de cada fila de mensagens que ele gerencia. Quando ocorrem alterações, a linha da tabela de status apropriado deve ser atualizada. Objetos de status são implementados para fornecer acesso às informações incluído na tabela de status e para informações adicionais não incluídas na tabela.
  
### <a name="to-implement-a-status-object"></a>Para implementar um objeto de status

1. Implemente o método **OpenStatusEntry** do seu objeto de logon. Quando clientes quiser abrir o objeto de status, ligarem [IMAPISession::OpenEntry](imapisession-openentry.md). MAPI atende a solicitação aberta chamando o método de **OpenStatusEntry** do seu provedor, fazendo com que o seu provedor abrir o objeto de status e retornar ao cliente um ponteiro para sua implementação **IMAPIStatus** . Na sua implementação **OpenStatusEntry** , conclua as seguintes etapas: 
    
   1. Se seu objeto logon ainda não tiver criado um objeto de status, execute as seguintes tarefas:
    
      1. Chame o suporte ao método do objeto [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para acessar a seção de perfil do seu provedor. 
          
      2. Crie um novo objeto de status.
          
      3. Armazenar uma referência para a seção de perfil no objeto de status do seu provedor e chame o método de [AddRef](http://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) da seção perfil para incrementar sua contagem de referência. 
          
      4. Armazenar uma referência ao objeto logon no objeto de status do seu provedor e chame o método de **AddRef** do objeto logon para incrementar sua contagem de referência. 
          
      5. Armazene uma referência ao objeto de status no objeto de logon do seu provedor.
    
   2. Chame o status método do objeto **AddRef** para incrementar sua contagem de referência do objeto de logon. 
    
   3. Defina o status **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) propriedade de um objeto como MAPI_STATUS.
    
   4. Defina o parâmetro de saída _lppMAPIStatus_ para apontar para o objeto de status e retornar. 
    
   5. Verifique o parâmetro de entrada _ulFlags_ . Se ele for definido como MAPI_MODIFY e o provedor oferece suporte para acesso de leitura/gravação para seu objeto de status, retorne um objeto gravável. No entanto, se o seu provedor não oferece suporte para acesso de leitura/gravação para seu objeto de status, não falhe. Retorne um objeto de status que é somente leitura. Clientes que receberão o objetos do status de leitura/gravação devem verificar que foi concedida permissão de leitura/gravação antes de tentar fazer alterações. 
    
2. Todos o status obrigatório defina as propriedades de objeto e o status da tabela. As propriedades que você pode incluir em sua linha da tabela de status devem estar disponíveis por meio de seu objeto de status, exceto as propriedades calculado MAPI. As propriedades necessárias são:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implementar o [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) métodos apropriados para seu provedor. Dependendo do seu provedor, você não precisará implementar todos os quatro métodos em **IMAPIStatus**. Cada provedor deve implementar uma versão somente leitura dos métodos do [IMAPIProp: IUnknown](imapipropiunknown.md) interface e o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . 

   Provedores de transporte também deverá implementar [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md)e todos os provedores devem oferecer suporte a [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md). No entanto, o suporte para [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) é opcional. Apenas os provedores de serviços que exigem senhas e permitir que os usuários alterem programaticamente precisam implementar esse método. Para cada método suportado, defina o bit correspondente na propriedade **PR_RESOURCE_METHODS** . Por exemplo, caso você ofereça suporte **ValidateState** e **SettingsDialog** apenas, defina **PR_RESOURCE_METHODS** como a seguir: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Os clientes devem verificar o valor de **PR_RESOURCE_METHODS** antes de tentar chamar seu objeto de status. Trata as chamadas para qualquer um dos seus métodos sem suporte, retornando MAPI_E_NO_SUPPORT. 
    
4. Chame [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) durante o logon para adicionar sua linha ou linhas à tabela de status. Passe uma matriz de valor de propriedade que contém as informações de coluna para a linha e 0 para o parâmetro _ulFlags_ . Se em algum momento posterior na sessão de alteração de status do seu provedor e ele ficar necessário para atualizar as informações de coluna, chame **ModifyStatusRow** novamente com o sinalizador STATUSROW_UPDATE definido. 
    
Para obter mais informações sobre objetos de status, consulte [Objetos de Status de MAPI](mapi-status-objects.md).
  
## <a name="see-also"></a>Confira também

- [Provedores de serviços MAPI](mapi-service-providers.md)

