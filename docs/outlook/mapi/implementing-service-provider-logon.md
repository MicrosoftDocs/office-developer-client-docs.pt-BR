---
title: Implementar o logon do provedor de serviços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1baa987961eecc6ee08b3ceb039062c8f1090ff7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589550"
---
# <a name="implementing-service-provider-logon"></a>Implementar o logon do provedor de serviços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI chama um método em seu objeto provedor para começar o processo de logon usando o ponteiro que você retornar de sua função de ponto de entrada. O método varia, dependendo do tipo de provedor de serviços da seguinte maneira:
  
- [IABProvider::Logon](iabprovider-logon.md) para provedores de catálogo de endereços 
    
- [IMSProvider::Logon](imsprovider-logon.md) para provedores de armazenamento de mensagem 
    
- [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) para provedores de transporte 
    
Execute as seguintes tarefas em qualquer método de logon que você implementar:
  
1. Incrementa a contagem de referência no objeto suporte que é passada como um parâmetro de entrada chamando o método [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) . 
    
2. Chame o suporte ao método do objeto [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para acessar a seção de perfil. 
    
3. Chame o método de [IMAPIProp::SetProps](imapiprop-setprops.md) da seção perfil para definir as seguintes propriedades: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > Não tente definir as propriedades da seção perfil **PR_RESOURCE_FLAGS** ou **PR_PROVIDER_DLL_NAME** . Ao fazer logon, essas propriedades são somente leitura. 
  
4. Verifique se as propriedades que você precisa para que a configuração seja são armazenadas no perfil ou estão disponíveis a partir do usuário. Para obter mais informações sobre como verificar sua configuração, consulte [Verificando a configuração de provedor de serviços](verifying-service-provider-configuration.md).
    
5. Chame o método de [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) de suporte do objeto para registrar um identificador exclusivo, ou [MAPIUID](mapiuid.md), se seu provedor for um provedor de repositório de catálogo ou mensagem de endereço. Provedores de transporte registrar estruturas **MAPIUID** quando o método seus [IXPLogon::AddressTypes](ixplogon-addresstypes.md) chamadas de MAPI. Para obter mais informações sobre como registrar um **MAPIUID**, consulte [Registrando serviço provedor exclusivo identificadores](registering-service-provider-unique-identifiers.md).
    
6. Criar uma instância de um objeto de logon e voltar com um dos seguintes valores:
    
  - S_OK para indicar um logon bem-sucedido.
    
  - MAPI_E_UNCONFIGURED para indicar que um ou mais das propriedades de configuração não estavam disponíveis.
    
  - MAPI_E_USER_CANCEL para indicar que o usuário cancelou a caixa de diálogo Configuração, fazendo com que as propriedades de configuração estar disponível.
    
  - MAPI_E_FAILONEPROVIDER para indicar que o provedor não pôde ser configurado, mas que MAPI deve permitir que ela seja usada independentemente. Métodos de logon devem retornar esse valor para reportar um erro não fatal, como quando o provedor exige uma senha e não pode solicitar ao usuário para que ele porque a interface do usuário está desabilitada. 
    
A lista anterior de tarefas descreve uma implementação mínima para um método de logon do provedor de serviço. Você pode incluir a funcionalidade adicional, se necessário. Por exemplo, alguns provedores chamarem [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para atualizar a tabela de status em seu método de logon. 
  
> [!NOTE]
> Para obter o melhor desempenho na hora do logon, evite chamar [IMAPISupport::PrepareSubmit](imapisupport-preparesubmit.md) ou [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md). Antes que essas chamadas podem concluir e retornar o controle ao seu método de logon, o MAPI spooler deve ser iniciado. 
  
## <a name="see-also"></a>Confira também

- [Iniciar um provedor de serviços](starting-a-service-provider.md)

