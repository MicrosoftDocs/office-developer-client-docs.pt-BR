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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 56a5f153dbd563397b9216af32a715692d0876d7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341605"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define um protótipo para uma função de ponto de entrada de serviço de mensagem para dar suporte à configuração de serviço de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi. h  <br/> |
|Função definida implementada por:  <br/> |Serviços de mensagens  <br/> |
|Função definida chamada por:  <br/> |MAPI  <br/> |
   
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

## <a name="parameters"></a>Parâmetros

 _hInstance_
  
> no Identificador da instância do serviço providerDLL. Normalmente, o identificador é usado para recuperar recursos. 
    
 _lpMalloc_
  
> no Ponteiro para um objeto de alocador de memória expondo a interface **IMalloc** do OLE. O serviço de mensagens pode precisar usar esse método de alocação quando estiver trabalhando com determinadas interfaces, como **IStream**. 
    
 _lpMAPISup_
  
> no Ponteiro para uma implementação de interface [IMAPISupport: IUnknown](imapisupportiunknown.md) . 
    
 _ulUIParam_
  
> no Um valor específico de implementação usado para passar informações da interface do usuário para uma função ou zero. O parâmetro _ulUIParam_ é o identificador de janela pai da caixa de diálogo de configuração e é do tipo HWND (conversão em um ULONG_PTR). Um valor igual A zero indica que não há janela pai. 
    
 _ulFlags_
  
> no Bitmask de sinalizadores que indicam opções para a função de entrada de serviço. Os seguintes sinalizadores podem ser definidos:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> A interface de usuário da configuração do serviço deve exibir a configuração atual, mas não permitir que o usuário a altere. 
    
SERVICE_UI_ALLOWED 
  
> Permite que uma caixa de diálogo de configuração seja exibida se necessário. Quando o sinalizador SERVICE_UI_ALLOWED estiver definido, a caixa de diálogo deve ser exibida somente se a matriz de valor da propriedade _lpProps_ estiver vazia ou não contiver uma configuração válida. Se SERVICE_UI_ALLOWED não estiver definido, uma caixa de diálogo ainda poderá ser exibida se o sinalizador SERVICE_UI_ALWAYS estiver definido. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Solicita que a caixa de diálogo de configuração do provedor ativo seja exibida na parte superior de outras caixas de diálogo. 
    
SERVICE_UI_ALWAYS 
  
> Requer que o serviço de mensagens exiba uma caixa de diálogo de configuração. Se o sinalizador SERVICE_UI_ALWAYS não estiver definido, uma caixa de diálogo de configuração ainda poderá ser exibida se o sinalizador SERVICE_UI_ALLOWED estiver definido e as informações de configuração válidas não estiverem disponíveis na matriz de valor da propriedade _lpProps_ . O SERVICE_UI_ALLOWED ou o SERVICE_UI_ALWAYS deve ser definido para permitir que uma interface de usuário seja exibida. 
    
 _ulContext_
  
> no A operação de configuração que o MAPI está executando no momento. O parâmetro _ulContext_ conterá um dos seguintes valores: 
    
MSG_SERVICE_CONFIGURE 
  
> As alterações na configuração do serviço devem ser feitas no perfil. Se o sinalizador SERVICE_UI_ALWAYS estiver definido, o serviço deverá exibir sua caixa de diálogo de configuração. A caixa de diálogo também deverá ser exibida se o sinalizador SERVICE_UI_ALLOWED estiver definido e se o parâmetro _lpProps_ estiver vazio ou não contiver dados de configuração válidos. Se _lpProps_ contiver dados válidos, nenhuma caixa de diálogo deve ser exibida e o serviço deve usar esses dados para fazer a alteração da configuração. 
    
MSG_SERVICE_CREATE 
  
> O serviço está sendo adicionado a um perfil. Se o sinalizador SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED estiver definido, o serviço deverá exibir sua caixa de diálogo de configuração. Se nenhum sinalizador estiver definido, o serviço deve falhar. 
    
MSG_SERVICE_DELETE 
  
> O serviço está sendo removido de um perfil. Depois de receber esse evento, o serviço deve retornar S_OK.
    
MSG_SERVICE_INSTALL 
  
