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
  
Todos os provedores de serviços devem implementar um objeto status e fornecer as propriedades dele para a tabela de status da sessão. Você pode incluir uma ou mais linhas na tabela de status, dependendo do número de recursos que você controla. Um provedor de transporte, por exemplo, deve criar uma linha na tabela de status para cada fila de mensagens gerenciada. Quando ocorrem alterações, a linha da tabela de status apropriada deve ser atualizada. Os objetos de status são implementados para fornecer acesso às informações incluídas na tabela de status e às informações adicionais não incluídas na tabela.
  
### <a name="to-implement-a-status-object"></a>Para implementar um objeto status

1. Implemente o método **OpenStatusEntry** do seu objeto logon. Quando os clientes desejam abrir seu objeto status, eles chamam [IMAPISession:: OpenEntry](imapisession-openentry.md). O MAPI atende à solicitação de abertura chamando o método **OpenStatusEntry** do provedor, fazendo com que o provedor abra seu objeto status e retorne ao cliente um ponteiro para sua implementação do **IMAPIStatus** . Na implementação do **OpenStatusEntry** , conclua as seguintes etapas: 
    
   1. Execute as seguintes tarefas se o seu objeto de logon ainda não tiver criado um objeto status:
    
      1. Chame o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) do objeto support para acessar a seção de perfil do provedor. 
          
      2. Criar um novo objeto status.
          
      3. Armazenar uma referência à seção de perfil no objeto de status do provedor e chamar o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/b4316efd-73d4-4995-b898-8025a316ba63%28Office.15%29.aspx) da seção de perfil para incrementar sua contagem de referência. 
          
      4. Armazenar uma referência ao objeto de logon no objeto de status do provedor e chamar o método **IUnknown:: AddRef** do objeto de logon para incrementar sua contagem de referência. 
          
      5. Armazenar uma referência ao objeto status no objeto de logon do provedor.
    
   2. Chame o método **IUnknown:: AddRef** do objeto status para incrementar sua contagem de referência no objeto logon. 
    
   3. Defina a propriedade **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)) do objeto status como MAPI_STATUS.
    
   4. Defina o parâmetro de saída _lppMAPIStatus_ para apontar para o objeto status e retornar. 
    
   5. Verifique o parâmetro de entrada _parâmetroulflags_ . Se ele estiver definido como MAPI_MODIFY e o provedor oferecer suporte ao acesso de leitura/gravação para seu objeto status, retorne um objeto gravável. No enTanto, se o provedor não oferecer suporte ao acesso de leitura/gravação ao objeto status, não falhará. Retornar um objeto de status somente leitura. Os clientes que esperam receber objetos de status de leitura/gravação devem verificar se a permissão de leitura/gravação foi concedida antes de tentar fazer qualquer alteração. 
    
2. Defina todas as propriedades de objeto status e tabela de status necessárias. As propriedades que você incluir na linha da tabela de status devem estar disponíveis por meio do seu objeto status, exceto as propriedades calculadas por MAPI. As propriedades necessárias são as seguintes:
    
   - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
   - **PR_PROVIDER_DLL_NAME** ([PidTagProviderDllName](pidtagproviderdllname-canonical-property.md))
    
   - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
   - **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md))
    
   - **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
    
   - **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))
    
   - **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md))
    
3. Implemente os métodos [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) que são apropriados para o seu provedor. Dependendo do seu provedor, você não precisa implementar todos os quatro métodos no **IMAPIStatus**. Cada provedor deve implementar uma versão somente leitura dos métodos da interface [IMAPIProp: IUnknown](imapipropiunknown.md) e o método [IMAPIStatus:: ValidateState](imapistatus-validatestate.md) . 

   Os provedores de transporte também devem implementar [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md)e todos os provedores devem oferecer suporte a [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md). No enTanto, o suporte para [IMAPIStatus:: ChangePassword](imapistatus-changepassword.md) é opcional. Somente provedores de serviço que exigem senhas e querem permitir que os usuários alterá-los programaticamente precisam implementar esse método. Para cada método que você dá suporte, defina o bit correspondente na propriedade **PR_RESOURCE_METHODS** . Por exemplo, se você oferecer **** suporte a ValidateState e **SettingsDialog** apenas, defina **PR_RESOURCE_METHODS** como o seguinte: 
    
   `STATUS_VALIDATE_STATE | STATUS_SETTINGS_DIALOG`
    
   Os clientes devem verificar o valor de **PR_RESOURCE_METHODS** antes de tentar chamar o objeto status. Gerenciar chamadas para qualquer um dos métodos sem suporte, retornando MAPI_E_NO_SUPPORT. 
    
4. Chame [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) durante o logon para adicionar sua linha ou linhas à tabela de status. Passe uma matriz de valor de propriedade que contém as informações de coluna da linha e 0 para o parâmetro _parâmetroulflags_ . Se, em algum momento, posteriormente na sessão, o status do provedor mudar e for necessário atualizar as informações da coluna, chame **ModifyStatusRow** novamente com o sinalizador STATUSROW_UPDATE definido. 
    
Para obter mais informações sobre objetos status, consulte [MAPI status Objects](mapi-status-objects.md).
  
## <a name="see-also"></a>Confira também

- [Provedores de serviço MAPI](mapi-service-providers.md)

