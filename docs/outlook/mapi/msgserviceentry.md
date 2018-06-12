---
title: MSGSERVICEENTRY
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MSGSERVICEENTRY
api_type:
- COM
ms.assetid: 655774a6-588c-44c7-903b-4497b7eccbc2
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 9af170f3445757eb96b9fe78c7cbea2c29ef4612
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768165"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Aplica-se a**: Outlook 
  
Define um protótipo para uma função de ponto de entrada de serviço mensagens oferecer suporte a configuração do serviço de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
|Função definido implementada por:  <br/> |Serviços de mensagens  <br/> |
|Função definido chamada pelo:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT MSGSERVICEENTRY(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulContext,
  ULONG cValues,
  LPSPropValue lpProps,
  LPPROVIDERADMIN lpProviderAdmin,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Par�metros

 _hInstance_
  
> [in] Identificador da instância do providerDLL serviço. A alça geralmente é usada para recuperar recursos. 
    
 _lpMalloc_
  
> [in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** . O serviço de mensagem, talvez seja necessário usar esse método de alocação ao trabalhar com certas interfaces como **IStream**. 
    
 _lpMAPISup_
  
> [in] Ponteiro para uma [IMAPISupport: IUnknown](imapisupportiunknown.md) implementação de interface. 
    
 _ulUIParam_
  
> [in] Um valor específico de implementação usado para passar as informações de interface de usuário para uma função ou zero. O parâmetro _ulUIParam_ é o identificador da janela pai para a caixa de diálogo de configuração e do tipo HWND (cast para um ULONG_PTR). Um valor de zero indica que não há nenhuma janela pai. 
    
 _ulFlags_
  
> [in] Bitmask dos sinalizadores indicando opções para a função de entrada de serviço. Sinalizadores a seguir podem ser definidos:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> Interface do usuário de configuração do serviço deve exibir a configuração atual, mas não permitir que o usuário alterá-lo. 
    
SERVICE_UI_ALLOWED 
  
> Permite que uma caixa de diálogo de configuração a ser exibido, se necessário. Quando o sinalizador SERVICE_UI_ALLOWED é definido, a caixa de diálogo deve ser exibida apenas se a matriz de valores de propriedade _lpProps_ está vazia ou não contiver uma configuração válida. Se SERVICE_UI_ALLOWED não estiver definida, uma caixa de diálogo ainda pode exibida se o sinalizador SERVICE_UI_ALWAYS está definido. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Solicita que a caixa de diálogo de configuração para o provedor ativa ser exibida na parte superior de outras caixas de diálogo. 
    
SERVICE_UI_ALWAYS 
  
> Requer o serviço de mensagem para exibir uma caixa de diálogo de configuração. Se o sinalizador SERVICE_UI_ALWAYS não estiver definido, uma caixa de diálogo Configuração ainda pode exibida se o sinalizador SERVICE_UI_ALLOWED está definido e as informações de configuração válida não estão disponíveis da matriz de valores de propriedade _lpProps_ . SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS deve ser definida para permitir que uma interface de usuário a ser exibido. 
    
 _ulContext_
  
> [in] A operação de configuração que MAPI está atualmente executando. O parâmetro _ulContext_ conterá um dos seguintes valores: 
    
MSG_SERVICE_CONFIGURE 
  
> Alterações na configuração do serviço devem ser feitas no perfil. Se o sinalizador SERVICE_UI_ALWAYS estiver definido, o serviço deve exibir sua caixa de diálogo de configuração. A caixa de diálogo também deve ser exibida se o sinalizador SERVICE_UI_ALLOWED está definido e o parâmetro _lpProps_ está vazio ou não contém dados de configuração válida. Se _lpProps_ contém dados válidos, nenhuma caixa de diálogo deve ser exibida e o serviço deve usar esses dados para tornar a alteração de configuração. 
    
MSG_SERVICE_CREATE 
  
> O serviço está sendo adicionado a um perfil. Se o SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED sinalizador estiver definido, o serviço deve exibir sua caixa de diálogo de configuração. Se nenhum dos sinalizadores estiver definida, o serviço deve falhar. 
    
MSG_SERVICE_DELETE 
  
> O serviço está sendo removido de um perfil. Após receber esse evento, o serviço deve retornar S_OK.
    
MSG_SERVICE_INSTALL 
  
> O serviço foi instalado a estação de trabalho do usuário de uma rede, disquete ou outra mídia externa. Após receber esse evento, o serviço geralmente Retorna S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Solicita que o serviço de cria uma instância adicional de um provedor. Se o serviço oferece suporte a essa operação, ele deve chamar [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md). Se o serviço não oferece suporte a essa operação, ele poderá retornar MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Solicita que o serviço excluir uma instância do provedor. Se o serviço oferece suporte a essa operação, ele deve chamar [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md). Se o serviço não oferece suporte a essa operação, ele poderá retornar MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> O serviço está sendo removido. Após receber esse evento, o serviço pode executar qualquer tarefa de limpeza que deve ser feita antes que o serviço termina e depois retornamos com um valor de sucesso. Se o usuário cancelar a remoção, o serviço deve retornar MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> [in] Contagem de valores de propriedade na matriz apontado pelo parâmetro _lpProps_ . O valor do parâmetro _cValues_ é zero se MAPI está passando sem valores de propriedade. 
    
 _lpProps_
  
> [in] Ponteiro para uma matriz opcional de [SPropValue](spropvalue.md) estruturas indicando valores para propriedades de suporte para o provedor que a função usará na configuração do serviço de mensagem. A função apenas usa esse parâmetro se o parâmetro _ulContext_ for definido como MSG_SERVICE_CONFIGURE. Esse parâmetro normalmente é usado para passar o caminho para um arquivo para um serviço baseado em arquivo, como um serviço de catálogo de endereços pessoal. Se o sinalizador MSG_SERVICE_CONFIGURE não será passado no parâmetro _ulFlags_ , o parâmetro _lpProps_ deve ser zero. 
    
 _lpProviderAdmin_
  
> [in] Ponteiro para uma interface de [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que a função pode usar para localizar as seções de perfil para um provedor específico no serviço de mensagem atual. 
    
 _lppMapiError_
  
> [out] Ponteiro para uma estrutura [MAPIERROR](mapierror.md) . A estrutura é alocada com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . Todos os membros são opcionais, embora a maioria das estruturas conterá uma cadeia de caracteres de mensagem de erro válido no membro _lpszError_ . Se os membros _lpszComponent_ ou _lpszError_ da estrutura estiverem presentes, sua memória deve ser eventualmente liberada por uma única chamada de [MAPIFreeBuffer](mapifreebuffer.md) na estrutura de base. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_UNCONFIGURED 
  
> O provedor de serviço não foi configurado. 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor não oferece suporte a alterações em seus objetos ou não oferece suporte a notificação de alterações. 
    
MAPI_E_BAD_CHARWIDTH 
  
> Tanto o sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode, ou MAPI_UNICODE não foi definido e a implementação só oferece suporte a Unicode.
    
## <a name="remarks"></a>Coment�rios

Uma função definida usando o protótipo de função **MSGSERVICEENTRY** permite que os serviços de mensagens para configurar sozinhos ou para executar outras ações específicas do serviço. A função principalmente fornece uma caixa de diálogo na qual o usuário pode alterar configurações específicas para o serviço de mensagem. Ele também pode oferecer suporte configuração programática usando a matriz de valor de propriedade passada no parâmetro _lpProps_ . Configuração programática é opcional, a menos que o serviço suporta o Assistente de perfil, para os quais é necessário. 
  
MAPI chama esse ponto de entrada do aplicativo de painel de controle ou em resposta a um aplicativo cliente chamar [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
MAPI coloca o nome da função que um serviço de mensagem usa para o protótipo **MSGSERVICEENTRY** mas prefira o nome **ServiceEntry**sem restrição. Não há nenhuma restrição quanto o ordinal da função e um único provedor DLL pode conter mais de uma função. No entanto, apenas um das funções pode ser nomeado **ServiceEntry**. 
  
Um serviço de mensagem pode usar a função [BuildDisplayTable](builddisplaytable.md) e o método [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) para simplificar a implementação de caixa de diálogo configuração. 
  
É possível que um usuário cancelar uma operação de MSG_SERVICE_UNINSTALL. Nesse caso, a função **ServiceEntry** deve verificar com o usuário para verificar se o serviço não deve ser removido e retornar MAPI_E_USER_CANCEL se o serviço permanecerá instalado. 
  
Uma função com base em protótipo **MSGSERVICEENTRY** retorna um dos valores HRESULT listados. MAPI encaminha esse valor ao responder a chamada de um cliente para [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Serviços de mensagem que exportar uma função de entrada de serviço devem incluir as propriedades de **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) e o **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) na seção serviço de mensagem do MAPISVC. 
  

