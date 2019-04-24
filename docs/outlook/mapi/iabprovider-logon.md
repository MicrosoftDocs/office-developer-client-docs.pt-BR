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
  
> no Um ponteiro para o objeto de suporte do provedor do catálogo de endereços.
    
 _ulUIParam_
  
> no Uma alça para a janela pai da caixa de diálogo de logon que o método de **logon** exibe, se permitido. O parâmetro _ulUIParam_ contém o valor do parâmetro do mesmo nome passado para MAPI na chamada anterior à função [funçãomapilogonex](mapilogonex.md) . 
    
 _lpszProfileName_
  
> no Um ponteiro para o nome do perfil da sessão.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o logon é executado. Os seguintes sinalizadores podem ser definidos:
    
AB_NO_DIALOG 
  
> O provedor não deve exibir uma caixa de diálogo durante o logon. Se esse sinalizador não for definido, o provedor poderá exibir uma caixa de diálogo solicitando que o usuário tenha informações de configuração ausentes.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **logon** seja retornado com êxito, possivelmente antes da conclusão do processo de logon. 
    
MAPI_UNICODE 
  
> Todas as cadeias de caracteres devem estar no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem estar no formato ANSI.
    
 _lpulcbSecurity_
  
> [in, out] Um ponteiro para o tamanho, em bytes, da estrutura de credenciais de segurança apontada pelo parâmetro _lppbSecurity_ . Na entrada, o valor deve ser diferente de zero; na saída, o valor deve ser zero. Em ambos os casos, os ponteiros devem ser válidos. 
    
 _lppbSecurity_
  
> [in, out] Um ponteiro para um ponteiro para credenciais de segurança. Na entrada, o valor deve ser diferente de zero; na saída, o valor deve ser zero. Em ambos os casos, o ponteiro deve ser válido.
    
 _lppMAPIError_
  
> bota Um ponteiro para um ponteiro para uma estrutura [MAPIERROR](mapierror.md) . O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** a ser retornada. 
    
 _lppABLogon_
  
> bota Um ponteiro para um ponteiro para o objeto de logon do provedor.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Uma conexão com uma sessão ativa foi estabelecida com êxito.
    
MAPI_E_FAILONEPROVIDER 
  
> O provedor não pode fazer logon, mas o MAPI pode continuar a fazer logon em outros provedores no serviço de mensagens aos quais o provedor pertence. 
    
MAPI_E_UNCONFIGURED 
  
> O provedor não tem informações suficientes para concluir o logon. MAPI chama a função de entrada de serviço de mensagem do provedor.
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para dar suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para dar suporte às informações de localidade do cliente.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo de logon. 
    
## <a name="remarks"></a>Comentários

As conexões são estabelecidas com cada provedor de catálogo de endereços no perfil de sessão quando um cliente chama o método [IMAPISession:: OpenAddressBook](imapisession-openaddressbook.md) . **OpenAddressBook** , em seguida, chama o método de **logon** de cada provedor. 
  
O nome do perfil apontado pelo parâmetro _lpszProfileName_ é exibido no conjunto de caracteres do cliente do usuário, conforme indicado pela presença ou ausência do sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ . 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Na sua implementação do método de **logon** , chame o método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) para registrar um identificador exclusivo ou uma estrutura [MAPIUID](mapiuid.md) . Cada um dos seus objetos terá um identificador de entrada que inclui este **MAPIUID**. MAPI usa o **MAPIUID** para corresponder a um objeto com seu provedor. Por exemplo, quando um cliente chama o método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir um usuário de mensagens, **OpenEntry** examina a parte **MAPIUID** do identificador de entrada que foi passado e a corresponde a um **MAPIUID** registrado por um provedor de catálogo de endereços. 
  
Se um cliente fizer logon no seu provedor mais de uma vez, talvez você queira registrar um **MAPIUID** diferente para cada logon. O registro de estruturas exclusivas do **MAPIUID** HABILITA o MAPI a rotear corretamente as solicitações para a instância apropriada do provedor. No enTanto, talvez você queira que todos os objetos de logon compartilhem um **MAPIUID**. Nesse caso, você deve ser capaz de lidar com o próprio roteamento em vez de confiar no MAPI. Para obter mais informações sobre como criar um **MAPIUID**, consulte [registro de identificadorEs exclusivos do provedor de serviços](registering-service-provider-unique-identifiers.md).
  
O objeto de suporte que o MAPI passa para seu método de **logon** no parâmetro _lpMAPISup_ fornece acesso a muitos dos métodos incluídos na interface [IMAPISupport: IUnknown](imapisupportiunknown.md) . O MAPI cria um objeto de suporte que é personalizado para o seu tipo de provedor. Por exemplo, se você precisar fazer logon em um sistema de mensagens subjacente ou serviço de diretório ao estabelecer sua conexão, você pode chamar o método [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) para recuperar as credenciais de segurança para essa sessão de logon específica. 
  
Se o **logon** for bem-sucedido, certifique-se de chamar o método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) do objeto support para incrementar sua contagem de referência. Isso permite que seu provedor Mantenha o ponteiro do objeto support no restante da sessão. Se você não chamar este método **AddRef** , o MAPI descarregará seu provedor. 
  
Você pode incluir o nome do perfil passado no parâmetro _lpszProfileName_ nas caixas de diálogo de erro, telas de logon ou outras interfaces de usuário. Para usar o nome do perfil, copie-o para o armazenamento que você alocou. 
  
Crie um objeto de logon e retorne um ponteiro para ele no parâmetro _lppABLogon_ . MAPI usa este objeto de logon para fazer chamadas para os métodos na sua implementação do [IABLogon](iablogoniunknown.md) . 
  
Se você precisar de uma senha durante o logon, exiba uma caixa de diálogo de logon somente se o sinalizador AB_NO_DIALOG não estiver definido. Se o usuário cancelar o processo de logon, geralmente clicando no botão **Cancelar** na caixa de diálogo, retornar MAPI_E_USER_CANCEL do **logon**.
  
Normalmente, quando um provedor de catálogo de endereços não pode fazer logon, o MAPI desabilita o serviço de mensagens ao qual o provedor de falha pertence, ou seja, o MAPI não tentará estabelecer conexões para qualquer um dos outros provedores que pertencem ao serviço para o restante da sessão marca. No enTanto, se o provedor não puder estabelecer uma conexão e você quiser não desabilitar todo o serviço, retorne MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED. O MAPI não desabilitará o serviço de mensagens ao qual o provedor pertence. 
  
Retornar MAPI_E_FAILONEPROVIDER se ocorrer um erro que não seja grave o suficiente para impedir que outros provedores no serviço de mensagens estabeleçam conexões. Retornar MAPI_E_UNCONFIGURED se as informações de configuração necessárias estiverem ausentes do perfil e você não puder exibir uma caixa de diálogo para solicitar o usuário. O MAPI responderá chamando a função de ponto de entrada do serviço de mensagens do provedor com o MSG_SERVICE_CONFIGURE definido como o parâmetro _ulContext_ para dar ao serviço uma oportunidade de configurar a si próprio, programaticamente ou usando uma folha de propriedades. Quando a função de ponto de entrada do serviço de mensagens terminar, o MAPI repete o logon. 
  
## <a name="see-also"></a>Confira também



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

