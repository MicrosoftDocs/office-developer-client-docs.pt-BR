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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8cb7934919722139622b6caf3aac741c9b2e54c5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582459"
---
# <a name="iabproviderlogon"></a>IABProvider::Logon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Estabelece uma conexão para uma sessão ativa.
  
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
  
> [in] Um ponteiro para o objeto de suporte do provedor de catálogo de endereços.
    
 _ulUIParam_
  
> [in] Uma alça para a janela pai para a caixa de diálogo de logon que exibe o método de **Logon** , se permitido. O parâmetro _ulUIParam_ contém o valor do parâmetro do mesmo nome passado para MAPI na chamada para a função [MAPILogonEx](mapilogonex.md) anterior. 
    
 _lpszProfileName_
  
> [in] Um ponteiro para o nome do perfil da sessão.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o logon é executado. Sinalizadores a seguir podem ser definidos:
    
AB_NO_DIALOG 
  
> O provedor não deve exibir uma caixa de diálogo durante o logon. Se esse sinalizador não estiver definido, o provedor pode exibir uma caixa de diálogo para solicitar ao usuário para faltando informações de configuração.
    
MAPI_DEFERRED_ERRORS 
  
> Permite o **Logon** retornar com êxito, possivelmente antes do processo de logon for concluído. 
    
MAPI_UNICODE 
  
> Todas as cadeias de caracteres devem estar no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres devem estar no formato ANSI.
    
 _lpulcbSecurity_
  
> [além, out] Um ponteiro para o tamanho, em bytes, da estrutura de credenciais de segurança apontado pelo parâmetro _lppbSecurity_ . Na entrada, o valor deve ser diferente de zero; na saída, o valor deve ser zero. Em ambos os casos, os ponteiros devem ser válidos. 
    
 _lppbSecurity_
  
> [além, out] Um ponteiro para um ponteiro para as credenciais de segurança. Na entrada, o valor deve ser diferente de zero; na saída, o valor deve ser zero. Em ambos os casos, o ponteiro deve ser válido.
    
 _lppMAPIError_
  
> [out] Um ponteiro para um ponteiro para uma estrutura [MAPIERROR](mapierror.md) . O parâmetro _lppMAPIError_ pode ser definido como NULL se não houver nenhuma estrutura **MAPIERROR** para retornar. 
    
 _lppABLogon_
  
> [out] Um ponteiro para um ponteiro para o objeto de logon do provedor.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Uma conexão para uma sessão ativa foi estabelecida com êxito.
    
MAPI_E_FAILONEPROVIDER 
  
> O provedor não pode fazer logon, mas MAPI pode continuar a fazer logon com os outros provedores no serviço de mensagem ao qual o provedor pertence. 
    
MAPI_E_UNCONFIGURED 
  
> O provedor tem informações suficientes para concluir o logon. Função de entrada de serviço de mensagem do provedor a chamadas de MAPI.
    
MAPI_E_UNKNOWN_CPID 
  
> O servidor não está configurado para oferecer suporte à página de código do cliente.
    
MAPI_E_UNKNOWN_LCID 
  
> O servidor não está configurado para oferecer suporte a informações de localidade do cliente.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** na caixa de diálogo de logon. 
    
## <a name="remarks"></a>Comentários

Conexões estabelecidas com cada provedor de catálogo de endereços no perfil da sessão quando um cliente chama o método [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) . **OpenAddressBook** chama o método de **Logon** do cada provedor. 
  
O nome do perfil apontado pelo parâmetro _lpszProfileName_ é exibido no conjunto de caracteres do cliente do usuário conforme indicado pela presença ou ausência do sinalizador MAPI_UNICODE no parâmetro _ulFlags_ . 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Em sua implementação do método **Logon** , chame o método de [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) para registrar um identificador exclusivo, ou uma estrutura [MAPIUID](mapiuid.md) . Cada um dos seus objetos terão um identificador de entrada que inclua este **MAPIUID**. O MAPI usa o **MAPIUID** para corresponder a um objeto com seu provedor. Por exemplo, quando um cliente chama o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir um usuário de mensagens, **OpenEntry** examina a parte **MAPIUID** do identificador de entrada que foi passado e faz a correspondência com um **MAPIUID** registrados por um provedor de catálogo de endereços. 
  
