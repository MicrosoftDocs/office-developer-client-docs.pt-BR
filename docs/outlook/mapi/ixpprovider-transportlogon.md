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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 96e81442125ae49e0c2856a1cf3a97a16d3453cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583334"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece uma sessão em que um aplicativo cliente faz logon em um provedor de transporte. 
  
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

_lpMAPISup_: [in] ponteiro para objeto de suporte do provedor de transporte para funções de retorno de chamada dentro de MAPI para esta sessão. Este objeto permanece válido até que o provedor de transporte libera a ele.
    
_ulUIParam_: [alça para a janela pai de todas as caixas de diálogo ou windows esse método exibe in]. O parâmetro _ulUIParam_ pode ser não-nulo, por exemplo, quando o LOGON_SETUP sinalizar é definida no parâmetro _lpulFlags_ . 
    
_lpszProfileName_: [in] ponteiro para o nome do perfil do usuário. O parâmetro _lpszProfileName_ é usado principalmente quando uma caixa de diálogo deve ser apresentada. 
    
_lpulFlags_: [in, out] Bitmask dos sinalizadores que controla como a sessão de logon é estabelecida. Sinalizadores a seguir podem ser definidos na entrada pelo spooler MAPI:
    
  - LOGON_NO_CONNECT: A conta de usuário está fazendo logon com esse provedor de transporte para fins que não seja de transmissão e recepção de mensagens. O provedor de transporte não deve tentar fazer quaisquer conexões com outros sistemas de mensagens.
        
  - LOGON_NO_DIALOG: Nenhuma caixa de diálogo deve ser exibida, mesmo se as credenciais de usuário que foram salvos no momento são inválidos ou insuficientes para logon.
        
  - LOGON_NO_INBOUND: O provedor de transporte não precisa inicializar para recepção de mensagens e não deve aceitar mensagens de entrada. O MAPI spooler pode usar o método [IXPLogon::TransportNotify](ixplogon-transportnotify.md) posteriormente para sinalizar o provedor de transporte para habilitar o processamento de mensagens de entrada. 
        
  - LOGON_NO_OUTBOUND: O provedor de transporte não tem ao inicializar o envio de mensagens, como o spooler MAPI não fornecerá nenhum. Se um aplicativo cliente requer uma conexão a um provedor remoto durante a composição de uma mensagem para que ele possa fazer chamadas de método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , o provedor de transporte verifique a conexão. O MAPI spooler pode usar **TransportNotify** para sinalizar o provedor de transporte quando começam a saída de operações. 
      
  - MAPI_UNICODE: A sequência no passado para o nome do perfil está no formato Unicode. Se o MAPI\_sinalizador UNICODE não estiver definida, a cadeia de caracteres é no formato ANSI.
      
    Sinalizadores a seguir podem ser definidos em saída pelo provedor de transporte:
      
  - LOGON_SP_IDLE: Solicitações o MAPI spooler frequentemente chamar método de [IXPLogon::Idle](ixplogon-idle.md) do provedor de transporte para o processamento de tempo ocioso. 
      
  - LOGON_SP_POLL: Solicita que o MAPI spooler frequentemente chamar o método [IXPLogon::Poll](ixplogon-poll.md) no objeto retornado de logon para verificar novas mensagens. Se esse sinalizador não estiver definida, o MAPI spooler apenas verifica novas mensagens quando o provedor de transporte usa o método [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) para notificar o spooler que não existem novas mensagens para processar. Um provedor de transporte se torna efetivamente somente enviar, não definindo esse sinalizador e por não notificar o MAPI spooler de recebimento da mensagem. 
      
  - LOGON_SP_RESOLVE: Solicitações que resolve o MAPI spooler total endereços de todos os endereços de mensagem para destinatários não suportados por este provedor de transporte. Portanto, se o provedor de transporte pode construir um caminho de resposta para todos os destinatários.
      
  - MAPI_UNICODE: As cadeias de caracteres retornadas na estrutura de [MAPIERROR](mapierror.md) , se houver, estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
_lppMAPIError_: [out] ponteiro para um ponteiro para a estrutura **MAPIERROR** retornado, se houver, que contém informações de versão, componente e contexto para o erro. O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar. 
    
_lppXPLogon_: [out] ponteiro para o ponteiro para o objeto de logon do provedor de transporte retornado.
    
## <a name="return-value"></a>Valor retornado

S_OK: A chamada foi bem-sucedida e retornou o valor esperado ou os valores.
    
MAPI_E_FAILONEPROVIDER: Este provedor não pode fazer logon, mas esse erro não deve desabilitar o serviço. 
    
MAPI_E_UNCONFIGURED: O perfil não conter informações suficientes para que o logon seja concluída. MAPI chama a função de ponto de entrada do serviço de mensagem do provedor.
    
MAPI_E_UNKNOWN_CPID: O provedor não oferece suporte a página de código do cliente.
    
MAPI_E_UNKNOWN_LCID: O provedor não oferece suporte a informações de localidade do cliente.
    
MAPI_E_USER_CANCEL: O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método **IXPProvider::TransportLogon** para estabelecer uma sessão de logon para um usuário. 
  
