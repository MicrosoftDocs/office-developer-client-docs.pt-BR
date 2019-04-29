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
  
O MAPI fornece um objeto support, um objeto que implementa a interface [IMAPISupport: IUnknown](imapisupportiunknown.md) , para todos os provedores de serviços durante o logon e para todos os serviços de mensagens durante a configuração. 
  
Os objetos de suporte não podem ser acessados por clientes; Eles são implementados por MAPI e chamados apenas por provedores de serviço. A interface **IMAPISupport** é especificada no arquivo de cabeçalho Mapispi. h. Seu identificador é IID_IMAPISup e o tipo de ponteiro é LPMAPISUP. Nenhuma propriedade MAPI é exposta por objetos de suporte. 
  
Um provedor pode ter um ou mais objetos support, dependendo do número de vezes que o MAPI registra o provedor ou o número de vezes que a função de entrada de serviço de mensagens do provedor é chamada. Normalmente, um provedor será conectado pelo menos uma vez por sessão. O catálogo de endereços e os provedores de transporte são registrados sempre que um cliente inicia uma sessão com uma entrada de perfil que as solicita. Os provedores de repositório de mensagens são registrados sempre que um cliente chama o método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) . 
  
No caso de vários logons em uma sessão, você pode optar por manter e usar cada objeto de suporte separadamente ou para reter e usar apenas o primeiro, descartando cada objeto de suporte subsequente. Para manter um objeto support, chame o método **IUnknown:: AddRef** . Chamar **AddRef** em um objeto support que você deseja manter em uma sessão é extremamente importante; se a chamada não for feita, o MAPI libera o objeto support e libera sua memória. 
  
O objetivo do objeto support é fornecer implementações para um número muito grande de métodos comumente usados pelos provedores. Cada objeto de suporte também contém dados contextuais específicos para sua própria instância, como a sessão na qual o provedor está sendo executado, a seção de perfil que o provedor está usando e informações de erro para a sessão. 
  
Há quatro tipos diferentes de objetos de suporte: um para cada tipo de provedor principal (catálogo de endereços, repositório de mensagens e transporte) e um para suporte de configuração. 
  
MAPI personaliza cada objeto support, incluindo implementações de métodos que são relevantes para seu uso. As implementações de alguns métodos, como [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md), estão incluídas em todos os objetos de suporte. Implementações de outros métodos, como [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md), só se aplicam a objetos de suporte específicos. Somente o repositório de mensagens e os provedores de transporte podem usar esse método; Quando um provedor de catálogo de endereços ou serviço de mensagens tenta chamá-lo, o MAPI retorna MAPI_E_NO_SUPPORT.
  
Os objetos de suporte podem ser usados para realizar várias tarefas, como as seguintes:
  
- Acessar uma seção de perfil.
    
- Copiando pastas ou mensagens. Para obter mais informações, consulte [copiar ou mover uma mensagem ou uma pasta](copying-or-moving-a-message-or-a-folder.md).
    
- Acessar objetos que pertencem a outros provedores. Para obter mais informações, consulte [support Object Access and Comparison](supporting-object-access-and-comparison.md). 
    
- Tratamento de notificações de eventos. Para obter mais informações, consulte [support Event Notification](supporting-event-notification.md).
    
- Alocar e liberar memória.
    
- Obter um identificador exclusivo.
    
- Invalidar objetos.
    
- Tratamento de erros.
    
- Registro de pré-processadors de mensagem. 
    
- Preparação de relatórios de entrega de mensagens. 
    