Se um cliente fizer logon ao seu provedor de mais de uma vez, convém registrar um **MAPIUID** de diferentes para cada logon. Registrar as estruturas **MAPIUID** exclusivas permite MAPI corretamente rotear solicitações para a instância do provedor apropriado. No entanto, convém ter cada objeto de logon compartilhar um **MAPIUID**. Nesse caso, você deve ser capaz de lidar com o roteamento sozinho, em vez de depender de MAPI. Para obter mais informações sobre como criar um **MAPIUID**, consulte [Registrando serviço provedor exclusivo identificadores](registering-service-provider-unique-identifiers.md).
  
O objeto de suporte a MAPI passa para seu método de **Logon** no parâmetro _lpMAPISup_ fornece acesso a muitos dos métodos incluídos no [IMAPISupport: IUnknown](imapisupportiunknown.md) interface. MAPI cria um objeto de suporte que é personalizado para seu tipo de provedor. Por exemplo, se você precisa fazer logon um sistema de mensagens subjacente ou o serviço de diretório ao estabelecer sua conexão, você pode chamar o método [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) para recuperar as credenciais de segurança para esta sessão de logon específica. 
  
Se o **Logon** for bem-sucedido, certifique-se de que você chamar o suporte ao método do objeto [AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) para incrementar sua contagem de referência. Isso permite que o seu provedor mantenha o ponteiro de objeto de suporte para o restante da sessão. Se você não chamar esse método **AddRef** , MAPI descarregará o seu provedor. 
  
Você pode incluir o nome do perfil passado no parâmetro _lpszProfileName_ em caixas de diálogo de erro, telas de logon ou outras interfaces de usuário. Para usar o nome do perfil, copie-o para armazenamento que você tiver alocado. 
  
Criar um objeto de logon e retornar um ponteiro para ele no parâmetro _lppABLogon_ . MAPI usa esse objeto de logon para fazer chamadas para os métodos na sua implementação [IABLogon](iablogoniunknown.md) . 
  
Se você precisar de uma senha durante o logon, exibe uma caixa de diálogo logon apenas se o sinalizador AB_NO_DIALOG não estiver definido. Se o usuário cancelar o processo de logon, geralmente clicando no botão **Cancelar** na caixa de diálogo retorne MAPI_E_USER_CANCEL de **Logon**.
  
Normalmente, quando um provedor de catálogo de endereços não pode fazer logon, MAPI desabilita o serviço de mensagem ao qual pertence o provedor está falhando — ou seja, MAPI não tentará estabelecer conexões por qualquer um dos outros provedores que pertencem ao serviço para o restante da sessão tempo de vida. No entanto, se o seu provedor não é possível estabelecer uma conexão e você não deseja desabilitar todo o serviço, retorne MAPI_E_FAILONEPROVIDER ou MAPI_E_UNCONFIGURED. MAPI não desabilitará o serviço de mensagem ao qual o provedor pertence. 
  
Retorno MAPI_E_FAILONEPROVIDER se ocorrer um erro que não é grave o suficiente para impedir que os outros provedores no serviço de mensagem estabelecer conexões. Retorne MAPI_E_UNCONFIGURED se as informações de configuração necessárias estão ausentes do perfil e você não pode exibir uma caixa de diálogo para solicitar ao usuário. MAPI responderá ao chamar a função de ponto de entrada do seu provedor mensagem serviço com MSG_SERVICE_CONFIGURE definido como o parâmetro _ulContext_ para fornecer o serviço a oportunidade de se configurar propriamente dito, seja programaticamente ou usar uma folha de propriedades. Quando a entrada de serviço de mensagem aponte concluiu a função, MAPI repete o logon. 
  
## <a name="see-also"></a>Confira também



[IABLogon::Logoff](iablogon-logoff.md)
  
[IABLogon::OpenEntry](iablogon-openentry.md)
  
[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)
  
[IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)

