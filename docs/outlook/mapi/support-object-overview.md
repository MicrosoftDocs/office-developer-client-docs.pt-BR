---
title: Visão geral do objeto support
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 55d8a9c78ae5132eaa8cf0f0aec5b252ef83b926
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433609"
---
# <a name="support-object-overview"></a>Visão geral do objeto support

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI fornece um objeto de suporte, um objeto que implementa a interface [IMAPISupport : IUnknown,](imapisupportiunknown.md) para todos os provedores de serviços durante o logon e para todos os serviços de mensagem durante a configuração. 
  
Os objetos de suporte não são acessíveis pelos clientes; eles são implementados por MAPI e chamados apenas por provedores de serviços. A interface **IMAPISupport** é especificada no arquivo de header Mapispi.h. Seu identificador é IID_IMAPISup e seu tipo de ponteiro é LPMAPISUP. Nenhuma propriedade MAPI é exposta por objetos de suporte. 
  
Um provedor pode receber um ou mais objetos de suporte, dependendo do número de vezes que o MAPI registra o provedor ou do número de vezes que a função de entrada do serviço de mensagens do provedor é chamada. Normalmente, um provedor será conectado pelo menos uma vez por sessão. Os provedores de transporte e de agenda são registrados sempre que um cliente inicia uma sessão com uma entrada de perfil que os solicita. Os provedores de repositório de mensagens são registrados sempre que um cliente chama o método [IMAPISession::OpenMsgStore.](imapisession-openmsgstore.md) 
  
No caso de vários logons em uma sessão, você pode optar por manter e usar cada objeto de suporte separadamente ou manter e usar somente o primeiro, descartando cada objeto de suporte subsequente. Para reter um objeto de suporte, chame **seu método IUnknown::AddRef.** Chamar **AddRef** em um objeto de suporte que você deseja reter ao longo de uma sessão é extremamente importante; se a chamada não for feita, o MAPI liberará o objeto de suporte e liberará sua memória. 
  
O objetivo do objeto de suporte é fornecer implementações para um número bastante grande de métodos comumente usados pelos provedores. Cada objeto de suporte também contém dados contextuais específicos de sua própria instância, como a sessão em que o provedor está executando, a seção de perfil que o provedor está usando e informações de erro para a sessão. 
  
Há quatro tipos diferentes de objetos de suporte: um para cada tipo de provedor principal (agenda, armazenamento de mensagens e transporte) e outro para suporte de configuração. 
  
MAPI customizes each support object by including implementations of methods that are relevant for its usage. Implementações de alguns métodos, como [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), estão incluídas em todos os objetos de suporte. Implementações de outros métodos, como [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md), aplicam-se somente a objetos de suporte específicos. Somente o armazenamento de mensagens e os provedores de transporte podem usar esse método; quando um provedor de agendamento de endereços ou um serviço de mensagens tentar chamá-lo, o MAPI retornará MAPI_E_NO_SUPPORT.
  
Os objetos de suporte podem ser usados para realizar muitas tarefas, como as seguintes:
  
- Acessando uma seção de perfil.
    
- Copiando pastas ou mensagens. Para obter mais informações, [consulte Copiar ou mover uma mensagem ou uma pasta.](copying-or-moving-a-message-or-a-folder.md)
    
- Acessar objetos que pertencem a outros provedores. Para obter mais informações, consulte [Suporte ao acesso e comparação de objetos.](supporting-object-access-and-comparison.md) 
    
- Manipulação de notificação de evento. Para obter mais informações, consulte [Suporte à notificação de evento.](supporting-event-notification.md)
    
- Alocando e liberando memória.
    
- Obtendo um identificador exclusivo.
    
- Invalidar objetos.
    
- Tratamento de erros.
    
- Registrando pré-processadores de mensagem. 
    
- Preparando relatórios de entrega de mensagens. 
    
