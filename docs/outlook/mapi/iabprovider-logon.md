---
title: IABProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABProvider.Logon
api_type:
- COM
ms.assetid: f9468715-1674-4d14-81c8-2f24dbaa0453
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 59c6d4a05c91511ad8c481fd4ddbe42396442190
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348780"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece uma conexão com uma sessão ativa.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG ulFlags,
  ULONG FAR * lpulcbSecurity,
  LPBYTE FAR * lppbSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPABLOGON FAR * lppABLogon
);
```

## <a name="parameters"></a>Parâmetros

 _lpMAPISup_
  
> [in] Um ponteiro para o objeto de suporte do provedor de agendas de endereços.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai da caixa de diálogo de logon que o método **logon** exibe, se permitido. O _parâmetro ulUIParam_ contém o valor do parâmetro do mesmo nome passado para MAPI na chamada anterior para a [função MAPILogonEx.](mapilogonex.md) 
    
 _lpszProfileName_
  
> [in] Um ponteiro para o nome do perfil da sessão.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o logon é realizado. Os sinalizadores a seguir podem ser definidos:
    
AB_NO_DIALOG 
  
> O provedor não deve exibir uma caixa de diálogo durante o logon. Se esse sinalizador não estiver definido, o provedor poderá exibir uma caixa de diálogo para solicitar ao usuário informações de configuração ausentes.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **o logon** retorne com êxito, possivelmente antes da finalização do processo de logon. 
    
MAPI_UNICODE 
  
> Todas as cadeias de caracteres devem estar no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, as cadeias de caracteres deverão estar no formato ANSI.
    
 _lpulcbSecurity_
  
> [in, out] Um ponteiro para o tamanho, em bytes, da estrutura de credenciais de segurança apontada pelo _parâmetro lppbSecurity._ Na entrada, o valor deve ser não zero; na saída, o valor deve ser zero. Em ambos os casos, os ponteiros devem ser válidos. 
    
 _lppbSecurity_
  
> [in, out] Um ponteiro para um ponteiro para credenciais de segurança. Na entrada, o valor deve ser não zero; na saída, o valor deve ser zero. Em ambos os casos, o ponteiro deve ser válido.
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para uma [estrutura MAPIERROR.](mapierror.md) O  _parâmetro lppMAPIError_ pode ser definido como NULL se não houver **estrutura MAPIERROR** a ser retornada. 
    
 _lppABLogon_
  
> [out] Um ponteiro para um ponteiro para o objeto de logon do provedor.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Uma conexão com uma sessão ativa foi estabelecida com êxito.
    
MAPI_E_FAILONEPROVIDER 
  
> O provedor não pode fazer logoff, mas o MAPI pode continuar a fazer logoff nos outros provedores no serviço de mensagens ao qual o provedor pertence. 
    
MAPI_E_UNCONFIGURED 
  
> O provedor tem informações insuficientes para concluir o logon. MAPI calls the provider's message service entry function.
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para dar suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para dar suporte às informações de localidade do cliente.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão **Cancelar** na caixa de diálogo de logon. 
    
## <a name="remarks"></a>Comentários

As conexões são estabelecidas com cada provedor de agendas no perfil de sessão quando um cliente chama o método [IMAPISession::OpenAddressBook.](imapisession-openaddressbook.md) **OpenAddressBook** chama o método de **Logon** de cada provedor. 
  
O nome de perfil apontado pelo parâmetro _lpszProfileName_ é exibido no conjunto de caracteres do cliente do usuário, conforme indicado pela presença ou ausência do sinalizador MAPI_UNICODE no parâmetro _ulFlags._ 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Na implementação do método **Logon,** chame o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar um identificador exclusivo ou estrutura [MAPIUID.](mapiuid.md) Cada um dos seus objetos terá um identificador de entrada que inclui este **MAPIUID**. MAPI uses the **MAPIUID** to match an object with its provider. Por exemplo, quando um cliente chama o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir um usuário de mensagens, **OpenEntry** examina a parte **MAPIUID** do identificador de entrada que foi passado e corresponde a ela com um **MAPIUID** registrado por um provedor de agendamento de endereços. 
  
Se um cliente faz logon no provedor mais de uma vez, talvez você queira registrar um **MAPIUID** diferente para cada logon. O registro de estruturas **MAPIUID** exclusivas permite que o MAPI roteie corretamente as solicitações para a instância de provedor apropriada. No entanto, talvez você queira que cada objeto de logon compartilhe um **MAPIUID.** Nesse caso, você deve ser capaz de lidar com o roteamento por conta própria em vez de depender de MAPI. Para obter mais informações sobre como criar um **MAPIUID,** consulte [Registrando identificadores](registering-service-provider-unique-identifiers.md)exclusivos do provedor de serviços.
  
O objeto de suporte que MAPI passa para o método **Logon** no parâmetro _lpMAPISup_ fornece acesso a muitos dos métodos incluídos na interface [IMAPISupport : IUnknown.](imapisupportiunknown.md) MAPI creates a support object that is customized to your type of provider. Por exemplo, se você precisar fazer logon em um sistema de mensagens ou serviço de diretório subjacente ao estabelecer sua conexão, poderá chamar o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para recuperar credenciais de segurança para esta sessão de logon específica. 
  
Se **Logon** for bem-sucedido, chame o método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do objeto de suporte para incrementar sua contagem de referência. Isso permite que seu provedor mantenha o ponteiro do objeto de suporte para o restante da sessão. Se você não chamar esse **método AddRef,** o MAPI descarregará seu provedor. 
  
Você pode incluir o nome do perfil passado no parâmetro  _lpszProfileName_ em caixas de diálogo de erro, telas de logon ou outras interfaces do usuário. Para usar o nome do perfil, copie-o para o armazenamento que você alocou. 
  
Crie um objeto de logon e retorne um ponteiro para ele no _parâmetro lppABLogon._ MAPI uses this logon object to make calls to the methods in your [IABLogon](iablogoniunknown.md) implementation. 
  
Se você precisar de uma senha durante o logon, exibirá uma caixa de diálogo de logon somente se o sinalizador AB_NO_DIALOG não estiver definido. Se o usuário cancelar o processo de **logon,** normalmente clicando no botão Cancelar na caixa de diálogo, retorne MAPI_E_USER_CANCEL logon . 
  
Normalmente, quando um provedor de agendas não consegue fazer logon, o MAPI desabilita o serviço de mensagens ao qual pertence o provedor com falha— ou seja, o MAPI não tentará estabelecer conexões para nenhum dos outros provedores que pertencem ao serviço pelo resto do tempo de vida da sessão. No entanto, se o provedor não puder estabelecer uma conexão e você quiser não desabilitar todo o serviço, retorne MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED. O MAPI não desabilitará o serviço de mensagens ao qual o provedor pertence. 
  
Retorne MAPI_E_FAILONEPROVIDER se ocorrer um erro que não seja sério o suficiente para impedir que os outros provedores no serviço de mensagens estabeleem conexões. Retorne MAPI_E_UNCONFIGURED se as informações de configuração necessárias não puderem ser exibidas no perfil e você não puder exibir uma caixa de diálogo para solicitar ao usuário. O MAPI responderá chamando a função de ponto de entrada do serviço de mensagens do provedor com o MSG_SERVICE_CONFIGURE definido como o parâmetro  _ulContext_ para dar ao serviço a chance de se configurar, programaticamente ou usando uma folha de propriedades. Quando a função de ponto de entrada do serviço de mensagens tiver sido concluída, o MAPI recuperará o logon. 
  
## <a name="see-also"></a>Confira também



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