A maioria dos provedores de transporte use o método de [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) fornecido com o objeto de suporte apontado pelo parâmetro _lpMAPISup_ para salvar e recuperar informações de identidade do usuário, os endereços de servidor e credenciais. Usando o **OpenProfileSection**, um provedor de transporte pode salvar informações arbitrárias e associá-lo a um logon para um determinado recurso. Por exemplo, um provedor pode usar **OpenProfileSection** para salvar o nome da conta e a senha associada a uma determinada sessão e quaisquer nomes de servidor ou outras informações necessárias que são necessárias para acessar os recursos para a sessão. MAPI oculta informações associadas a um recurso contra o acesso externo. Seção de perfil e torná-los disponível por meio de _lpMAPISup_ é gerenciada pelo spooler MAPI para que dados relacionados nesse contexto do usuário são separados da dados para outros contextos. 
  
O provedor de transporte deve chamar o método **AddRef** no objeto suporte e manter uma cópia do ponteiro para este objeto como parte do objeto de logon do provedor. 
  
O nome de exibição de perfil no _lpszProfileName_ é fornecido para que o provedor de transporte possa ser usado em caixas de diálogo de logon ou mensagens de erro. Se o provedor retém esse nome, ele deve ser copiado para o armazenamento alocado pelo provedor. 
  
Talvez seja necessário fazer trabalho adicional no logon para estabelecer as credenciais de uma boa necessárias para operações entre provedores complementares provedores de transporte que estejam intimamente ligadas a outros provedores de serviços.
  
Geralmente, os provedores de transporte são abertos quando o usuário fizer logon pela primeira vez a um perfil. Porque o primeiro logon para um perfil, portanto, geralmente vem antes do logon em qualquer armazenamento de mensagem, o MAPI spooler geralmente chama **TransportLogon** com os LOGON_NO_INBOUND LOGON_NO_OUTBOUND sinalizadores e definir no _lpulFlags_. Posteriormente, quando os repositórios de mensagem apropriada estão disponíveis na sessão de perfil, o MAPI spooler chama **TransportNotify** para iniciar as operações de entrada e saídas para o provedor de transporte. 
  
Passando o sinalizador LOGON_NO_CONNECT os sinais de _lpulFlags_ operação offline do provedor de transporte. Este sinalizador indica que nenhuma conexões externas devem ser feitas; Se o provedor de transporte não é possível estabelecer uma sessão sem uma conexão externa, ele deverá retornar um valor de erro para o logon. 
  
Um provedor de transporte deve definir o sinalizador LOGON_SP_IDLE em _lpulFlags_ em tempo de inicialização se ele foi projetado para usar o tempo que o sistema caso contrário gasta ocioso. Esse período é frequentemente usado para lidar com operações automáticas, como download, automática de mensagens atingiu o tempo mensagem Baixando ou atingiu o tempo de envio da mensagem. Se esse sinalizador estiver definido, o MAPI spooler chama **ocioso** quando ocorre de tempo ocioso do sistema iniciar essas operações. O MAPI spooler não chamar **ocioso** em intervalos definidos; em vez disso, ele é chamado somente durante o tempo ocioso true. Portanto, os provedores não devem funcionar em qualquer pressuposição sobre frequência seus métodos **Idle** serão chamados. Os provedores que suportam as operações de tempo ocioso devem fornecer uma interface de usuário de configuração para ele na sua folha de propriedades do provedor. 
  
Se o logon do provedor de transporte for bem sucedido, o provedor deve retornar no parâmetro _lppXPLogon_ um ponteiro para um objeto de logon. O MAPI spooler usarão este objeto para acesso do provedor adicionais. Se **TransportLogon** exibe uma caixa de diálogo de logon e o usuário cancela logon normalmente clicando no botão **Cancelar** na caixa de diálogo o provedor deve retornar MAPI_E_USER_CANCEL. 
  
Para a maioria dos valores de erro retornado da **TransportLogon**, MAPI desabilita os serviços de mensagem ao qual o provedor pertence. MAPI não chamará qualquer provedor que pertencem a esse serviço para o restante da sessão MAPI. Por outro lado, quando **TransportLogon** retorna o valor de erro MAPI_E_FAILONEPROVIDER de seu logon, MAPI não desabilite o serviço de mensagem ao qual o provedor pertence. **TransportLogon** deve retornar MAPI_E_FAILONEPROVIDER se encontra um erro dizendo que não garantem a desabilitação do serviço para o restante da sessão. 
  
Se um provedor retorna MAPI_E_UNCONFIGURED de seu logon, MAPI será chamada de função de entrada de serviço de mensagem do provedor e tente novamente o logon. MAPI passa MSG_SERVICE_CONFIGURE como contexto, para fornecer o serviço a oportunidade de se configurar. Se o cliente tiver escolhido permitir que uma interface de usuário de fazer logon, o serviço pode representar sua folha de propriedades de configuração para que o usuário pode digitar informações de configuração. 
  
Se o provedor localiza que todas as informações necessárias não estão no perfil, ele deverá retornar MAPI_E_UNCONFIGURED para que a função de ponto de entrada do serviço de mensagem do provedor chamadas de MAPI. 
  
## <a name="see-also"></a>Confira também

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

