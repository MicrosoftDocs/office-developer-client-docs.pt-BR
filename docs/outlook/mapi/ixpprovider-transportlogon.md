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
  
Estabelece uma sessão na qual um aplicativo cliente faz o login em um provedor de transporte. 
  
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

_lpMAPISup_: [in] Ponteiro para o objeto de suporte do provedor de transporte para funções de retorno de chamada no MAPI para esta sessão. Esse objeto permanece válido até que o provedor de transporte o libere.
    
_ulUIParam_: [in] Manipular a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. O _parâmetro ulUIParam_ pode ser não nulo, por exemplo, quando o sinalizador LOGON_SETUP é definido no parâmetro _lpulFlags._ 
    
_lpszProfileName_: [in] Ponteiro para o nome de perfil do usuário. O  _parâmetro lpszProfileName_ é usado principalmente quando uma caixa de diálogo deve ser apresentada. 
    
_lpulFlags_: [in, out] Bitmask de sinalizadores que controla como a sessão de logon é estabelecida. Os sinalizadores a seguir podem ser definidos na entrada pelo spooler MAPI:
    
  - LOGON_NO_CONNECT: a conta de usuário está fazendo logon nesse provedor de transporte para fins que não são de transmissão e recepção de mensagens. O provedor de transporte não deve tentar fazer conexões com outros sistemas de mensagens.
        
  - LOGON_NO_DIALOG: nenhuma caixa de diálogo deverá ser exibida mesmo se as credenciais de usuário salvas no momento são inválidas ou insuficientes para logon.
        
  - LOGON_NO_INBOUND: o provedor de transporte não precisa inicializar para recebimento de mensagens e não deve aceitar mensagens de entrada. O spooler MAPI pode usar o [método IXPLogon::TransportNotify](ixplogon-transportnotify.md) posteriormente para sinalizar o provedor de transporte para habilitar o processamento de mensagens de entrada. 
        
  - LOGON_NO_OUTBOUND: o provedor de transporte não precisa inicializar o envio de mensagens, pois o spooler MAPI não fornece nenhum. Se um aplicativo cliente exigir uma conexão com um provedor remoto durante a composição de uma mensagem para que possa fazer chamadas de método [IXPLogon::AddressTypes,](ixplogon-addresstypes.md) o provedor de transporte deverá fazer a conexão. O spooler MAPI pode usar **TransportNotify** para sinalizar o provedor de transporte quando as operações de saída podem começar. 
      
  - MAPI_UNICODE: a cadeia de caracteres passada para o nome do perfil está no formato Unicode. Se o sinalizador \_ UNICODE MAPI não estiver definido, a cadeia de caracteres está no formato ANSI.
      
    Os sinalizadores a seguir podem ser definidos na saída pelo provedor de transporte:
      
  - LOGON_SP_IDLE: solicita que o spooler MAPI frequentemente chame o método [IXPLogon::Idle](ixplogon-idle.md) do provedor de transporte para processamento de tempo ocioso. 
      
  - LOGON_SP_POLL: solicita que o spooler MAPI frequentemente chame o método [IXPLogon::P oll](ixplogon-poll.md) no objeto de logon retornado para verificar se há novas mensagens. Se esse sinalizador não estiver definido, o spooler MAPI só verificará se há novas mensagens quando o provedor de transporte usar o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) para notificar o spooler de que há novas mensagens a processar. Um provedor de transporte efetivamente se torna somente de envio não definindo esse sinalizador e notificando o spooler MAPI do recebimento de mensagens. 
      
  - LOGON_SP_RESOLVE: solicita que o spooler MAPI resolva para endereços completos todos os endereços de mensagem para destinatários não suportados por esse provedor de transporte. Portanto, o provedor de transporte pode construir um caminho de resposta para todos os destinatários.
      
  - MAPI_UNICODE: as cadeias de caracteres retornadas na [estrutura MAPIERROR,](mapierror.md) se alguma, estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
_lppMAPIError_: [out] Ponteiro para um ponteiro para a estrutura **MAPIERROR** retornada, se alguma, que contenha informações de versão, componente e contexto para o erro. O  _parâmetro lppMAPIError_ pode ser definido como NULL se não houver **estrutura MAPIERROR** a ser retornada. 
    
_lppXPLogon_: [out] Ponteiro para o ponteiro para o objeto de logon do provedor de transporte retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK: a chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_FAILONEPROVIDER: este provedor não pode fazer logoff, mas esse erro não deve desabilitar o serviço. 
    
MAPI_E_UNCONFIGURED: o perfil não contém informações suficientes para que o logon seja concluído. O MAPI chama a função de ponto de entrada do serviço de mensagens do provedor.
    
MAPI_E_UNKNOWN_CPID: o provedor não pode suportar a página de código do cliente.
    
MAPI_E_UNKNOWN_LCID: o provedor não pode suportar as informações de localidade do cliente.
    
MAPI_E_USER_CANCEL: o usuário cancelou a operação, normalmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o **método IXPProvider::TransportLogon** para estabelecer uma sessão de logon para um usuário. 
  
