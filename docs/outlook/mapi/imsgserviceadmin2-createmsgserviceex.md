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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310007"
---
# <a name="imsgserviceadmin2createmsgserviceex"></a>IMsgServiceAdmin2::CreateMsgServiceEx

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um serviço de mensagens ao perfil atual e retorna à UID do serviço recém-adicionada.
  
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
  
> no Um ponteiro para o nome do serviço de mensagens a ser adicionado. Esse nome de serviço de mensagem deve aparecer na seção **[serviços]** do arquivo MapiSvc. inf. 
    
 _lpszDisplayName_
  
> no Um ponteiro para o nome de exibição do serviço de mensagens a ser adicionado. O parâmetro _lpszDisplayName_ será ignorado se o serviço de mensagens tiver definido a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) no arquivo MapiSvc. inf.
    
 _ulUIParam_
  
> no Uma alça para a janela pai de qualquer caixa de diálogo ou Windows este método é exibido.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o serviço de mensagens é instalado. Os seguintes sinalizadores podem ser definidos:
    
MAPI_UNICODE
  
> Os parâmetros lpszService e lpszDisplayName devem ser convertidos em LPWSTR e interpretados como cadeias de caracteres Unicode.
    
SERVICE_NO_RESTART_WARNING
  
> Ao adicionar um novo serviço de mensagens ao perfil, o subsistema MAPI, com base em várias circunstâncias e critérios, geralmente determina que essa ação requer uma reinicialização do Outlook. Se o sinalizador SERVICE_NO_RESTART_WARNING não estiver incluído e a interface do usuário for baseada nos sinalizadores SERVICE_UI_ALWAYS e SERVICE_UI_ALLOWED e pelo menos um processo estiver conectado ao perfil atual, essa função exibirá a mensagem "você deve reiniciar o Outlook para que as alterações entrem em vigor. " Incluir o sinalizador SERVICE_NO_RESTART_WARNING suprime a exibição dessa mensagem de aviso.
    
SERVICE_UI_ALLOWED
  
> A interface do usuário de configuração do serviço de mensagens é permitida se necessário.
    
SERVICE_UI_ALWAYS
  
> O serviço de mensagens exibe sua folha de propriedades de configuração.
    
 _lpuidService_
  
> bota O ponteiro para a UID do serviço de mensagens adicionado.
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NOT_FOUND
  
> O nome do serviço de mensagens não está na seção **[serviços]** de MapiSvc. inf. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin2:: CreateMsgServiceEx** adiciona um serviço de mensagens ao perfil atual. **CreateMsgServiceEx** chama a função de ponto de entrada do serviço de mensagens para executar qualquer tarefa de configuração específica do serviço. Se o sinalizador SERVICE_UI_ALLOWED estiver definido no parâmetro _parâmetroulflags_ , o serviço de mensagens que estiver sendo instalado poderá exibir uma folha de propriedades, permitindo que o usuário defina suas configurações. 
  
O arquivo MapiSvc. inf contém a lista de provedores que compõem um serviço de mensagens e as propriedades de cada um. **CreateMsgServiceEx** primeiro cria uma nova seção de perfil para o serviço de mensagens e, em seguida, copia Todas as informações desse serviço do arquivo MapiSvc. inf para o perfil, criando novas seções para cada provedor. 
  
Depois que todas as informações tiverem sido copiadas de MapiSvc. inf, a função de ponto de entrada do serviço de mensagens, **MSGSERVICEENTRY**, será chamada com o valor MSG_SERVICE_CREATE definido no parâmetro _ulContext_ . Se o sinalizador SERVICE_UI_ALLOWED estiver definido no parâmetro _parâmetroulflags_ do método **CreateMsgServiceEx** , os valores nos parâmetros _ulUIParam_ e _parâmetroulflags_ também serão passados quando a função de ponto de entrada do serviço de mensagens for chamada. Os provedores de serviços devem exibir suas folhas de propriedades de configuração para que os usuários possam configurar o serviço de mensagens. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se o argumento **CreateMsgServiceEx** _LPUIDSERVICE_ não for nulo, a propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) do serviço de mensagem que foi adicionada ao perfil será retornada no **GUID** para o qual ele aponta. 
  
Passe o valor da propriedade **PR_SERVICE_UID** no parâmetro _lpuidService_ para o método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) para configurar o serviço. 
  
> [!CAUTION]
> A implementação do Microsoft Outlook 2010 do subsistema MAPI não oferece suporte ao MAPI_UNICODE e falhará se for usado. 
  
> [!IMPORTANT]
> A interface IMsgServiceAdmin2 é exposta pelo mesmo objeto que implementa a interface IMsgServiceAdmin e está disponível usando a implementação do subsistema MAPI do Outlook desde o Outlook 2003. Sua IID é definida da seguinte maneira: `#if !defined(INITGUID) || defined(USES_IID_IMsgServiceAdmin2)` >   `DEFINE_OLEGUID(IID_IMsgServiceAdmin2,0x00020387, 0, 0);`> > o _parâmetroulflags_ SERVICE_NO_RESTART_WARNING pode não estar definido no arquivo de cabeçalho baixável que você tem atualmente e, nesse caso, você pode adicioná-lo ao seu código usando o seguinte valor: >`#define SERVICE_NO_RESTART_WARNING 0x00000080`
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin2 : IMsgServiceAdmin](imsgserviceadmin2imsgserviceadmin.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

