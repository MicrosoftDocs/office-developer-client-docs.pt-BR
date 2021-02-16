---
title: IMsgServiceAdmin2CreateMsgServiceEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin2.CreateMsgServiceEx
api_type:
- COM
ms.assetid: 4910dabd-9380-4fde-a440-5c64d74c0bba
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: b7fe25491228f00f6865af963db36f27bae5d7a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410179"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um serviço de mensagem ao perfil atual e retorna o UID do serviço recém-adicionado.
  
```cpp
HRESULT CreateMsgServiceEx(
  LPSTR lpszService,
  LPSTR lpszDisplayName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags,    
  LPMAPIUID lpuidService
);
```

## <a name="parameters"></a>Parâmetros

 _lpszService_
  
> [in] Um ponteiro para o nome do serviço de mensagens a ser acrescentado. Esse nome de serviço de mensagem deve aparecer na seção **[Serviços]** do arquivo MapiSvc.inf. 
    
 _lpszDisplayName_
  
> [in] Um ponteiro para o nome de exibição do serviço de mensagens a ser acrescentado. O  _parâmetro lpszDisplayName_ será ignorado se o serviço de mensagens tiver definido a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) no arquivo MapiSvc.inf.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o serviço de mensagens é instalado. Os sinalizadores a seguir podem ser definidos:
    
MAPI_UNICODE
  
> Os parâmetros lpszService e lpszDisplayName devem ser lançados para LPWSTR e interpretados como cadeias de caracteres Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Ao adicionar um novo serviço de mensagens ao perfil, o subsistema MAPI, com base em várias circunstâncias e critérios, geralmente determina que essa ação requer uma reinicialização do Outlook. Se o sinalizador SERVICE_NO_RESTART_WARNING não estiver incluído e a interface do usuário for permitida, com base nos sinalizadores SERVICE_UI_ALWAYS e SERVICE_UI_ALLOWED, e pelo menos um processo estiver conectado ao perfil atual, essa função exibirá a mensagem "Você deve reiniciar o Outlook para que essas alterações entre em vigor". A inclusão SERVICE_NO_RESTART_WARNING sinalizador suprime a exibição dessa mensagem de aviso.
    
SERVICE_UI_ALLOWED
  
> A interface do usuário de configuração do serviço de mensagens é permitida, se necessário.
    
SERVICE_UI_ALWAYS
  
> O serviço de mensagens exibe sua folha de propriedades de configuração.
    
 _lpuidService_
  
> [out] O ponteiro para a UID do serviço de mensagens adicionado.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NOT_FOUND
  
> O nome do serviço de mensagens não está na seção **[Serviços]** de MapiSvc.inf. 
    
## <a name="remarks"></a>Comentários

O **método IMsgServiceAdmin2::CreateMsgServiceEx** adiciona um serviço de mensagem ao perfil atual. **CreateMsgServiceEx** chama a função de ponto de entrada do serviço de mensagens para executar qualquer tarefa de configuração específica do serviço. Se o SERVICE_UI_ALLOWED sinalizador for definido no parâmetro  _ulFlags,_ o serviço de mensagem que está sendo instalado poderá exibir uma folha de propriedades permitindo que o usuário defina suas configurações. 
  
O arquivo MapiSvc.inf contém a lista de provedores que comem um serviço de mensagens e as propriedades de cada um deles. **CreateMsgServiceEx** primeiro cria uma nova seção de perfil para o serviço de mensagens e, em seguida, copia todas as informações para esse serviço do arquivo MapiSvc.inf para o perfil, criando novas seções para cada provedor. 
  
Depois que todas as informações foram copiadas de MapiSvc.inf, a função de ponto de entrada do serviço de mensagens, **MSGSERVICEENTRY**, é chamada com o valor MSG_SERVICE_CREATE definido no parâmetro _ulContext._ Se o sinalizador SERVICE_UI_ALLOWED for definido no parâmetro _ulFlags_ do método **CreateMsgServiceEx,** os valores nos parâmetros _ulUIParam_ e _ulFlags_ também serão passados quando a função de ponto de entrada do serviço de mensagens for chamada. Os provedores de serviços devem exibir suas folhas de propriedades de configuração para que os usuários possam configurar o serviço de mensagens. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se o argumento **CreateMsgServiceEx** _lpuidService_ não for NULL, a propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço de mensagens que foi adicionado ao perfil será retornada no **GUID** ao qual ele aponta. 
  
Passe o valor da **propriedade PR_SERVICE_UID** parâmetro  _lpuidService_ para o método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar o serviço. 
  
> [!CAUTION]
> The Microsoft Outlook 2010 implementation of the MAPI subsystem does not support MAPI_UNICODE and will fail if it is used. 
  
> [!IMPORTANT]
> A interface IMsgServiceAdmin2 é exposta pelo mesmo objeto que implementa a interface IMsgServiceAdmin e está disponível usando a implementação do Outlook do subsistema MAPI desde o Outlook 2003. Sua IID é definida da seguinte maneira: > `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> O _SERVICE_NO_RESTART_WARNING ulFlags_ pode não ser definido no arquivo de header baixável que você tem no momento; nesse caso, você pode adicioná-lo ao seu código usando o seguinte valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

