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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427875"
---
# <a name="msgserviceentry"></a>MSGSERVICEENTRY

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define um protótipo para uma função de ponto de entrada do serviço de mensagens para dar suporte à configuração do serviço de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapispi.h  <br/> |
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
  
> [in] Alça da instância do provedor de serviçosDLL. O alça é normalmente usado para recuperar recursos. 
    
 _lpMalloc_
  
> [in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.** O serviço de mensagens pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**. 
    
 _lpMAPISup_
  
> [in] Ponteiro para uma [implementação de interface IMAPISupport : IUnknown.](imapisupportiunknown.md) 
    
 _ulUIParam_
  
> [in] Um valor específico de implementação usado para passar informações da interface do usuário para uma função ou zero. O  _parâmetro ulUIParam_ é o identificador da janela pai da caixa de diálogo de configuração e é do tipo HWND (cast to a ULONG_PTR). Um valor zero indica que não há janela pai. 
    
 _ulFlags_
  
> [in] Bitmask de sinalizadores indicando opções para a função de entrada de serviço. Os sinalizadores a seguir podem ser definidos:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
MSG_SERVICE_UI_READ_ONLY 
  
> A interface do usuário de configuração do serviço deve exibir a configuração atual, mas não permitir que o usuário a altere. 
    
SERVICE_UI_ALLOWED 
  
> Permite que uma caixa de diálogo de configuração seja exibida, se necessário. Quando o SERVICE_UI_ALLOWED de texto estiver definido, a caixa de diálogo deverá ser exibida somente se a matriz de valores da propriedade  _lpProps_ estiver vazia ou não tiver uma configuração válida. Se SERVICE_UI_ALLOWED não estiver definido, uma caixa de diálogo ainda poderá ser exibida se o sinalizador SERVICE_UI_ALWAYS estiver definido. 
    
UI_CURRENT_PROVIDER_FIRST 
  
> Solicita que a caixa de diálogo de configuração do provedor ativo seja exibida sobre outras caixas de diálogo. 
    
SERVICE_UI_ALWAYS 
  
> Requer que o serviço de mensagens exibir uma caixa de diálogo de configuração. Se o sinalizador SERVICE_UI_ALWAYS não estiver definido, uma caixa de diálogo de configuração ainda poderá ser exibida se o sinalizador SERVICE_UI_ALLOWED estiver definido e as informações de configuração válidas não estarão disponíveis na matriz de valores da propriedade _lpProps._ As SERVICE_UI_ALLOWED ou SERVICE_UI_ALWAYS devem ser definidas para permitir que uma interface do usuário seja exibida. 
    
 _ulContext_
  
> [in] A operação de configuração que o MAPI está executando no momento. O  _parâmetro ulContext_ conterá um dos seguintes valores: 
    
MSG_SERVICE_CONFIGURE 
  
> As alterações na configuração do serviço devem ser feitas no perfil. Se o SERVICE_UI_ALWAYS sinalizador estiver definido, o serviço deverá exibir sua caixa de diálogo de configuração. A caixa de diálogo também deverá ser exibida se o sinalizador SERVICE_UI_ALLOWED estiver definido e o parâmetro  _lpProps_ estiver vazio ou não tiver dados de configuração válidos. Se  _lpProps_ contiver dados válidos, nenhuma caixa de diálogo deverá ser exibida e o serviço deverá usar esses dados para fazer a alteração na configuração. 
    
MSG_SERVICE_CREATE 
  
> O serviço está sendo adicionado a um perfil. Se o sinalizador SERVICE_UI_ALWAYS ou SERVICE_UI_ALLOWED estiver definido, o serviço deverá exibir sua caixa de diálogo de configuração. Se nenhum sinalizador estiver definido, o serviço deve falhar. 
    
MSG_SERVICE_DELETE 
  
> O serviço está sendo removido de um perfil. Depois de receber esse evento, o serviço deve retornar S_OK.
    
MSG_SERVICE_INSTALL 
  
> O serviço foi instalado na estação de trabalho do usuário a partir de uma rede, disquete ou outra mídia externa. Depois de receber esse evento, o serviço geralmente retorna S_OK. 
    
MSG_SERVICE_PROVIDER_CREATE 
  
> Solicita que o serviço crie uma instância adicional de um provedor. Se o serviço suportar essa operação, ele deverá chamar [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md). Se o serviço não suportar essa operação, ele poderá retornar MAPI_E_NO_SUPPORT. 
    
MSG_SERVICE_PROVIDER_DELETE 
  
> Solicita que o serviço exclua uma instância do provedor. Se o serviço suportar essa operação, ele deverá chamar [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md). Se o serviço não suportar essa operação, ele poderá retornar MAPI_E_NO_SUPPORT.
    
MSG_SERVICE_UNINSTALL 
  
> O serviço está sendo removido. Depois de receber esse evento, o serviço pode executar qualquer tarefa de limpeza que deve ser feita antes do serviço terminar e, em seguida, retornar com um valor de sucesso. Se o usuário cancelar a remoção, o serviço deverá retornar MAPI_E_USER_CANCEL. 
    
 _cValues_
  
> [in] Contagem de valores de propriedade na matriz apontada pelo _parâmetro lpProps._ O valor do parâmetro  _cValues_ será zero se MAPI não estiver passando valores de propriedade. 
    
 _lpProps_
  
> [in] Ponteiro para uma matriz opcional de [estruturas SPropValue](spropvalue.md) indicando valores para propriedades com suporte do provedor que a função usará na configuração do serviço de mensagens. A função só usará esse parâmetro se o  _parâmetro ulContext_ estiver definido como MSG_SERVICE_CONFIGURE. Esse parâmetro é normalmente usado para passar o caminho para um arquivo para um serviço baseado em arquivo, como um serviço de agenda pessoal. Se o MSG_SERVICE_CONFIGURE sinalizador não for passado no  _parâmetro ulFlags,_ o parâmetro  _lpProps_ deverá ser zero. 
    
 _lpProviderAdmin_
  
> [in] Ponteiro para uma interface [IProviderAdmin:IUnknown](iprovideradminiunknown.md) que a função pode usar para localizar seções de perfil para um provedor específico no serviço de mensagens atual. 
    
 _lppMapiError_
  
> [out] Ponteiro para uma [estrutura MAPIERROR.](mapierror.md) A estrutura é alocada com a [função MAPIAllocateBuffer.](mapiallocatebuffer.md) Todos os membros são opcionais, embora a maioria das estruturas contenha uma cadeia de caracteres de mensagem de erro válida _no membro lpszError._ Se os membros  _lpszComponent_ ou  _lpszError_ da estrutura estão presentes, sua memória eventualmente deve ser liberada por uma única chamada para [MAPIFreeBuffer](mapifreebuffer.md) na estrutura base. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_UNCONFIGURED 
  
> O provedor de serviços não foi configurado. 
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
MAPI_E_NO_SUPPORT 
  
> O provedor não suporta alterações em seus objetos ou não suporta a notificação de alterações. 
    
MAPI_E_BAD_CHARWIDTH 
  
> O sinalizador MAPI_UNICODE foi definido e a implementação não dá suporte a Unicode ou MAPI_UNICODE não foi definido e a implementação só dá suporte a Unicode.
    
## <a name="remarks"></a>Comentários

Uma função definida usando o protótipo **de função MSGSERVICEENTRY** permite que os serviços de mensagens se configurem ou executem outras ações específicas do serviço. A função fornece principalmente uma caixa de diálogo na qual o usuário pode alterar configurações específicas para o serviço de mensagens. Ele também pode dar suporte à configuração programática usando a matriz de valores de propriedade passada no _parâmetro lpProps._ A configuração programática é opcional, a menos que o serviço suporte o Assistente de Perfil, para o qual ele é necessário. 
  
MAPI calls this entry point from the Control Panel application or in response to a client application calling [IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md) or [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
MAPI não coloca restrições no nome da função que um serviço de mensagem usa para o protótipo **MSGSERVICEENTRY,** mas prefere o nome **ServiceEntry**. Não há restrições no ordinal para a função, e um único provedor DLL pode conter mais de uma função. No entanto, apenas uma das funções pode ser chamada **de ServiceEntry**. 
  
Um serviço de mensagens pode usar a [função BuildDisplayTable](builddisplaytable.md) e o [método IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) para simplificar a implementação da caixa de diálogo de configuração. 
  
É possível que um usuário cancele uma operação MSG_SERVICE_UNINSTALL usuário. Nesse caso, a **função ServiceEntry** deve verificar com o usuário para verificar se o serviço não deve ser removido e retornar MAPI_E_USER_CANCEL se o serviço permanece instalado. 
  
Uma função baseada no protótipo **MSGSERVICEENTRY** retorna um dos valores HRESULT listados. MAPI forwards this value when responding to a client's call to [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). 
  
Os serviços de mensagem que exportam uma função de entrada de serviço devem incluir as propriedades **PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md)) e **PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)) na seção de serviço de mensagens de MAPISVC.INF. 
  

