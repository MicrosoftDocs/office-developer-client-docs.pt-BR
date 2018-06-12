---
title: Visão geral do objeto de suporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5b062891-39ab-4334-9706-5b376719d5e4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ecc5439b4abbbfd920fba5456db7462f7967388f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770514"
---
# <a name="support-object-overview"></a>Visão geral do objeto de suporte

  
  
**Aplica-se a**: Outlook 
  
MAPI representa um objeto de suporte, um objeto que implementa o [IMAPISupport: IUnknown](imapisupportiunknown.md) interface, para todos os provedores de serviço durante o logon e para todos os serviços de mensagem durante a configuração. 
  
Objetos de suporte não estão acessíveis por clientes; eles são implementados pelo MAPI e chamados apenas por provedores de serviços. A interface **IMAPISupport** é especificada no arquivo de cabeçalho Mapispi.h. Seu identificador é IID_IMAPISup e seu tipo de ponteiro é LPMAPISUP. Sem propriedades MAPI são expostas pelos objetos de suporte. 
  
Um provedor pode ser fornecido como um ou mais objetos de suporte, dependendo o número de vezes que MAPI faz o provedor de logon ou o número de vezes que é chamada de função de entrada de serviço de mensagem do provedor. Normalmente, um provedor será registrado pelo menos uma vez por sessão. Provedores de transporte e o catálogo de endereço estão conectados toda vez que um cliente inicia uma sessão com uma entrada de perfil que solicita-los. Provedores de armazenamento de mensagem são registradas toda vez que um cliente chama o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
  
No caso de vários logons em uma sessão, você pode escolher tanto de reter e usar a cada objeto de suporte separadamente ou de reter e usar somente o primeiro, descartar cada objeto de suporte subsequentes. Para manter um objeto de suporte, chame seu método de **AddRef** . Chamar **AddRef** em um objeto de suporte que você deseja reter durante uma sessão é extremamente importante; Se a chamada não for feita, o MAPI libera o objeto de suporte e libera sua memória. 
  
A finalidade do objeto suporte é fornecer implementações para um grande número de métodos normalmente usados pelos provedores. Cada objeto de suporte também contém dados contextuais específicos para sua própria instância, como a sessão que o provedor está sendo executado no, a seção de perfil, que o provedor está usando e informações de erro para a sessão. 
  
Há quatro tipos diferentes de objetos de suporte: uma para cada tipo de provedor principais (catálogo de endereços, repositório de mensagem e transporte) e outra para suporte de configuração. 
  
MAPI personaliza a cada objeto de suporte, incluindo implementações dos métodos que são relevantes para o seu uso. Implementações de alguns métodos, como [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md), estão incluídas em todos os objetos de suporte. Implementações de outros métodos, como [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md), aplicam-se somente aos objetos de suporte específico. Somente o repositório de mensagens e os provedores de transporte podem usar esse método; Quando um provedor de catálogo de endereços ou de um serviço de mensagem tente chamá-lo, MAPI retorna MAPI_E_NO_SUPPORT.
  
Objetos de suporte podem ser usados para realizar várias tarefas, como o seguinte:
  
- Acessando uma seção de perfil.
    
- Copiar pastas ou mensagens. Para obter mais informações, consulte [copiar ou mover uma mensagem ou uma pasta](copying-or-moving-a-message-or-a-folder.md).
    
- Acessando os objetos que pertencem a outros provedores. Para obter mais informações, consulte [comparação e acesso a objetos com suporte](supporting-object-access-and-comparison.md). 
    
- Manipulação de notificação de evento. Para obter mais informações, consulte [Suporte a notificação de evento](supporting-event-notification.md).
    
- Alocar e liberar memória.
    
- Obtendo um identificador exclusivo.
    
- A invalidação de objetos.
    
- Tratamento de erros.
    
- Registrando pré-processador de mensagem. 
    
- Preparando os relatórios de entrega de mensagem. 
    