No momento do logon, o MAPI chama o método de logon de cada objeto provedor do provedor de serviços. Para provedores de catálogo de endereços, as chamadas MAPI [IABProvider:: logon](iabprovider-logon.md). Para provedores de repositórios de mensagens, as chamadas MAPI [IMSProvider:: logon](imsprovider-logon.md). Para provedores de transporte, as chamadas MAPI [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md). O MAPI passa um ponteiro para o objeto support apropriado em um dos parâmetros para este método. O método de logon por sua vez cria uma instância de um objeto de logon, passando-o para o ponteiro do objeto support. O objeto logon chama o método **IUnknown:: AddRef** do objeto support para mantê-lo, se necessário. Para obter mais informações sobre o processo de logon para provedores de serviços, consulte [Iniciar um provedor de serviços](starting-a-service-provider.md).
  
Quando um cliente faz logoff, o MAPI chama o método logoff do objeto de logon. O método logoff chama o método **IUnknown:: Release** do objeto support para indicar que o provedor não mais pretende chamar nenhum dos métodos de suporte. Assim como ocorre com o logon, os métodos de logoff têm nomes levemente diferentes. As interfaces [IABLogon](iablogoniunknown.md) e [IMSLogon](imslogoniunknown.md) têm métodos de **logoff** ; a interface [IXPLogon](ixplogoniunknown.md) tem um método [TransportLogoff](ixplogon-transportlogoff.md) . 
  
As funções de ponto de entrada de serviço de mensagens são chamadas quando uma tentativa de logon falha com o erro MAPI_E_UNCONFIGURED ou quando um cliente inicia uma solicitação de configuração. MAPI instancia um objeto de suporte de configuração e chama a função de ponto de entrada do serviço de mensagem para o provedor não configurado ou para o provedor cuja configuração está prestes a ser alterada. Ao contrário dos outros objetos de suporte, os objetos de suporte de configuração só são válidos até que a função de ponto de entrada seja retornada; os serviços de mensagens não chamam os métodos **AddRef** desses objetos para mantê-los. 
  
Normalmente, o MAPI faz chamadas para a função de ponto de entrada de serviço de mensagens de um provedor, mas, às vezes, um provedor é solicitado a fazer a chamada. Isso pode ocorrer quando um cliente chama o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) de um provedor para solicitar que o provedor exiba sua folha de propriedades de configuração. **SettingsDialog** deve chamar [IMAPISupport:: GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) para obter um objeto de suporte de configuração que pode passar para a função de ponto de entrada do serviço de mensagens. 
  
O método [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) está disponível para determinar os endereços das funções de alocação e desalocação de memória sem ter que vincular com MAPI. O uso do **GetMemAllocRoutines** também facilita o rastreamento de vazamentos de memória ao redor das chamadas de função de alocação com o código de depuração. Se você chamar **GetMemAllocRoutines**, como é recomendado, faça isso antes de chamar a função [CreateIProp](createiprop.md) , que requer os endereços da função de alocação como parâmetros. 
  
Quando você precisar criar um novo catálogo de endereços ou um objeto de repositório de mensagens, crie e defina uma chave de pesquisa para o objeto na sua propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Chame [IMAPISupport:: NewUID](imapisupport-newuid.md) para obter um identificador exclusivo a ser usado na criação de uma chave de pesquisa. Não use seu próprio [MAPIUID](mapiuid.md)embutido em código. O **MAPIUID** de um provedor deve ser usado somente para identificadores de entrada. Para obter mais informações sobre como construir chaves de pesquisa, consulte [MAPI Record and Search Keys](mapi-record-and-search-keys.md).
  
Um aplicativo cliente pode, às vezes, liberar um objeto sem liberar um ou mais de seus objetos associados. Nesse caso, um provedor pode precisar renderizar um objeto não-liberado inutilizável. Para fazer isso, o provedor libera todos os recursos conectados ao objeto e, em seguida, chama [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) para invalidar a vtable do objeto. **MakeInvalid** substitui os métodos **IUnknown** da vtable (**QueryInterface**, **ADDREF**e **Release**) por implementações MAPI padrão e faz com que todos os outros métodos retornem MAPI_E_INVALID_OBJECT. O **MakeInvalid** também libera toda a memória do objeto que não a vtable. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviço MAPI](mapi-service-providers.md)