A maioria dos provedores de transporte usa o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) fornecido com o objeto de suporte apontado pelo parâmetro  _lpMAPISup_ para salvar e recuperar informações de identidade do usuário, endereços de servidor e credenciais. Usando **OpenProfileSection**, um provedor de transporte pode salvar informações arbitrárias e associá-la a um logon em um recurso específico. Por exemplo, um provedor pode usar **OpenProfileSection** para salvar o nome da conta e a senha associados a uma sessão específica e quaisquer nomes de servidor ou outras informações necessárias para acessar os recursos dessa sessão. O MAPI oculta as informações associadas a um recurso de acesso externo. A seção de perfil disponibilizada por meio de  _lpMAPISup_ é gerenciada pelo spooler MAPI para que os dados relacionados a esse contexto de usuário são separados dos dados de outros contextos. 
  
O provedor de transporte deve chamar o método **IUnknown::AddRef** no objeto de suporte e manter uma cópia do ponteiro para esse objeto como parte do objeto de logon do provedor. 
  
O nome de exibição de perfil  _em lpszProfileName_ é fornecido para que o provedor de transporte possa usá-lo em mensagens de erro ou caixas de diálogo de logon. Se o provedor reter esse nome, ele deverá ser copiado para o armazenamento alocado pelo provedor. 
  
Os provedores de transporte que estão fortemente juntos com outros provedores de serviços podem precisar fazer trabalho adicional no logon para estabelecer as boas credenciais necessárias para operações entre provedores complementares.
  
Normalmente, os provedores de transporte são abertos quando o usuário faz o logor pela primeira vez em um perfil. Como o primeiro logon em um perfil, portanto, geralmente vem antes do logon em qualquer armazenamento de mensagens, o spooler MAPI geralmente chama **TransportLogon** com os sinalizadores LOGON_NO_INBOUND e LOGON_NO_OUTBOUND definidos em  _lpulFlags_. Posteriormente, quando os armazenamentos de mensagens apropriados estão disponíveis na sessão de perfil, o spooler MAPI chama **TransportNotify** para iniciar operações de entrada e saída para o provedor de transporte. 
  
Passar o LOGON_NO_CONNECT sinalizador em  _lpulFlags_ sinaliza a operação offline do provedor de transporte. Esse sinalizador indica que nenhuma conexão externa deve ser feita; se o provedor de transporte não puder estabelecer uma sessão sem uma conexão externa, ele deverá retornar um valor de erro para o logon. 
  
Um provedor de transporte deve definir o LOGON_SP_IDLE de transporte em  _lpulFlags_ no momento da inicialização se ele for projetado para usar o tempo que o sistema gasta ocioso. Esse tempo costuma ser usado para lidar com operações automáticas, como download automático de mensagens, download de mensagens com tempo ou envio de mensagem com tempo. Se esse sinalizador estiver definido, o spooler MAPI chamará **Idle** quando o tempo ocioso do sistema ocorrer para iniciar essas operações. O spooler MAPI não chama **Idle** em intervalos definidos; em vez disso, ele é chamado somente durante o tempo ocioso real. Portanto, os provedores não devem trabalhar em qualquer suposição sobre a frequência com que seus métodos **Idle** serão chamados. Provedores que suportam operações de tempo ocioso devem fornecer uma interface de usuário de configuração para ela em sua folha de propriedades do provedor. 
  
Se o logon do provedor de transporte for bem-sucedido, o provedor deverá retornar no parâmetro  _lppXPLogon_ um ponteiro para um objeto de logon. O spooler MAPI usará esse objeto para acesso de provedor adicional. Se **TransportLogon** exibir uma caixa de diálogo de logon e o  usuário cancelar o logon normalmente clicando no botão Cancelar na caixa de diálogo, o provedor deverá retornar MAPI_E_USER_CANCEL. 
  
Para a maioria dos valores de erro **retornados de TransportLogon**, o MAPI desabilita os serviços de mensagem aos quais o provedor pertence. O MAPI não chamará nenhum provedor que pertença a esse serviço para o restante da sessão MAPI. Por outro lado, quando **TransportLogon** retorna o MAPI_E_FAILONEPROVIDER de erro de seu logon, o MAPI não desabilita o serviço de mensagens ao qual o provedor pertence. **TransportLogon** deve retornar MAPI_E_FAILONEPROVIDER se encontrar um erro que não garante a desabilitação do serviço para o restante da sessão. 
  
Se um provedor retornar MAPI_E_UNCONFIGURED de seu logon, o MAPI chamará a função de entrada do serviço de mensagens do provedor e repetirá o logon. O MAPI MSG_SERVICE_CONFIGURE como contexto, para dar ao serviço uma chance de se configurar. Se o cliente tiver optado por permitir uma interface do usuário no logon, o serviço poderá apresentar sua folha de propriedades de configuração para que o usuário possa inserir informações de configuração. 
  
Se o provedor achar que todas as informações necessárias não estão no perfil, ele deverá retornar MAPI_E_UNCONFIGURED para que o MAPI chama a função de ponto de entrada do serviço de mensagens do provedor. 
  
## <a name="see-also"></a>Confira também

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