> O serviço foi instalado na estação de trabalho do usuário a partir de uma rede, disquete ou outra mídia externa. Depois de receber esse evento, o serviço normalmente retorna S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Solicita que o serviço crie uma instância adicional de um provedor. Se o serviço oferecer suporte a essa operação, ele deverá chamar [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md). Se o serviço não oferecer suporte a essa operação, poderá retornar MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Solicita que o serviço exclua uma instância de provedor. Se o serviço oferecer suporte a essa operação, ele deverá chamar [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md). Se o serviço não oferecer suporte a essa operação, poderá retornar MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> O serviço está sendo removido. Depois de receber esse evento, o serviço pode executar qualquer tarefa de limpeza que deve ser realizada antes que o serviço seja encerrado e, em seguida, retorne com um valor de sucesso. Se o usuário cancelar a remoção, o serviço deverá retornar MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> no Contagem de valores de propriedade na matriz apontada pelo parâmetro _lpProps_ . O valor do parâmetro _cValues_ será zero se o MAPI não passar nenhum valor de propriedade. 
    
 _lpProps_
  
> no Ponteiro para uma matriz opcional de estruturas [SPropValue](spropvalue.md) indicando valores para propriedades suportadas pelo provedor que a função usará na configuração do serviço de mensagens. A função só usa esse parâmetro se o parâmetro _ulContext_ estiver definido como MSG_SERVICE_CONFIGURE. Esse parâmetro é comumente usado para passar o caminho para um arquivo de um serviço baseado em arquivo, como um serviço de catálogo de endereços pessoal. Se o sinalizador MSG_SERVICE_CONFIGURE não for passado no parâmetro _parâmetroulflags_ , o parâmetro _lpProps_ deverá ser zero. 
    
 _lpProviderAdmin_
  
> no Ponteiro para uma interface [IProviderAdmin: IUnknown](iprovideradminiunknown.md) que a função pode usar para localizar seções de perfil de um provedor específico no serviço de mensagens atual. 
    
 _lppMapiError_
  
> bota Ponteiro para uma estrutura [MAPIERROR](mapierror.md) . A estrutura é alocada com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . Todos os membros são opcionais, embora a maioria das estruturas contenha uma cadeia de mensagem de erro válida no membro _lpszError_ . Se os membros _lpszComponent_ ou _lpszError_ da estrutura estiverem presentes, sua memória deverá ser liberada por uma única chamada para [MAPIFreeBuffer](mapifreebuffer.md) na estrutura base. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados. 
    
MAPI_E_UNCONFIGURED 
  
> O provedor de serviços não foi configurado. 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor não oferece suporte a alterações em seus objetos ou não dá suporte à notificação de alterações. 
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não tem suporte para Unicode ou o MAPI_UNICODE não foi definido e a implementação só oferece suporte a Unicode.
    
## <a name="remarks"></a>Comentários

Uma função definida usando o protótipo de função **MSGSERVICEENTRY** permite que os serviços de mensagens se configurem ou realizem outras ações específicas do serviço. A função fornece principalmente uma caixa de diálogo na qual o usuário pode alterar as configurações específicas do serviço de mensagens. Também pode oferecer suporte à configuração programática usando a matriz de valor de propriedade passada no parâmetro _lpProps_ . A configuração programática é opcional, a menos que o serviço dê suporte ao assistente de perfil, para o qual é necessário. 
  
MAPI chama esse ponto de entrada do aplicativo do painel de controle ou em resposta a um aplicativo cliente chamando [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) ou [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
O MAPI não coloca nenhuma restrição no nome da função que um serviço de mensagem usa para o protótipo **MSGSERVICEENTRY** , mas prefere o nome de **entrada**. Não há nenhuma restrição no ordinal para a função e uma única DLL de provedor pode conter mais de uma função. No enTanto, apenas uma das funções pode ser nomeada como de **entrada**. 
  
Um serviço de mensagens pode usar a função [BuildDisplayTable](builddisplaytable.md) e o método [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) para simplificar a implementação da caixa de diálogo de configuração. 
  
É possível que um usuário cancele uma operação MSG_SERVICE_UNINSTALL. Nesse caso, a função de serviço de **entrada** deve verificar com o usuário se o serviço não deve ser removido e retornar MAPI_E_USER_CANCEL se o serviço permanecer instalado. 
  
Uma função com base no protótipo **MSGSERVICEENTRY** retorna um dos valores HRESULT listados. O MAPI encaminha esse valor ao responder à chamada de um cliente para [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Os serviços de mensagens que exportam uma função de entrada de serviço devem incluir as propriedades **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) e **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) na seção serviço de mensagens de MAPISVC. INF. 
  

