---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 53b2733dbf38d680027dc00ecf5513f384e46660
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417305"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece uma sessão na qual um aplicativo cliente faz logon em um provedor de transporte. 
  
```cpp
HRESULT TransportLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG FAR * lpulFlags,
  LPMAPIERROR FAR * lppMAPIError,
  LPXPLOGON FAR * lppXPLogon
);
```

## <a name="parameters"></a>Parâmetros

_lpMAPISup_: [in] ponteiro para o objeto support do provedor de transporte para funções de retorno de chamada no MAPI para esta sessão. Este objeto permanece válido até que o provedor de transporte o libere.
    
_ulUIParam_: [in] Handle para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido. O parâmetro _ulUIParam_ pode ser não nulo, por exemplo, quando o sinalizador LOGON_SETUP é definido no parâmetro _lpulFlags_ . 
    
_lpszProfileName_: [in] ponteiro para o nome do perfil do usuário. O parâmetro _lpszProfileName_ é usado principalmente quando uma caixa de diálogo deve ser apresentada. 
    
_lpulFlags_: [in, out] bitmask de sinalizadores que controlam como a sessão de logon é estabelecida. Os seguintes sinalizadores podem ser definidos na entrada pelo spooler MAPI:
    
  - LOGON_NO_CONNECT: a conta de usuário está fazendo logon no provedor de transporte para fins diferentes de transmissão e recebimento de mensagens. O provedor de transporte não deve tentar fazer conexões com outros sistemas de mensagens.
        
  - LOGON_NO_DIALOG: nenhuma caixa de diálogo deve ser exibida, mesmo que as credenciais de usuário salvas no momento sejam inválidas ou insuficientes para logon.
        
  - LOGON_NO_INBOUND: o provedor de transporte não precisa inicializar a recepção de mensagens e não deve aceitar mensagens de entrada. O MAPI spooler pode usar o método [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) posteriormente para sinalizar o provedor de transporte para habilitar o processamento de mensagens de entrada. 
        
  - LOGON_NO_OUTBOUND: o provedor de transporte não precisa ser inicializado para enviar mensagens, pois o spooler MAPI não fornece nenhum. Se um aplicativo cliente requer uma conexão com um provedor remoto durante a composição de uma mensagem para que possa fazer chamadas de método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) , o provedor de transporte deve fazer a conexão. O MAPI spooler pode usar o **TransportNotify** para sinalizar o provedor de transporte quando as operações de saída podem começar. 
      
  - MAPI_UNICODE: a cadeia de caracteres passada para o nome do perfil está no formato Unicode. Se o sinalizador\_de MAPI Unicode não estiver definido, a cadeia de caracteres estará no formato ANSI.
      
    Os seguintes sinalizadores podem ser definidos na saída pelo provedor de transporte:
      
  - LOGON_SP_IDLE: solicita que o spooler MAPI chame com frequência o método de ociosidade do provedor de transporte [IXPLogon:: Idle](ixplogon-idle.md) para processamento em tempo ocioso. 
      
  - LOGON_SP_POLL: solicita que o spooler MAPI chame com frequência o método [IXPLogon::P oll](ixplogon-poll.md) no objeto de logon retornado para verificar se há novas mensagens. Se esse sinalizador não for definido, o spooler MAPI só verificará novas mensagens quando o provedor de transporte usar o método [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) para notificar o spooler de que há novas mensagens a serem processadas. Um provedor de transporte se torna somente envio por não definir esse sinalizador e não notifica o spooler MAPI de recebimento de mensagens. 
      
  - LOGON_SP_RESOLVE: solicita que o spooler MAPI resolva para endereços completos todos os endereços de mensagens para destinatários não suportados por este provedor de transporte. Portanto, o provedor de transporte pode construir um caminho de resposta para todos os destinatários.
      
  - MAPI_UNICODE: as cadeias de caracteres retornadas na estrutura [MAPIERROR](mapierror.md) , se houver, estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
_lppMAPIError_: [out] ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada, se houver, que contenham informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada. 
    
_lppXPLogon_: [out] ponteiro para o ponteiro para o objeto de logon do provedor de transporte retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK: a chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_FAILONEPROVIDER: este provedor não pode fazer logon, mas esse erro não deve desabilitar o serviço. 
    
MAPI_E_UNCONFIGURED: o perfil não contém informações suficientes para que o logon seja concluído. MAPI chama a função de ponto de entrada do serviço de mensagens do provedor.
    
MAPI_E_UNKNOWN_CPID: o provedor não pode dar suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID: o provedor não oferece suporte às informações de localidade do cliente.
    
MAPI_E_USER_CANCEL: o usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPProvider:: TransportLogon** para estabelecer uma sessão de logon para um usuário. 
  