No momento do logon, o MAPI chama o método de logon do objeto provedor de cada provedor de serviços. Para provedores de agendas, MAPI chama [IABProvider::Logon](iabprovider-logon.md). Para provedores de armazenamento de mensagens, MAPI chama [IMSProvider::Logon](imsprovider-logon.md). Para provedores de transporte, MAPI chama [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). MAPI passa um ponteiro para o objeto de suporte apropriado em um dos parâmetros para esse método. O método de logon, por sua vez, instania um objeto de logon, passando a ele o ponteiro do objeto de suporte. O objeto de logon chama o método **IUnknown::AddRef** do objeto de suporte para retê-lo, se necessário. Para obter mais informações sobre o processo de logon para provedores de serviços, consulte [Iniciando um provedor de serviços.](starting-a-service-provider.md)
  
Quando um cliente faz logoff, o MAPI chama o método de logoff do objeto de logon. O método logoff chama o método **IUnknown::Release** do objeto de suporte para indicar que o provedor não pretende mais chamar nenhum dos métodos de suporte. Assim como no logon, os métodos logoff têm nomes ligeiramente diferentes. As interfaces [IABLogon](iablogoniunknown.md) [e IMSLogon](imslogoniunknown.md) têm **métodos Logoff;** a interface [IXPLogon](ixplogoniunknown.md) tem um [método TransportLogoff.](ixplogon-transportlogoff.md) 
  
As funções de ponto de entrada do serviço de mensagens são chamadas quando uma tentativa de logon falha com o erro MAPI_E_UNCONFIGURED ou quando um cliente inicia uma solicitação de configuração. MAPI instantiates a configuration support object and calls the message service entry point function for either the unconfigured provider or the provider whose configuration is about to change. Ao contrário dos outros objetos de suporte, os objetos de suporte de configuração são válidos apenas até que a função de ponto de entrada retorne; os serviços de mensagem não chamam os métodos **AddRef** desses objetos para retê-los. 
  
Normalmente, o MAPI faz chamadas para a função de ponto de entrada do serviço de mensagens do provedor, mas, às vezes, um provedor é solicitado a fazer a chamada. Isso pode ocorrer quando um cliente chama o método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) de um provedor para solicitar que o provedor exibir sua folha de propriedades de configuração. **SettingsDialog** deve chamar [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) para obter um objeto de suporte de configuração que ele pode passar para a função de ponto de entrada do serviço de mensagens. 
  
O [método IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) está disponível para determinar os endereços das funções de alocação e de alocação de memória sem precisar vincular com MAPI. O **uso de GetMemAllocRoutines** também facilita o rastreamento de vazamentos de memória envolvendo as chamadas de função de alocação com código de depuração. Se você chamar **GetMemAllocRoutines**, conforme recomendado, faça isso antes de chamar a [função CreateIProp,](createiprop.md) que requer os endereços de função de alocação como parâmetros. 
  
Quando você precisar criar um novo objeto de armazenamento de endereços ou de armazenamento de mensagens, crie e de definida uma chave de pesquisa para o objeto em sua **propriedade PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Chame [IMAPISupport::NewUID](imapisupport-newuid.md) para obter um identificador exclusivo a ser usado na criação de uma chave de pesquisa. Não use seu próprio [MAPIUID](mapiuid.md)codificado. **MAPIUID** de um provedor deve ser usado somente para identificadores de entrada. Para obter mais informações sobre como construir chaves de pesquisa, consulte [Registro MAPI e chaves de pesquisa.](mapi-record-and-search-keys.md)
  
Às vezes, um aplicativo cliente pode liberar um objeto sem liberar um ou mais de seus objetos associados. Nesse caso, um provedor pode precisar renderizar um objeto não lançado inutilizável. Para fazer isso, o provedor libera todos os recursos conectados ao objeto e chama [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) para invalidar a vtable do objeto. **MakeInvalid** substitui os métodos **IUnknown** da vtable (**QueryInterface**, **AddRef** e **Release**) por implementações mapi padrão e faz com que todos os outros métodos retornem MAPI_E_INVALID_OBJECT. **MakeInvalid** também libera toda a memória do objeto que não seja vtable. 
  
## <a name="see-also"></a>Confira também



[Provedores de Serviços MAPI](mapi-service-providers.md)