Ao fazer logon, MAPI chama o método de logon do objeto de provedor de cada provedor de serviço. Para provedores de catálogo de endereços, MAPI chama [IABProvider::Logon](iabprovider-logon.md). Para provedores de repositório de mensagem, MAPI chama [IMSProvider::Logon](imsprovider-logon.md). Para provedores de transporte, MAPI chama [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). MAPI passa um ponteiro para o objeto de suporte apropriado em um dos parâmetros a este método. Por sua vez, o método logon instancia um objeto de logon, passando-lhe o ponteiro de objeto de suporte. O objeto de logon chama o suporte ao método do objeto **AddRef** para mantê-la, se necessário. Para obter mais informações sobre o processo de logon para provedores de serviços, consulte [Iniciando um provedor de serviços](starting-a-service-provider.md).
  
Quando um cliente fizer logoff, MAPI chama o método de logoff do objeto logon. O método logoff chama o suporte ao método do objeto **IUnknown:: Release** para indicar que o provedor não são mais pretende chamar qualquer um dos métodos de suporte. Assim como acontece com o logon, os métodos de logoff têm nomes ligeiramente diferentes. As interfaces [IABLogon](iablogoniunknown.md) e [IMSLogon](imslogoniunknown.md) possuem métodos de **Logoff** ; a interface de [IXPLogon](ixplogoniunknown.md) tem um método [TransportLogoff](ixplogon-transportlogoff.md) . 
  
Funções de ponto de entrada de serviço de mensagem são chamadas quando uma tentativa de logon falha com o erro MAPI_E_UNCONFIGURED ou quando um cliente inicia uma solicitação de configuração. MAPI instancia um objeto de configuração de suporte e chama a função de ponto de entrada de serviço de mensagem para o provedor não configurado ou o provedor cuja configuração está prestes a ser alterada. Ao contrário de outros objetos de suporte, objetos de configuração de suporte são válidos até o ponto de entrada a função retorna; Serviços de mensagem não chamar métodos de **AddRef** desses objetos para mantê-los. 
  
Normalmente, MAPI faz chamadas para a função do ponto de entrada do provedor, uma mensagem serviço, mas, em alguns casos, um provedor é solicitado a fazer a chamada. Isso pode ocorrer quando um cliente chama o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) de um provedor para solicitar o provedor para exibir sua folha de propriedades de configuração. **SettingsDialog** deve chamar [IMAPISupport::GetSvcConfigSupportObj](imapisupport-getsvcconfigsupportobj.md) para obter um objeto de suporte de configuração que ele pode passar para a função de ponto de entrada de serviço de mensagem. 
  
O método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) está disponível para determinar os endereços das funções de memória alocação e desalocação sem ter que deseja estabelecer um vínculo com MAPI. Usar **GetMemAllocRoutines** também facilita rastrear o vazamento de memória, envolvendo as chamadas de função de alocação com código de depuração. Se você chamar **GetMemAllocRoutines**, conforme é recomendado, fazê-lo antes de chamar a função [CreateIProp](createiprop.md) , que requer os endereços de função de alocação como parâmetros. 
  
Quando você precisar criar um novo catálogo de endereços ou mensagem armazenar objeto, crie e defina uma chave de pesquisa para o objeto em sua propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Chame [IMAPISupport::NewUID](imapisupport-newuid.md) para obter um identificador exclusivo a serem usados na criação de uma chave de pesquisa. Não use seu próprio codificadas [MAPIUID](mapiuid.md). De um provedor **MAPIUID** deve ser usado apenas para os identificadores de entrada. Para obter mais informações sobre a construção de chaves de pesquisa, consulte [MAPI registro e chaves de pesquisa](mapi-record-and-search-keys.md).
  
Um aplicativo cliente em alguns casos, pode liberar um objeto sem liberar um ou mais dos seus objetos afiliados. Nesse caso, talvez seja necessário um provedor inutilizar um objeto não lançado. Para fazer isso, o provedor libera todos os recursos conectados com o objeto e, em seguida, chama [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) para invalidar vtable do objeto. **MakeInvalid** substitui os métodos de **IUnknown** do vtable (**QueryInterface**, **AddRef**e **Release**) com implementações de MAPI padrão e faz com que todos os outros métodos retornar MAPI_E_INVALID_OBJECT. **MakeInvalid** também libera a memória de todos os objetos que não seja o vtable. 
  
## <a name="see-also"></a>Confira também



[Provedores de serviços MAPI](mapi-service-providers.md)