A maioria dos provedores de transporte usa o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) fornecido com o objeto support apontado pelo parâmetro _lpMAPISup_ para salvar e recuperar informações de identidade de usuário, endereços de servidor e credenciais. Usando o **OpenProfileSection**, um provedor de transporte pode salvar informações arbitrárias e associá-las a um determinado recurso. Por exemplo, um provedor pode usar o **OpenProfileSection** para salvar o nome da conta e a senha associados a uma determinada sessão e quaisquer nomes de servidor ou outras informações necessárias para acessar os recursos dessa sessão. MAPI oculta informações associadas a um recurso de fora do Access. A seção de perfil disponibilizada por meio do _lpMAPISup_ é gerenciada pelo spooler MAPI, de modo que os dados relacionados a esse contexto de usuário são separados dos dados de outros contextos. 
  
O provedor de transporte deve chamar o método **IUnknown:: AddRef** no objeto support e manter uma cópia do ponteiro para este objeto como parte do objeto de logon do provedor. 
  
O nome de exibição do perfil no _lpszProfileName_ é fornecido para que o provedor de transporte possa usá-lo nas mensagens de erro ou nas caixas de diálogo de logon. Se o provedor mantiver esse nome, ele deve ser copiado para o armazenamento alocado pelo provedor. 
  
Os provedores de transporte que estão rigidamente acoplados a outros provedores de serviços podem ter que realizar trabalho adicional no logon para estabelecer as boas credenciais necessárias para operações entre os provedores complementares.
  
Normalmente, os provedores de transporte são abertos quando o usuário faz logon pela primeira vez em um perfil. Como o primeiro logon em um perfil, portanto, geralmente vem antes do logon em qualquer repositório de mensagens, o spooler MAPI normalmente chama **TransportLogon** com os sinalizadores LOGON_NO_INBOUND e LOGON_NO_OUTBOUND definidos no _lpulFlags_. Posteriormente, quando os repositórios de mensagens apropriados estiverem disponíveis na sessão de perfil, o spooler MAPI chamará o **TransportNotify** para iniciar as operações de entrada e saída para o provedor de transporte. 
  
Passar o sinalizador LOGON_NO_CONNECT no _lpulFlags_ sinaliza a operação offline do provedor de transporte. Este sinalizador indica que nenhuma conexão externa deve ser feita; Se o provedor de transporte não puder estabelecer uma sessão sem uma conexão externa, ele deverá retornar um valor de erro para o logon. 
  
Um provedor de transporte deve definir o sinalizador LOGON_SP_IDLE no _lpulFlags_ no momento da inicialização, caso tenha sido projetado para usar o tempo em que o sistema, caso contrário, gastará ocioso. Essa hora é freqüentemente usada para lidar com operações automáticas, como download automático de mensagens, download de mensagens com tempo, ou envio de mensagens com tempo. Se esse sinalizador estiver definido, o spooler MAPI chamará **ocioso** quando o tempo ocioso do sistema ocorrer para iniciar essas operações. O spooler MAPI não chama **Idle** em intervalos definidos; em vez disso, ele é chamado somente durante o tempo ocioso real. Portanto, os provedores não devem funcionar em qualquer pressuposição da frequência **** com que seus métodos ociosos serão chamados. Os provedores que oferecem suporte a operações de tempo ocioso devem fornecer uma interface de usuário de configuração para ele na folha de propriedades do provedor. 
  
Se o logon do provedor de transporte tiver êxito, o provedor deverá retornar o parâmetro _lppXPLogon_ um ponteiro para um objeto logon. O spooler MAPI usará esse objeto para acesso de provedor adicional. Se **TransportLogon** exibe uma caixa de diálogo de logon e o usuário cancela o logon normalmente clicando no botão **Cancelar** na caixa de diálogo o provedor deve retornar MAPI_E_USER_CANCEL. 
  
Para a maioria dos valores de erro retornados de **TransportLogon**, o MAPI desabilita os serviços de mensagens aos quais o provedor pertence. O MAPI não chamará nenhum provedor que pertença a esse serviço para o restante da sessão MAPI. Por outro lado, quando **TransportLogon** retorna o valor de erro MAPI_E_FAILONEPROVIDER de seu logon, MAPI não desabilita o serviço de mensagens ao qual o provedor pertence. **TransportLogon** deve retornar MAPI_E_FAILONEPROVIDER se encontrar um erro que não garante a desabilitação do serviço para o restante da sessão. 
  
Se um provedor retornar MAPI_E_UNCONFIGURED de seu logon, o MAPI chamará a função de entrada do serviço de mensagens do provedor e, em seguida, repetirá o logon. O MAPI passa MSG_SERVICE_CONFIGURE como o contexto, para dar ao serviço uma oportunidade de se configurar. Se o cliente optou por permitir uma interface de usuário no logon, o serviço pode apresentar sua folha de propriedades de configuração para que o usuário possa inserir informações de configuração. 
  
Se o provedor descobrir que todas as informações necessárias não estão no perfil, ele deve retornar MAPI_E_UNCONFIGURED para que o MAPI chame a função de ponto de entrada do serviço de mensagem do provedor. 
  
## <a name="see-also"></a>Confira também

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

