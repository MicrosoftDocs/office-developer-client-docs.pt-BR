---
title: Implementar o logon do provedor de serviços
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3d3c309f-fe60-43a9-beda-16b09ec769db
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 533c00a0c994e7dfc5adc476899553bc39a2a9ab
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310084"
---
# <a name="implementing-service-provider-logon"></a>Implementar o logon do provedor de serviços

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI chama um método no seu objeto Provider para começar o processo de logon usando o ponteiro retornado da função de ponto de entrada. O método varia conforme a seguir, dependendo do tipo de seu provedor de serviços:
  
- [IABProvider:: logon](iabprovider-logon.md) para provedores de catálogo de endereços 
    
- [IMSProvider:: logon](imsprovider-logon.md) para provedores de repositórios de mensagens 
    
- [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) para provedores de transporte 
    
Execute as seguintes tarefas em qualquer método de logon que você implementar:
  
1. Incrementa a contagem de referência no objeto support que é passado como um parâmetro de entrada chamando seu método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) . 
    
2. Chame o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) do objeto support para acessar sua seção de perfil. 
    
3. Chame o método [IMAPIProp::](imapiprop-setprops.md) SetProps da seção de perfil para definir as seguintes propriedades: 
    
  - **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
  - **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
    
  - **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
    
  - **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))
    
  > [!NOTE]
  > Não tente definir as propriedades **PR_RESOURCE_FLAGS** ou **PR_PROVIDER_DLL_NAME** da seção de perfil. No momento do logon, essas propriedades são somente leitura. 
  
4. Verifique se as propriedades necessárias para a configuração estão armazenadas no perfil ou estão disponíveis a partir do usuário. Para obter mais informações sobre como verificar sua configuração, consulte [verifyIng Service Provider Configuration](verifying-service-provider-configuration.md).
    
5. Chame o método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) do objeto support para registrar um identificador exclusivo ou [MAPIUID](mapiuid.md), se seu provedor for um catálogo de endereços ou um provedor de repositório de mensagens. Provedores de transporte registram estruturas **MAPIUID** quando MAPI chama o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . Para obter mais informações sobre como registrar um **MAPIUID**, consulte [registro de identificadorEs exclusivos do provedor de serviços](registering-service-provider-unique-identifiers.md).
    
6. Crie uma instância de um objeto de logon e retorne com um dos seguintes valores:
    
  - S_OK para indicar um logon bem-sucedido.
    
  - MAPI_E_UNCONFIGURED para indicar que uma ou mais das propriedades de configuração não estavam disponíveis.
    
  - MAPI_E_USER_CANCEL para indicar que o usuário cancelou a caixa de diálogo de configuração, fazendo com que as propriedades de configuração não estejam disponíveis.
    
  - MAPI_E_FAILONEPROVIDER para indicar que o provedor não pôde ser configurado, mas esse MAPI deve permitir que ele seja usado independentemente. Os métodos de logon devem retornar esse valor para relatar um erro não fatal, como quando o provedor requer uma senha e não pode solicitar ao usuário porque a interface do usuário está desabilitada. 
    
A lista anterior de tarefas descreve uma implementação mínima para um método de logon do provedor de serviços. Você pode incluir funcionalidade adicional, se necessário. Por exemplo, alguns provedores chamam [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para atualizar a tabela status no seu método de logon. 
  
> [!NOTE]
> Para obter o melhor desempenho no momento do logon, evite chamar o [IMAPISupport::P reparesubmit](imapisupport-preparesubmit.md) ou [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md). Antes que essas chamadas possam concluir e retornar o controle para seu método de logon, o spooler MAPI deve ser iniciado. 
  
## <a name="see-also"></a>Confira também

- [Iniciar um provedor de serviços](starting-a-service-provider.md)

